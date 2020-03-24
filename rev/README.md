# Reverse engineering worksheet

Taken from Reverse Engineering for Beginners


<h2>Empty Functions</h2>


	f:
		ret



<h2>Returning Values</h2>

	f:
		mov eax, 123
		ret


<h2>Hello World</h2>

	CONST SEGMENT
	$SG3830 DB 'hello, world', 0AH, 00H
	CONST ENDS
	PUBLIC _main
	EXTRN _printf:PROC
	; Function compile flags: /Odtp
	_TEXT SEGMENT
	_main PROC
		push ebp
		mov ebp, esp
		push OFFSET $SG3830
		call _printf
		add esp, 4
		xor eax, eax
		pop ebp
		ret 0
	_main ENDP
	_TEXT ENDS


<h2>Function prologue Epilogue</h2>

	push ebp
	mov ebp, esp
	sub esp, X

	mov esp, ebp
	pop ebp
	ret 0

<h2>Stack</h2>

	.LC0:
		.string "hi! %d, %d, %d\n"
	f:
		push ebp
		mov ebp, esp
		push ebx
		sub esp, 660
		lea ebx, [esp+39]
		and ebx, -16 ; align pointer by 16-bit border
		mov DWORD PTR [esp], ebx ; s
		mov DWORD PTR [esp+20], 3
		mov DWORD PTR [esp+16], 2
		mov DWORD PTR [esp+12], 1
		mov DWORD PTR [esp+8], OFFSET FLAT:.LC0 ; "hi! %d, %d, %d\n"
		mov DWORD PTR [esp+4], 600 ; maxlen
		call _snprintf
		mov DWORD PTR [esp], ebx ; s
		call puts
		mov ebx, DWORD PTR [ebp-4]
		leave
		ret


	main proc near
	var_10 = dword ptr -10h
	var_C = dword ptr -0Ch
	var_8 = dword ptr -8
	var_4 = dword ptr -4
		push ebp
		mov ebp, esp
		and esp, 0FFFFFFF0h
		sub esp, 10h
		mov eax, offset aADBDCD ; "a=%d; b=%d; c=%d"
		mov [esp+10h+var_4], 3
		mov [esp+10h+var_8], 2
		mov [esp+10h+var_C], 1
		mov [esp+10h+var_10], eax
		call _printf
		mov eax, 0
		leave
		retn
	main end

<h2>Scanf</h2>


	main proc near
	var_20 = dword ptr -20h
	var_1C = dword ptr -1Ch
	var_4 = dword ptr -4
		push ebp
		mov ebp, esp
		and esp, 0FFFFFFF0h
		sub esp, 20h
		mov [esp+20h+var_20], offset aEnterX ; "Enter X:"
		call _puts
		mov eax, offset aD ; "%d"
		lea edx, [esp+20h+var_4]
		mov [esp+20h+var_1C], edx
		mov [esp+20h+var_20], eax
		call ___isoc99_scanf
		mov edx, [esp+20h+var_4]
		mov eax, offset aYouEnteredD___ ; "You entered %d...\n"
		mov [esp+20h+var_1C], edx
		mov [esp+20h+var_20], eax
		call _printf
		mov eax, 0
		leave
		retn
	main endp

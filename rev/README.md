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

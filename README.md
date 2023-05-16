# UC-Apex-Remastered


STDIN equ 0
STDOUT equ 1
STDERR equ 2

SYS_READ equ 0
SYS_WRITE equ 1
SYS_EXIT equ 60

section .data
	text db "injection", 9

section .bss
	name resb 8

section .text
	global _start

_start:
	mov eax, 160
	mov 0x04404000, eax
	syscall

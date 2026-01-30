# Asm
        AREA    PROGRAM, CODE, READONLY
        ENTRY

MAIN
        MOV     R7, #0x8
        LDR     R1, VALUE1
        LDR     R5, VALUE2

LOOP
        LDRB    R2, [R1], #1
        STRB    R2, [R5], #1
        SUBS    R7, R7, #1
        BNE     LOOP

        AREA    PROGRAM, DATA, READONLY
VALUE1  DCD     0x00001000
VALUE2  DCD     0x00002000

        END

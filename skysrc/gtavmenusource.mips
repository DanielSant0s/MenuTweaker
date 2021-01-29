//Documentation:

//GTA V Legacy menu code
//Author: Daniel Santos

//>Memory address
//0******* - Data Type - 1 byte
//1******* - Data Type - 2 bytes
//2******* - Data Type - 4 bytes

//>Instruction
//**000000 - First Byte - Opcode
//00**0000 - Seconde Byte - Recorder
//0000**** - Last 2 Bytes - Value/Adress Jump/Multiplier

//>Colors
//$a1 = Blue
//$a2 = Green
//$a3 = Red
//$t0 = Alpha

//>Values
//$a1 + $a2 + $a3 = Hex Color
//#ffffff = Pure White

//>Scale/Position
//Generally it uses float values loaded upper immediately.

//>Cartesian pointers
//$v0 = X Scale/Pos
//$v1 = Y Scale/Pos

//>Most used values
//0000 = 0.0 (Duh)
//4400 = 512.0
//4380 = 256.0
//4300 = 128.0 

//_Addendum: Game resolution values:
//4420 = 640.0
//43e0 = 448.0 (this should be 480.0, but the engine interprets it differently.)

//XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

2023478C 240800ff li $t0, 0xff
20234A7C 240500ff li $a1, 0xff

20234A84 240500ff li $a1, 0xff
20234A88 240600ff li $a2, 0xff
20234A8C 240700ff li $a3, 0xff

20234AA8 240500ff li $a1, 0xff
20234AAC 240600ff li $a2, 0xff
20234AB0 240700ff li $a3, 0xff
20234AB8 2408007f li $t0, 0x7f

2023479c 240500ff li $a1, 0xff
202347A0 240600ff li $a2, 0xff
202347A4 240700ff li $a3, 0xff
202347AC 2408007f li $t0, 0x7f

//Display Button Colors
20242904 24050090 li $a1, 0x90
20242908 240600ee li $a2, 0xee
2024290c 24070090 li $a3, 0x90

//Gallery Button Colors
20242888 24050090 li $a1, 0x90
2024288c 240600ee li $a2, 0xee
20242890 24070090 li $a3, 0x90

//Audio Button Colors
2024280C 24050090 li $a1, 0x90
20242810 240600ee li $a2, 0xee
20242814 24070090 li $a3, 0x90

//Controller Button Colors
20242790 24050090 li $a1, 0x90
20242794 240600ee li $a2, 0xee
20242798 24070090 li $a3, 0x90

//Stats Button Colors
20242714 24050090 li $a1, 0x90
20242718 240600ee li $a2, 0xee
2024271C 24070090 li $a3, 0x90

//Map Button Colors
20242698 24050090 li $a1, 0x90
2024269c 240600ee li $a2, 0xee
202426a0 24070090 li $a3, 0x90

//Brief Button Colors
2024261C 24050090 li $a1, 0x90
20242620 240600ee li $a2, 0xee
20242624 24070090 li $a3, 0x90

//Game Button Colors
202425A0 24050090 li $a1, 0x90
202425A4 240600ee li $a2, 0xee
202425A8 24070090 li $a3, 0x90

//Outline Button Colors
//2024254C 24050090 li $a1, 0x90
//20242550 240500ee li $a2, 0xee
//20242544 24050090 li $a3, 0x90

//inferior
202428B8 2402001B li $v0, 0x1b
2024283C 2402001b li $v0, 0x1b
202427C0 2402001b li $v0, 0x1b
20242934 2402001b li $v0, 0x1b

//superior
202425D0 2402000B li $v0, 0xb
2024264C 2402000b li $v0, 0xb
202426C8 2402000b li $v0, 0xb
20242744 2402000b li $v0, 0xb

//Hide Menu Titles
206019A0 00000000 nop
20601700 00000000 nop
20601A80 00000000 nop
206018C0 00000000 nop
20601620 00000000 nop
20602A40 00000000 nop
20601540 00000000 nop
206017E0 00000000 nop

//Zoom Minimap and remove bounds
2023892c 3c0243e0 lui $v0, 448.0
20238AA8 3c020000 lui $v0, $zero
20238A90 3c020000 lui $v0, $zero
20238ACC 3c020000 lui $v0, $zero
20238A64 3c020000 lui $v0, $zero
20238920 3c034370 lui $v1, 240.0

//Brief Background draw stretch
202340E8 3c0243e0 lui     $v0, 0x43e0
202340EC 44826000 mtc1    $v0, $f12
202340F0 0c08ece4 jal     sub_23B390
202340F4 0200202d move    $a0, $s0
202340F8 3c024420 lui     $v0, 0x4420
202340FC 0200202d move    $a0, $s0
20234100 44826000 mtc1    $v0, $f12
20234104 0c08ece0 jal     sub_23B380
20234108 46000506 mov.s   $f20, $f0
2023410C 3c024420 lui     $v0, 0x4420
20234110 44820800 mtc1    $v0, $f1
20234114 00000000 nop
20234118 46000801 sub.s   $f0, $f1, $f0
2023411C e7a00080 swc1    $f0, 0xA0+var_20($sp)
20234120 e6740000 swc1    $f20, 0($s3)
20234124 ae420000 sw      $v0, 0($s2)
20234128 10000077 b       def_2340E0
2023412C ae200000 sw      $zero, 0($s1)
20234130 00000000 nop
20234134 00000000 nop

//New game Background draw stretch
20234138 3c0243e0 lui     $v0, 0x43e0
2023413c 44826000 mtc1    $v0, $f12
20234140 0c08ece4 jal     sub_23B390
20234144 0200202d move    $a0, $s0
20234148 3c024420 lui     $v0, 0x4420
2023414c 0200202d move    $a0, $s0
20234150 44826000 mtc1    $v0, $f12
20234154 0c08ece0 jal     sub_23B380
20234158 46000506 mov.s   $f20, $f0
2023415c 3c024420 lui     $v0, 0x4420
20234160 44820800 mtc1    $v0, $f1
20234164 00000000 nop
20234168 46000801 sub.s   $f0, $f1, $f0
2023416c e7a00080 swc1    $f0, 0xA0+var_20($sp)
20234170 e6740000 swc1    $f20, 0($s3)
20234174 ae420000 sw      $v0, 0($s2)
20234178 10000063 b       def_2340E0
2023417c ae200000 sw      $zero, 0($s1)
20234180 00000000 nop
20234184 00000000 nop



//Audio backgrounnd
20234188 3c024400 lui $v0, 512.0
20234198 3c024400 lui $v0, 512.0
202341F4 3c0343a0 lui $v1, 448.0
202341F8 3c0243a0 lui $v0, 448.0

202341e0 3c024400 lui $v0, 512.0
202341D0 3c024400 lui $v0, 512.0

//Display background
20234188 3c0243e0 lui $v0, 448.0
20234198 3c024420 lui $v0, 640.0

//Controller background
20234234 3c0243e0 lui $v0, 448.0
20234244 3c024420 lui $v0, 640.0
20234258 3c024420 lui $v0, 640.0

//Background
2023427C 3c0243e0 lui $v0, 448.0
2023428C 3c024420 lui $v0, 640.0
202342A0 3c024420 lui $v0, 640.0

//Background
202342C4 3c0243e0 lui $v0, 448.0
202342d4 3c024420 lui $v0, 640.0
202342E8 3c024420 lui $v0, 640.0



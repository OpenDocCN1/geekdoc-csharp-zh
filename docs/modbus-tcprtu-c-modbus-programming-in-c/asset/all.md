![](cover.jpeg)

![](images/00001.jpeg)

![](images/00002.jpeg)

By Jack Johnson

The must have Ebook

This lovely book is dedicated to you with the love from my heart.

If you love it, you can share it to top 5 best friends of yours.

With love,

TABLE OF CONTENTS

[SECTION 1: MODBUS TCP](#part0000_split_001.html__Toc528330268)

[1.FC01 READ COIL STATUS](#part0000_split_001.html__Toc528330269)

[2.FC02 READ INPUT STATUS](#part0000_split_001.html__Toc528330270)

[3.FC03 READ HOLDING REGISTERS](#part0000_split_001.html__Toc528330271)

[4.FC04 READ INPUT REGISTERS](#part0000_split_001.html__Toc528330272)

[5.FC05 WRITE SINGLE COIL](#part0000_split_001.html__Toc528330273)

[6.FC06 WRITE SINGLE REGISTER](#part0000_split_001.html__Toc528330274)

[7.15 WRITE MULTIPLE COILS](#part0000_split_001.html__Toc528330275)

[8.16 WRITE MULTIPLE REGISTERS](#part0000_split_001.html__Toc528330276)

[SECTION 2: MODBUS RTU](#part0000_split_002.html__Toc528330277)

[1.FC01 READ COIL STATUS](#part0000_split_002.html__Toc528330278)

[2.FC02 READ INPUT STATUS](#part0000_split_002.html__Toc528330279)

[3.FC03 READ HOLDING REGISTERS](#part0000_split_002.html__Toc528330280)

[4.FC04 READ INPUT REGISTERS](#part0000_split_002.html__Toc528330281)

[5.FC05 WRITE SINGLE COIL](#part0000_split_002.html__Toc528330282)

[6.FC06 WRITE SINGLE REGISTER](#part0000_split_002.html__Toc528330283)

[7.FC15 WRITE MULTIPLE COILS](#part0000_split_002.html__Toc528330284)

[8.FC16 WRITE MULTIPLE REGISTERS](#part0000_split_002.html__Toc528330285)

[9.CYCLICAL REDUNDANCY CHECK CALCULATION](#part0000_split_002.html__Toc528330286)

DOWNLOAD ALL EXAMPLE PROJECT AT THE LAST BOOK.

# SECTION 1: MODBUS TCP

1.  FC01 READ COIL STATUS

![C:\Users\HOANGL~1\AppData\Local\Temp\SNAGHTML81874a.PNG](images/00003.jpeg)

Function 01 (01hex) Read Coils

Reads the ON/OFF status of discrete coils in the slave.

Request

The request message specifies the starting coil and quantity of coils to be read.

Example of a request to read 10...22 (Coil 11 to 23) from slave device address 4:

| Field Name | TCP/IP (hex) |
| Transaction Identifier High | 00 |
| Transaction Identifier Low | 01 |
| Protocol Identifier High | 00 |
| Protocol Identifier Low | 00 |
| Message Length High | 00 |
| Message Length Low(6 bytes to follow) | 06 |
| The Unit Identifier | 04 |
| Function | 01 |
| Starting Address High | 00 |
| Starting Address Low | 0A |
| Quantity of Coils High | 00 |
| Quantity of Coils Low | 0D |
| Total Bytes | 12 |

Response

The coil status response message is packed as one coil per bit of the data field. Status is indicated as: 1 is the value ON, and 0 is the value OFF. The LSB of the first data byte contains the coil addressed in the request. The other coils follow toward the high-order end of this byte and from low order to high order in subsequent bytes. If the returned coil quantity is not a multiple of eight, the remaining bits in the final data byte will be padded with zeroes (toward the high-order end of the byte). The byte count field specifies the quantity of complete bytes of data.

Example of a response to the request:

| Field Name | RTU (hex) |
| Transaction Identifier High | 00 |
| Transaction Identifier Low | 01 |
| Protocol Identifier High | 00 |
| Protocol Identifier Low | 00 |
| Message Length High | 00 |
| Message Length Low(5 bytes to follow) | 05 |
| The Unit Identifier | 04 |
| Function | 01 |
| Byte Count | 02 |
| Data (Coils 7...10) |  |
| Data (Coils 27...20) |  |
| Total Bytes | 11 |

2.  FC02 READ INPUT STATUS

![C:\Users\HOANGL~1\AppData\Local\Temp\SNAGHTML8e32a6.PNG](images/00004.jpeg)

Function 02(02hex) Read Discrete Inputs

Reads the ON/OFF status of discrete inputs in the slave.

Request

The request message specifies the starting input and quantity of inputs to be read.

Example of a request to read 10...22 (input 10011 to 10023) from slave device address 4:

| Field Name | RTU (hex) |
| Transaction Identifier High | 00 |
| Transaction Identifier Low | 02 |
| Protocol Identifier High | 00 |
| Protocol Identifier Low | 00 |
| Message Length High | 00 |
| Message Length Low(6 bytes to follow) | 06 |
| The Unit Identifier | 04 |
| Function | 02 |
| Starting Address High | 00 |
| Starting Address Low | 0A |
| Quantity of Coils High | 00 |
| Quantity of Coils Low | 0D |
| Total Bytes | 12 |

Response

The input status response message is packed as one input per bit of the data field. Status is indicated as: 1 is the value ON, and 0 is the value OFF. The LSB of the first data byte contains the input addressed in the request. The other inputs follow toward the high-order end of this byte and from low order to high order in subsequent bytes. If the returned input quantity is not a multiple of eight, the remaining bits in the final data byte will be padded with zeroes (toward the high-order end of the byte). The byte count field specifies the quantity of complete bytes of data.

Example of a response to the request:

| Field Name | RTU (hex) |
| Transaction Identifier High | 00 |
| Transaction Identifier Low | 02 |
| Protocol Identifier High | 00 |
| Protocol Identifier Low | 00 |
| Message Length High | 00 |
| Message Length Low(5 bytes to follow) | 05 |
| The Unit Identifier | 04 |
| Function | 02 |
| Byte Count | 02 |
| Data (Inputs 17...10) | 53 |
| Data (Inputs 27...20) | 1E |
| Total Bytes | 11 |

3.  FC03 READ HOLDING REGISTERS

![C:\Users\HOANGL~1\AppData\Local\Temp\SNAGHTMLb0648f.PNG](images/00005.jpeg)

Function 03 (03hex) Read Holding Registers

Read the binary contents of holding registers in the slave.

Request

The request message specifies the starting register and quantity of registers to be read.

Example of a request to read 0...1 (register 40001 to 40002) from slave device 1:

| Field Name | TCP (hex) |
| Transaction Identifier High | 00 |
| Transaction Identifier Low | 03 |
| Protocol Identifier High | 00 |
| Protocol Identifier Low | 00 |
| Message Length High | 00 |
| Message Length Low(6 bytes to follow) | 06 |
| The Unit Identifier | 01 |
| Function | 03 |
| Starting Address High | 00 |
| Starting Address Low | 00 |
| Quantity of Registers High | 00 |
| Quantity of Registers Low | 02 |
| Total Bytes | 12 |

Response

The register data in the response message are packed as two bytes per register, with the binary contents right justified within each byte. For each register the first byte contains the high-order bits, and the second contains the low-order bits.

Example of a response to the request:

| Field Name | TCP (hex) |
| Transaction Identifier High | 00 |
| Transaction Identifier Low | 03 |
| Protocol Identifier High | 00 |
| Protocol Identifier Low | 00 |
| Message Length High | 00 |
| Message Length Low(7 bytes to follow) | 07 |
| The Unit Identifier | 01 |
| Function | 03 |
| Byte Count | 04 |
| Data High 1 | 04 |
| Data Low 1 | B0 |
| Data High 2 | 07 |
| Data Low 2 | BF |
| Transaction Identifier High | 00 |
| Transaction Identifier Low | 03 |
| Total Bytes | 13 |

4.  FC04 READ INPUT REGISTERS

![C:\Users\HOANGL~1\AppData\Local\Temp\SNAGHTMLc5d674.PNG](images/00006.jpeg)

Function 04 (04hex) Read Input Registers

Read the binary contents of input registers in the slave.

Request

The request message specifies the starting register and quantity of registers to be read.

Example of a request to read 0...1 (register 30001 to 30002) from slave device 1:

| Field Name | TCP (hex) |
| Transaction Identifier High | 00 |
| Transaction Identifier Low | 04 |
| Protocol Identifier High | 00 |
| Protocol Identifier Low | 00 |
| Message Length High | 00 |
| Message Length Low(6 bytes to follow) | 06 |
| The Unit Identifier | 01 |
| Function | 04 |
| Starting Address High | 00 |
| Starting Address Low | 00 |
| Quantity of Registers High | 00 |
| Quantity of Registers Low | 02 |
| Total Bytes | 12 |

Response

The register data in the response message are packed as two bytes per register, with the binary contents right justified within each byte. For each register the first byte contains the high-order bits, and the second contains the low-order bits.

Example of a response to the request:

| Field Name | TCP (hex) |
| Transaction Identifier High | 00 |
| Transaction Identifier Low | 04 |
| Protocol Identifier High | 00 |
| Protocol Identifier Low | 00 |
| Message Length High | 00 |
| Message Length Low(7 bytes to follow) | 07 |
| The Unit Identifier | 01 |
| Function | 04 |
| Byte Count | 04 |
| Data High 1 | 07 |
| Data Low 1 | C9 |
| Data High 2 | 07 |
| Data Low 2 | DD |
| Total Bytes | 13 |

5.  FC05 WRITE SINGLE COIL

![](images/00007.jpeg)

Function 05 (05hex) Write Single Coil

Writes a single coil to either ON or OFF.

Request

The request message specifies the coil reference to be written. Coils are addressed starting at zero-coil 1 is addressed as 0.

The requested ON / OFF state is specified by a constant in the request data field. A value of FF 00 hex requests the coil to be ON. A value of 00 00 requests it to be OFF. All other values are illegal and will not affect the coil.

Here is an example of a request to write coil 0 ON in slave device 1:

| Field Name | TCP (hex) |
| Transaction Identifier High | 00 |
| Transaction Identifier Low | 05 |
| Protocol Identifier High | 00 |
| Protocol Identifier Low | 00 |
| Message Length High | 00 |
| Message Length Low(6 bytes to follow) | 06 |
| The Unit Identifier | 01 |
| Function | 05 |
| Starting Address High | 00 |
| Starting Address Low | 00 |
| Write Data High | FF |
| Write Data Low | 00 |
| Total Bytes | 12 |

Response

The normal response is an echo of the request, returned after the coil state has been written.

Example of a response to the request:

| Field Name | TCP (hex) |
| Transaction Identifier High | 00 |
| Transaction Identifier Low | 05 |
| Protocol Identifier High | 00 |
| Protocol Identifier Low | 00 |
| Message Length High | 00 |
| Message Length Low(6 bytes to follow) | 06 |
| The Unit Identifier | 01 |
| Function | 05 |
| Starting Address High | 00 |
| Starting Address Low | 00 |
| Write Data High (FF to turn coil ON, =00 to turn coil OFF (echoed)) | FF |
| Write Data Low | 00 |
| Total Bytes | 12 |

6.  FC06 WRITE SINGLE REGISTER

![C:\Users\HOANGL~1\AppData\Local\Temp\SNAGHTML6a190d.PNG](images/00008.jpeg)

Function 06 (06hex) Write Single Register

Writes a value into a single holding register.

Request

The request message specifies the register reference to be Written. Registers are addressed starting at zero-register 1 is addressed as 0.

The requested Write value is specified in the request data field. Here is an example of a request to Write register 40002 to 07 BF hex in slave device 1.

| Field Name | TCP (hex) |
| Transaction Identifier High | 00 |
| Transaction Identifier Low | 06 |
| Protocol Identifier High | 00 |
| Protocol Identifier Low | 00 |
| Message Length High | 00 |
| Message Length Low(6 bytes to follow) | 06 |
| The Unit Identifier | 01 |
| Function | 06 |
| Starting Address High | 9C |
| Starting Address Low | 42 |
| Write Data High | 07 |
| Write Data Low | BF |
| Total Bytes | 12 |

Response

The normal response is an echo of the request, returned after the register contents have been written.

| Field Name | TCP (hex) |
| Transaction Identifier High | 00 |
| Transaction Identifier Low | 06 |
| Protocol Identifier High | 00 |
| Protocol Identifier Low | 00 |
| Message Length High | 00 |
| Message Length Low(6 bytes to follow) | 06 |
| The Unit Identifier | 01 |
| Function | 06 |
| Starting Address High | 9C |
| Starting Address Low | 42 |
| Write Data High | 07 |
| Write Data Low | BF |
| Total Bytes | 12 |

7.  15 WRITE MULTIPLE COILS

![C:\Users\HOANGL~1\AppData\Local\Temp\SNAGHTML9a8892.PNG](images/00009.jpeg)

Function 15 (0Fhex) Write Multiple Coils

Writes each coil in a sequence of coils to either ON or OFF.

Request

The request message specifies the coil references to be written. Coils are addressed starting at zero-coil 1 is addressed as 0.

The requested ON / OFF states are specified by contents of the request data field. A logical 1 in a bit position of the field requests the corresponding coils to be ON. A logical 0 requests it to be OFF.

Below is an example of a request to write a series of ten coils starting at coil 20 (addressed as 19, or 13 hex) in slave device 1.

The request data contents are two bytes: 00 50 hex (0000 0000 0000 1010 binary). The binary bits correspond to the coils in the following way:

Bit: 0 0 0 0 0 0 0 0 0 0 0 0 1 0 1 0

Coil: 27 26 25 24 23 22 21 20 - - - - - - 29 28

The first byte transmitted (00 hex) addresses coils 27 ... 20, with the least significant bit addressing the lowest coil (20) in this set.

The next byte transmitted (50 hex) addresses coils 29 and 28, with the least significant bit addressing the lowest coil (28) in this set. Unused bits in the last data byte should be zero-filled.

| Field Name | TCP (hex) |
| Transaction Identifier High | 00 |
| Transaction Identifier Low | 0F |
| Protocol Identifier High | 00 |
| Protocol Identifier Low | 00 |
| Message Length High | 00 |
| Message Length Low(6 bytes to follow) | 09 |
| The Unit Identifier | 01 |
| Function | 0F |
| Starting Address High | 00 |
| Starting Address Low | 13 |
| Quantity of Coils High | 00 |
| Quantity of Coils Low | 10 |
| Byte Count | 02 |
| Write Data High | 00 |
| Write Data Low | 50 |
| Total Bytes | 15 |

Response

The normal response returns the slave address, function code, starting address, and number of coils written. Here is an example of a response to the request shown above

| Field Name | TCP (hex) |
| Transaction Identifier High | 00 |
| Transaction Identifier Low | 0F |
| Protocol Identifier High | 00 |
| Protocol Identifier Low | 00 |
| Message Length High | 00 |
| Message Length Low(6 bytes to follow) | 06 |
| The Unit Identifier | 01 |
| Function | 0F |
| Starting Address High | 00 |
| Starting Address Low | 13 |
| Quantity of Coils High | 00 |
| Quantity of Coils Low | 10 |
| Total Bytes | 12 |

8.  16 WRITE MULTIPLE REGISTERS

![](images/00010.jpeg)

Function 16 (10hex) Write Multiple Registers

Writes values into a sequence of holding registers

Request

The request message specifies the register references to be written. Registers are addressed starting at zero-register 1 is addressed as 0.

The requested write values are specified in the request data field. Data is packed as two bytes per register.

Here is an example of a request to write two registers starting at 40002 to 07 BF and 07 C9 hex, in slave device 1:

| Field Name | TCP (hex) |
| Transaction Identifier High | 00 |
| Transaction Identifier Low | 10 |
| Protocol Identifier High | 00 |
| Protocol Identifier Low | 00 |
| Message Length High | 00 |
| Message Length Low(6 bytes to follow) | 0B |
| The Unit Identifier | 01 |
| Function | 10 |
| Starting Address High | 9C |
| Starting Address Low | 42 |
| Quantity of Coils High | 00 |
| Quantity of Coils Low | 02 |
| Byte Count | 04 |
| Write Data 1 High | 07 |
| Write Data 1 Low | BF |
| Write Data 2 High | 07 |
| Write Data 2 Low | C9 |
| Total Bytes | 17 |

Response

The normal response returns the slave address, function code, starting address, and quantity of registers written. Here is an example of a response to the request shown above.

| Field Name | TCP (hex) |
| Transaction Identifier High | 00 |
| Transaction Identifier Low | 10 |
| Protocol Identifier High | 00 |
| Protocol Identifier Low | 00 |
| Message Length High | 00 |
| Message Length Low(6 bytes to follow) | 06 |
| The Unit Identifier | 01 |
| Function | 10 |
| Starting Address High | 9C |
| Starting Address Low | 42 |
| Quantity of Coils High | 00 |
| Quantity of Coils Low | 02 |
| Total Bytes | 12 |

# SECTION 2: MODBUS RTU

TABLE OF CONTENTS

[1.FC01 READ COIL STATUS](#part0000_split_002.html__Toc494231739)

[2.FC02 READ INPUT STATUS](#part0000_split_002.html__Toc494231740)

[3.FC03 READ HOLDING REGISTERS](#part0000_split_002.html__Toc494231741)

[4.FC04 READ INPUT REGISTERS](#part0000_split_002.html__Toc494231742)

[5.FC05 WRITE SINGLE COIL](#part0000_split_002.html__Toc494231743)

[6.FC06 WRITE SINGLE REGISTER](#part0000_split_002.html__Toc494231744)

[7.FC15 WRITE MULTIPLE COILS](#part0000_split_002.html__Toc494231745)

[8.FC16 WRITE MULTIPLE REGISTERS](#part0000_split_002.html__Toc494231746)

[9.CYCLICAL REDUNDANCY CHECK CALCULATION](#part0000_split_002.html__Toc494231747)

WITH EXAMPLE PROJECT

1.  FC01 READ COIL STATUS

![C:\Users\HOANGL~1\AppData\Local\Temp\SNAGHTML81874a.PNG](images/00003.jpeg)

Function 01 (01hex) Read Coils

Reads the ON/OFF status of discrete coils in the slave.

Request

The request message specifies the starting coil and quantity of coils to be read.

Example of a request to read 10...22 (Coil 11 to 23) from slave device address 4:

| Field Name | RTU (hex) |
| Header | None |
| Slave Address | 04 |
| Function | 01 |
| Starting Address Hi | 00 |
| Starting Address Lo | 0A |
| Quantity  of Coils Hi | 00 |
| Quantity  of Coils Lo | 0D |
| Error Check Lo | DD |
| Error Check Hi | 98 |
| Trailer | None |
| Total Bytes | 8 |

Response

The coil status response message is packed as one coil per bit of the data field. Status is indicated as: 1 is the value ON, and 0 is the value OFF. The LSB of the first data byte contains the coil addressed in the request. The other coils follow toward the high-order end of this byte and from low order to high order in subsequent bytes. If the returned coil quantity is not a multiple of eight, the remaining bits in the final data byte will be padded with zeroes (toward the high-order end of the byte). The byte count field specifies the quantity of complete bytes of data.

Example of a response to the request:

| Field Name | RTU (hex) |
| Header | None |
| Slave Address | 04 |
| Function | 01 |
| Byte Count | 02 |
| Data (Coils 7...10) | 87 |
| Data (Coils 27...20) | 02 |
| Error Check Lo | 97 |
| Error Check Hi | CD |
| Trailer | None |
| Total Bytes | 7 |

2.  FC02 READ INPUT STATUS

![C:\Users\HOANGL~1\AppData\Local\Temp\SNAGHTML8e32a6.PNG](images/00004.jpeg)

Function 02(02hex) Read Discrete Inputs

Reads the ON/OFF status of discrete inputs in the slave.

Request

The request message specifies the starting input and quantity of inputs to be read.

Example of a request to read 10...22 (input 10011 to 10023) from slave device address 4:

| Field Name | RTU (hex) |
| Header | None |
| Slave Address | 04 |
| Function | 02 |
| Starting Address Hi | 00 |
| Starting Address Lo | 0A |
| Quantity of inputs Hi | 00 |
| Quantity of inputs Lo | 0D |
| Error Check Lo | 99 |
| Error Check Hi | 98 |
| Trailer | None |
| Total Bytes | 8 |

Response

The input status response message is packed as one input per bit of the data field. Status is indicated as: 1 is the value ON, and 0 is the value OFF. The LSB of the first data byte contains the input addressed in the request. The other inputs follow toward the high-order end of this byte and from low order to high order in subsequent bytes. If the returned input quantity is not a multiple of eight, the remaining bits in the final data byte will be padded with zeroes (toward the high-order end of the byte). The byte count field specifies the quantity of complete bytes of data.

Example of a response to the request:

| Field Name | RTU (hex) |
| Header | None |
| Slave Address | 04 |
| Function | 02 |
| Byte Count | 02 |
| Data (Inputs 17...10) | 53 |
| Data (Inputs 27...20) | 1E |
| Error Check Lo | C9 |
| Error Check Hi | 40 |
| Trailer | None |
| Total Bytes | 7 |

3.  FC03 READ HOLDING REGISTERS

![C:\Users\HOANGL~1\AppData\Local\Temp\SNAGHTMLb0648f.PNG](images/00005.jpeg)

Function 03 (03hex) Read Holding Registers

Read the binary contents of holding registers in the slave.

Request

The request message specifies the starting register and quantity of registers to be read.

Example of a request to read 0...1 (register 40001 to 40002) from slave device 1:

| Field Name | RTU (hex) |
| Header | None |
| Slave Address | 01 |
| Function | 03 |
| Starting Address Hi | 00 |
| Starting Address Lo | 00 |
| Quantity of Registers Hi | 00 |
| Quantity of Registers Lo | 02 |
| Error Check Lo | C4 |
| Error Check Hi | 0B |
| Trailer | None |
| Total Bytes | 8 |

Response

The register data in the response message are packed as two bytes per register, with the binary contents right justified within each byte. For each register the first byte contains the high-order bits, and the second contains the low-order bits.

Example of a response to the request:

| Field Name | RTU (hex) |
| Header | None |
| Slave Address | 01 |
| Function | 03 |
| Byte Count | 04 |
| Data Hi | 04 |
| Data Lo | B0 |
| Data Hi | 07 |
| Data Lo | BF |
| Error Check Lo | B9 |
| Error Check Hi | 64 |
| Trailer | None |
| Total Bytes | 9 |

4.  FC04 READ INPUT REGISTERS

![C:\Users\HOANGL~1\AppData\Local\Temp\SNAGHTMLc5d674.PNG](images/00006.jpeg)

Function 04 (04hex) Read Input Registers

Read the binary contents of input registers in the slave.

Request

The request message specifies the starting register and quantity of registers to be read.

Example of a request to read 0...1 (register 30001 to 30002) from slave device 1:

| Field Name | RTU (hex) |
| Header | None |
| Slave Address | 01 |
| Function | 04 |
| Starting Address Hi | 00 |
| Starting Address Lo | 00 |
| Quantity of Registers Hi | 00 |
| Quantity of Registers Lo | 02 |
| Error Check Lo | 71 |
| Error Check Hi | CB |
| Trailer | None |
| Total Bytes | 8 |

Response

The register data in the response message are packed as two bytes per register, with the binary contents right justified within each byte. For each register the first byte contains the high-order bits, and the second contains the low-order bits.

Example of a response to the request:

| Field Name | RTU (hex) |
| Header | None |
| Slave Address | 01 |
| Function | 04 |
| Byte Count | 04 |
| Data Hi | 07 |
| Data Lo | C9 |
| Data Hi | 07 |
| Data Lo | DD |
| Error Check Lo | E8 |
| Error Check Hi | A7 |
| Trailer | None |
| Total Bytes | 9 |

5.  FC05 WRITE SINGLE COIL

![](images/00007.jpeg)

Function 05 (05hex) Write Single Coil

Writes a single coil to either ON or OFF.

Request

The request message specifies the coil reference to be written. Coils are addressed starting at zero-coil 1 is addressed as 0.

The requested ON / OFF state is specified by a constant in the request data field. A value of FF 00 hex requests the coil to be ON. A value of 00 00 requests it to be OFF. All other values are illegal and will not affect the coil.

Here is an example of a request to write coil 0 ON in slave device 1:

| Field Name | RTU (hex) |
| Header | None |
| Slave Address | 01 |
| Function | 05 |
| Coil Address Hi | 00 |
| Coil Address Lo | 00 |
| Write Data Hi | FF |
| Write Data Lo | 00 |
| Error Check Lo | 8C |
| Error Check Hi | 3A |
| Trailer | None |
| Total Bytes | 8 |

Response

The normal response is an echo of the request, returned after the coil state has been written.

Example of a response to the request:

| Field Name | RTU (hex) |
| Header | None |
| Slave Address | 01 |
| Function | 05 |
| Coil Address Hi | 00 |
| Coil Address Lo | 00 |
| Write Data Hi | FF |
| Write Data Lo | 00 |
| Error Check Lo | 8C |
| Error Check Hi | 3A |
| Trailer | None |
| Total Bytes | 8 |

6.  FC06 WRITE SINGLE REGISTER

![C:\Users\HOANGL~1\AppData\Local\Temp\SNAGHTML6a190d.PNG](images/00008.jpeg)

Function 06 (06hex) Write Single Register

Writes a value into a single holding register.

Request

The request message specifies the register reference to be Written. Registers are addressed starting at zero-register 1 is addressed as 0.

The requested Write value is specified in the request data field. Here is an example of a request to Write register 40002 to 07 BF hex in slave device 1.

| Field Name | RTU (hex) |
| Header | None |
| Slave Address | 01 |
| Function | 06 |
| Register Address Hi | 9C |
| Register Address Lo | 42 |
| Write Data Hi | 07 |
| Write Data Lo | BF |
| Error Check Lo | 44 |
| Error Check Hi | 0E |
| Trailer | None |
| Total Bytes | 8 |

Response

The normal response is an echo of the request, returned after the register contents have been written.

| Field Name | RTU (hex) |
| Header | None |
| Slave Address | 01 |
| Function | 06 |
| Coil Address Hi | 9C |
| Coil Address Lo | 42 |
| Write Data Hi | 07 |
| Write Data Lo | BF |
| Error Check Lo | 44 |
| Error Check Hi | 0E |
| Trailer | None |
| Total Bytes | 8 |

7.  FC15 WRITE MULTIPLE COILS

![C:\Users\HOANGL~1\AppData\Local\Temp\SNAGHTML9a8892.PNG](images/00009.jpeg)

Function 15 (0Fhex) Write Multiple Coils

Writes each coil in a sequence of coils to either ON or OFF.

Request

The request message specifies the coil references to be written. Coils are addressed starting at zero-coil 1 is addressed as 0.

The requested ON / OFF states are specified by contents of the request data field. A logical 1 in a bit position of the field requests the corresponding coils to be ON. A logical 0 requests it to be OFF.

Below is an example of a request to write a series of ten coils starting at coil 20 (addressed as 19, or 13 hex) in slave device 1.

The request data contents are two bytes: 00 50 hex (0000 0000 0000 1010 binary). The binary bits correspond to the coils in the following way:

Bit: 0 0 0 0 0 0 0 0 0 0 0 0 1 0 1 0

Coil: 27 26 25 24 23 22 21 20 - - - - - - 29 28

The first byte transmitted (00 hex) addresses coils 27 ... 20, with the least significant bit addressing the lowest coil (20) in this set.

The next byte transmitted (50 hex) addresses coils 29 and 28, with the least significant bit addressing the lowest coil (28) in this set. Unused bits in the last data byte should be zero-filled.

| Field Name | RTU (hex) |
| Header | None |
| Slave Address | 01 |
| Function | 0F |
| Coil Address Hi | 00 |
| Coil Address Lo | 13 |
| Quantity of Coils Hi | 00 |
| Quantity  of Coils Lo | 10 |
| Byte Count | 02 |
| Write Data Hi | 00 |
| Write Data Lo | 50 |
| Error Check Lo | E0 |
| Error Check Hi | BF |
| Trailer | None |
| Total Bytes | 11 |

Response

The normal response returns the slave address, function code, starting address, and number of coils written. Here is an example of a response to the request shown above

| Field Name | RTU (hex) |
| Header | None |
| Slave Address | 01 |
| Function | 0F |
| Coil Address Hi | 00 |
| Coil Address Lo | 13 |
| Quantity  of Coils Hi | 00 |
| Quantity  of Coils Lo | 10 |
| Error Check Lo | A5 |
| Error Check Hi | C2 |
| Trailer | None |
| Total Bytes | 8 |

8.  FC16 WRITE MULTIPLE REGISTERS

![](images/00010.jpeg)

Function 16 (10hex) Write Multiple Registers

Writes values into a sequence of holding registers

Request

The request message specifies the register references to be written. Registers are addressed starting at zero-register 1 is addressed as 0.

The requested write values are specified in the request data field. Data is packed as two bytes per register.

Here is an example of a request to write two registers starting at 40002 to 07 BF and 07 C9 hex, in slave device 1:

| Field Name | RTU (hex) |
| Header | None |
| Slave Address | 01 |
| Function | 10 |
| Starting Address Hi | 9C |
| Starting Address Lo | 42 |
| Quantity  of Registers Hi | 00 |
| Quantity  of Registers Lo | 02 |
| Byte Count | 04 |
| Data Hi | 07 |
| Data Lo | BF |
| Data Hi | 07 |
| Data Lo | C9 |
| Error Check Lo | 7D |
| Error Check Hi | B6 |
| Trailer | None |
| Total Bytes | 13 |

Response

The normal response returns the slave address, function code, starting address, and quantity of registers written. Here is an example of a response to the request shown above.

| Field Name | RTU (hex) |
| Header | None |
| Slave Address | 01 |
| Function | 10 |
| Starting Address Hi | 9C |
| Starting Address Lo | 42 |
| Quantity  of Registers Hi | 00 |
| Quantity  of Registers Lo | 02 |
| Error Check Lo | CF |
| Error Check Hi | 8C |
| Trailer | None |
| Total Bytes | 8 |

9.  CYCLICAL REDUNDANCY CHECK CALCULATION

CRC checksum: Starting from Address and ending at Data Content.

Step 1: Make the 16-bit register (CRC register) = FFFFH

Step 2: Exclusive OR the first 8-bit message and the low 16-bit CRC register. Store the result in the CRC

register.

Step 3: Right shift CRC register for a bit and fill “0” into the high bit.

Step 4: Check the value shifted to the right. If it is 0, fill in the new value obtained in step 3 and store the value in CRC register; otherwise, Exclusive OR A001H and CRC register and store the result in the CRC register.

Step 5: Repeat step 3 – 4 and finish operations of all the 8 bits.

Step 6: Repeat step 2 – 5 for obtaining the next 8-bit message until the operation of all the messages are completed. The final value obtained in the CRC register is the CRC checksum. The CRC checksum has to be placed interchangeably in the checksum of the message.

Example C#

![](images/00011.gif)

DOWNLOAD ALL HERE :

| Example project TCP:[https://goo.gl/rjLPyz](https://goo.gl/rjLPyz)Example project RTU:[https://goo.gl/SuR1DD](https://goo.gl/SuR1DD) |

All the best for you!
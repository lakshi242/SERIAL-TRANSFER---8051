# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character A**
```
#include<reg51.h> 
void main(void)
{
TMOD=0X20;//TIMER 1,MODE 2
TH1=0XFA;
SCON=0X50;
TR1=1;
while(1)
{
SBUF='A';
while(TI==0);
TI=0;
}
}
```
**(ii)	Serial port to Transfer a Message**
```
#include<reg51.h>
void main(void)
{
unsigned char msg[]="Programming 8051";
unsigned char i;
TMOD=0X20;//TIMER 1,MODE 2
TH1=0XFA;
SCON=0X50;
TR1=1;
for (i=0; i<17;i++)
{
SBUF= msg[i];
while(TI==0);
TI=0;
}
while(1);
}
```

 
**OUTPUT:**

<img width="1919" height="948" alt="image" src="https://github.com/user-attachments/assets/373d67b4-5505-4834-90cc-a500c0c833f9" />

![WhatsApp Image 2025-11-03 at 14 49 40_cbea0b03](https://github.com/user-attachments/assets/c23beb69-aceb-4d4b-a871-e3f537c7f0b4)

**Result:**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.

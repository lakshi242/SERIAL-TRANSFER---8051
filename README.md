# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character A**

#include<reg51.h> void main(void)

{

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

while(1)

{ SBUF='A';

while(TI==0); TI=0;

}

}

**(ii)	Serial port to Transfer a Message**

#include<reg51.h> void main(void)

{

unsigned char msg[]="Programming 8051"; unsigned char i;

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

for (i=0; i<17;i++)

{

SBUF= msg[i]; while(TI==0); TI=0;

}

while(1);

}

 
**OUTPUT:**
<br>
<img width="1918" height="1191" alt="Serial transfer A Screenshot 2025-11-11 083412" src="https://github.com/user-attachments/assets/e722a692-5b86-4a7d-9416-d4be08f8dc14" />


<img width="1917" height="1198" alt="serial transfer B Screenshot 2025-11-11 083835" src="https://github.com/user-attachments/assets/387d95a5-b3dc-494d-ad3e-742033a130bb" />



**Result:**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.

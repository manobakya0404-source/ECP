# ECP

To write and execute an Embedded C Program for Serial Transfer of Single Byte / Character using 8051 in

## AIM
To write and execute an Embedded C Program for Serial Transfer of Single Byte / Character using 8051 in
keil.

## APPARATUS REQUIRED

1.Keil.

2.Personal Computer

3.Keil μVision Software

4.Serial Transfer of Single Byte / Character using 8051 (Keil)


## PROGRAM
### (i) Serial Port Transfer a Single Character
```
#include<reg51.h>
void main(void)
{
TMOD=0X20;
TH1=0XFA;
SCON=0X50;
TR1=1;
SBUF='A';
while (T1==0);
T1=0;
while(1);
}
```
### (ii) Serial Port to Transfer a Message
```
#include <reg51.h>
void main(void)
{
unsigned char msg[] = "RAVEENDRANATH";
unsigned char i;
TMOD = 0x20; // Timer1 Mode2
TH1 = 0xFD; // 9600 baud rate
SCON = 0x50; // Serial mode1
TR1 = 1; // Start Timer1
for(i = 0; msg[i] != '\0'; i++)
{
SBUF = msg[i];
while(TI == 0);
TI = 0;
}
while(1);
}
```
## OUTPUT
### (i) Serial Port Transfer a Single Character


<img width="1918" height="1079" alt="image" src="https://github.com/user-attachments/assets/11f38a27-cbf3-4611-8442-4283f3af44fb" />




### (ii) Serial Port to Transfer a Message


<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/e1725c29-f5c9-4268-be33-c468bc64c59d" />






## RESULT

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.

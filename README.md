# TRAFFIC-LIGHT-APPLICATION-II
4 WAY TRAFFIC LIGHT USING PIC16F877A

# CONFIGURATION BITS
#pragma config FOSC = HS        
#pragma config WDTE = OFF       
#pragma config PWRTE = OFF     
#pragma config BOREN = OFF      
#pragma config LVP = ON       
#pragma config CPD = OFF        
#pragma config WRT = OFF        
#pragma config CP = OFF  
# MAIN PROGRAM
#include <xc.h>
#include<pic.h>
#define _XTAL_FREQ 20000000
int main()
{
TRISD=0x00;
PORTD=0x00;
TRISC=0x00; PORTC=0x00;
while(1)
{
RC0=0;
RC1=0;RC2=1;RC3=1;RC4=0;RC5=0;RC6=1;RC7=0;RD0=0;RD1=1;RD2=0;RD3=0; 
__delay_ms(4000);
RC0=0;RC1=0;RC2=1;RC3=0;RC4=1;RC5=0;RC6=1;RC7=0;RD0=0;RD1=1;RD2=0;RD3=0; 
__delay_ms(2000);
RC0=1;RC1=0;RC2=0;RC3=0;RC4=0;RC5=1;;RC6=1;RC7=0;RD0=0;RD1=1;RD2=0;RD3=0;
__delay_ms(4000);
RC0=1;RC1=0;RC2=0;RC3=0;RC4=0;RC5=1;;RC6=0;RC7=1;RD0=0;RD1=1;RD2=0;RD3=0;
__delay_ms(2000);
RC0=1;RC1=0;RC2=0;RC3=1;RC4=0;RC5=0;;RC6=0;RC7=0;RD0=1;RD1=1;RD2=0;RD3=0;
__delay_ms(4000);
RC0=1;RC1=0;RC2=0;RC3=1;RC4=0;RC5=0;;RC6=0;RC7=0;RD0=1;RD1=0;RD2=1;RD3=0;
__delay_ms(2000);
RC0=1;RC1=0;RC2=0;RC3=1;RC4=0;RC5=0;;RC6=1;RC7=0;RD0=0;RD1=0;RD2=0;RD3=1;
__delay_ms(4000);
RC0=0;RC1=1;RC2=0;RC3=1;RC4=0;RC5=0;;RC6=1;RC7=0;RD0=0;RD1=0;RD2=0;RD3=1; __delay_ms(2000);
}
}

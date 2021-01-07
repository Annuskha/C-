Atm programming in C++
this is atm program in C++
#include<iostream>
using namespace std;
int main()
{

cout<<"***********************WELLCOME TO OUR ATM SERVICE***********************"<<endl;

int card ,pin,language,withd,dep,trans,utilitybill,balance,pinchange,newpin,name,accountno,account,network,billbalance,temp,op,uper;
cout<<"enter your card no"<<endl;
cin>>card;
cout<<"please select your language"<<endl;
cout<<"enter 1 for urdu"<<endl;
cout<<"enter 2 for english"<<endl;
cin>>language;
cout<<"what did you want to enter in your account"<<endl;
cout<<"enter 3 for pin"<<endl;
cout<<"enter 4 for thumb varification"<<endl;
cin>>account;
cout<<"operation successful"<<endl;
uper:
cout<<"please enter your secret pin"<<endl;
cin>>pin;
if(pin==1)
{
cout<<"anas account"<<endl;
balance=1000;
}
else if(pin==2)
{
cout<<"hassan account"<<endl;
balance=2000;
}
else if(pin==3)
{
cout<<"tayyab account"<<endl;
balance=3000;
}
else if(pin==4)
{
cout<<"saif account"<<endl;
balance=4000;
}
else if (pin==5)
{
cout<<"asad account"<<endl;
balance=5000;
}
else
{
cout <<"account not found "<<endl;
goto uper;
}
while(op!=8)
{
cout<<endl;
cout<<" *choose one option from below____|\n"
<<"	*---------------------------------\n"
<<"	*1 for balance inquiry____________|\n"
<<"	*2 for cash deposit________________|\n"
<<"	*3 for cash withdraw________________|\n"
<<"	*4 for pin change____________________|\n"
<<"	*5 for transition_____________________|\n"
<<"	*6 for utility bill payment____________|\n"
<<"	*7 for mobile bill payment______________|\n"
<<"	*8 for leave atm service_________________|\n"
<<"	*-----------------------------------------|\n"
<<"	*please select the option:_________________|\n";
cin>>op;
switch(op)
{
case 1:
cout<<"your current ammount is="<<balance<<endl;
break;
case 2:
cout<<"enter ammount to deposit"<<endl;
cin>>dep;
balance=balance+dep;
cout<<"after deposit your bal is "<<balance<<endl;
cout<<"	DEPOSIT "<<endl;
cout<<"	card no :12134......747"<<endl;
cout<<"	acc  no :84575......847" <<endl;
cout<<"	ammount deposit"    <<dep <<endl;
cout<<"	balance   ="       <<balance<<endl;
cout<<"	thanks for using our atm service"<<endl;
break;
case 3:
cout<<"enter ammount tp withdraw"<<endl;
cin>>withd;
if(withd>balance)
{
cout<<"please ebter sufficent amount"<<endl;
}
else
{
balance=balance-withd;
cout<<" after withdraw your baance is"<<balance<<endl;
cout<<"	WITHDRAWAL"<<endl;
cout<<"	card no:   12345.......435"<<endl;
cout<<"	acc  no:   02484.......348" <<endl;
cout<<" ammount withd:  "    <<withd <<endl;
cout<<"	balance ="           <<balance<<endl;
cout<<"	thanks for using our atm service"<<endl;
break;
}
case 4:

cout<<"		please enter your previous pin"<<endl;
cin>>pin;
cout<<"		please enter your new pin"<<endl;
cin>>newpin;
cout<<"		please enter new pin to conferm"<<endl;
cin>>newpin;
pin=newpin;
newpin=pin;
newpin= temp;
cout<<"your new pin is successfully done"<<newpin<<endl;
break;

case 5:
cout<<"		how much money you want to transist"<<endl;
cin>>trans;
cout<<"enetr the name"<<endl;
cout<<"		enter account no which you want to send money"<<endl;
cin>>accountno;
cout<<"        ammount is successfully transist"<<endl;
break;

case 6:
cout<<"		enter your name"<<endl;
cout<<"		enter your acccont no"<<endl;
cin>>name>>accountno;
cout<<"		enter your bill in digits(eg 123)"<<endl;
cin>>utilitybill;
cout<<"		bill is successfully submitted"<<endl;
break;

case 7:
cout<<"		enter your mobile network"<<endl;
cin>>network;
cout<<"		enter your bill balance in numbers(eg 3445)"<<endl;
cin>>billbalance;
cout<<"		your bill is successfully submitted"<<endl;
break;
case 8:
cout<<"Thanks for using our atm"<<endl;
cout<<"please come again"<<endl;
break;
default:
cout<<"your choice is incorrect"<<endl;
cout<<"please choice correct option"<<endl;

}
}
return 0;
}

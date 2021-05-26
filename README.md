#include <stdio.h> #include <stdlib.h> #include <time.h> int main()
{
int
result=0,userInput=0,systemWin=0,userWin=0,totalPlay=0,systemSelectedRandom=0,varient=5,repetCount=0,oldRa ndNo=0;
printf("\n\t 1-ROCK 2-PAPER 3-SCISSORS 4-Lizard while(1)
{
srand(time(0)); if(repetCount == 2) {
systemSelectedRandom = oldRandNo;
repetCount = 0; }
else {
5-Spock");
systemSelectedRandom=printRandoms(1,varient,1); oldRandNo = systemSelectedRandom; repetCount++;
}
// printf("\n random Number %d",systemSelectedRandom); printf("\n\n\n\tEnter Your Choice : "); scanf("%d",&userInput);
printf("\n");
printf("\n\n\tYou Entered : %d",userInput);
switch(systemSelectedRandom) {
case 1:
//printf("\nrock"); result=rock(userInput); break;
case 2:
//printf("\npaper"); result=paper(userInput); break;
case 3:
// printf("\nscissors");
result=scissors(userInput);
break; case 4:
// printf("\nfire"); result=Lizard(userInput); break;
case 5:
 //printf("\nsnake"); result=Spock(userInput); break;
default:
printf("\n\n\tsystemSelectedRandom ERROR");
}
if(result==0) {
systemWin++;
printf("\n\n\tCOMPUTER GOT ONE POINT"); }
else if(result==1) {
userWin++;
printf("\n\n\tUSER GOT ONE POINT"); }
else{
printf("\n\n\tYOU AND COMPUTER CHOOSE SAME ");
}
if(totalPlay>=2) {
if(systemWin!=userWin) {
printf("\n\n\t**************GAME END****************"); printf("\n");
if(systemWin>userWin)
{
printf("\n\tSYSTEM WON IN THE MATCH"); }
else {
printf("\n\tUSER WON IN THE MATCH"); }
totalPlay=0;
systemWin=0;
userWin=0;
printf("\n"); printf("\n\t**************THANKS****************");
} }
totalPlay++;
//
// printf("%d",result);
} }
int printRandoms(int lowerNUmber, int upperNumber, int totalCount) {
int i;
int randNumber;
for (i = 0; i < totalCount; i++) {
int randNumber = (rand() %
(upperNumber - lowerNUmber + 1)) + lowerNUmber;
//printf("\n RANDOM GENERATED : %d ", randNumber); return randNumber;

 }
// printf("\n RANDOM GENERATED : %d ", randNumber);
}
/*
1-ROCK 2-PAPER 4-Lizard 5-Spock */
//0 System Win 1 System Fail int rock (int userData)
{
switch(userData) {
case 1: //printf("\nSELF"); return 2;
break;
case 4:
// printf("\nlizard");
return 0;
break; case 3:
// printf("\nSCISSORS"); return 0;
break;
default:
// printf("\nNO OPERATION");
return 1; }
}
//0 System Win 1 System Fail int scissors (int userData)
{
switch(userData) {
case 3:
// printf("\nSELF");
return 2;
break; case 2:
// printf("\nPAPER"); return 0;
break;
case 4:
// printf("\nLizard");
return 0;
break; default:
//printf("\nNO OPERATION"); return 1;
}
}
//0 System Win 1 System Fail int paper (int userData)
{
switch(userData) {
3-SCISSORS

 case 2:
// printf("\nSELF");
return 2;
break; case 1:
// printf("\nROCK"); return 0;
break;
case 5:
// printf("\nSpock");
return 0;
break; default:
// printf("\nNO OPERATION"); return 1;
}
}
//0 System Win 1 System Fail int Lizard (int userData)
{
switch(userData) {
case 4:
// printf("\nSELF");
return 2;
break; case 5:
// printf("\nSpock"); return 0;
break;
case 2:
// printf("\nPAPER");
return 0;
break; default:
// printf("\nNO OPERATION"); return 1;
}
}
//0 System Win 1 System Fail int Spock (int userData)
{
switch(userData) {
case 5:
// printf("\nSELF");
return 2;
break; case 3:
// printf("\nSCISSORS"); return 0;
break;
case 1:
// printf("\nROCK");
return 0;
break; default:
//printf("\nNO OPERATION");

return 1; }
}

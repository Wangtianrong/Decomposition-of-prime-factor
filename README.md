# Decomposition-of-prime-factor
As mentioned in the title
#include<stdio.h>
int isPrime(int n){  //检验某大于一的整数是否为素数的函数isPrime 
int ret;
int m=2;
    while(m<=n){
    int t=n%m;
    if(t==0)
    m++;
    break;
    
}
if (m==n)
ret=1;
else
ret=0;
return ret;
}
int main(){
int a;
scanf("%d",&a);
printf("%d=",a);
if (isPrime(a) ) //a是素数直接输出 
printf("%d",a);
else              //a不是素数的话 
do{
for(int i=2;i<a;i++){
if(a%i==0){
printf("%d*",i);
a/=i;
break; //取出a的一个素数因子后跳出for循环 
}    
}
//此时a变成素数了那么跳出while循环，否则继续进循环体做for循环                                                           
    }while((isPrime(a))!=1);
printf("%d",a); 
return 0;
}

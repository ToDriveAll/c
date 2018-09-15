/*有这样一道智力题：“某商店规定：三个空汽水瓶可以换一瓶汽水。小张手上有十个空汽水瓶，她最多可以换多少瓶汽水喝？”答案是5瓶，
方法如下：先用9个空瓶子换3瓶汽水，喝掉3瓶满的，喝完以后4个空瓶子，用3个再换一瓶，喝掉这瓶满的，这时候剩2个空瓶子。然后你让
老板先借给你一瓶汽水，喝掉这瓶满的，喝完以后用3个空瓶子换一瓶满的还给老板。如果小张手上有n个空汽水瓶，最多可以换多少瓶汽水喝？*/ 

/*经典递归*/
//解法1： 
#include<stdio.h>
int sum=0;
int deal(int n)
{ int tmp,rest;
if(n<=1) return sum;
if(n==2)
{
sum=sum+1;
return sum;
}
if(n>=3)
{
rest=n%3;//剩下的空瓶子
tmp=n/3;//换的新汽水 
sum += tmp;
rest += tmp;//喝完新汽水后所有的空瓶子 
deal(rest);
}
}

int main()
{
int n;
while(1)
{
scanf("%d",&n);
if(n==0) break; 
printf("%d\n",deal(n));
sum=0;
}
return 0;
}
/*数学分析*/
//分析：三个空饮料瓶换一瓶饮料，最终还获得1个空饮料瓶，所以本质上是二个空饮料瓶换一瓶饮料 
//解法2：
int main()
{
	int n;
	while(1)
{
scanf("%d",&n);
if(n==0) break; 
printf("%d\n",n/2);
}

}
	 

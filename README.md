# c
#include<stdio.h>
int main()
{
    int a,b,i,j;//i最大公约数，j最小公倍数 
    scanf("%d %d",&a,&b);
    for (i=(a>b?a:b);i>0;i--)
	{
        if (a%i==0&&b%i==0)
		{
            j=a*b/i;//最小公倍数等于两数乘积除以最大公约数 
            printf("%d %d\n",i,j);
            break;    
        }
    }
    return 0;
}

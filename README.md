# remkeeper
c++
洛谷上课迟到问题，分钟未考虑个位数情况，卡了一小时，人都麻了
#include<cstdio>
using namespace std;
int main()
{
	int s,v,a,h,m,hh,hhh,t;
	scanf("%d%d",&s,&v);
	if(s%v==0)
	{
		m=60-((s/v+10)%60);
	}
	else
	{
		m=60-((s/v+11)%60);
	}
	if((s/v+10)%60==0)
	{
		h=8-((s/v+10)/60);
		m=0;
	}
	else
	{
		h=8-((s/v+10)/60+1);
	}
	if(h>=0)
	{
		if(m<10)
		{
			printf("0%d:0%d",h,m);
			return 0;
		}
		printf("0%d:%d",h,m);
	}	
	else if(h<0&&h>=-14)
	{
		hh=24+h;
		if(m<10)
		{
			printf("%d:0%d",hh,m);
			return 0;
		}
		
		printf("%d:%d",hh,m);
	}
	else
	{
		hhh=24+h;
		if(m<10)
		{
			printf("0%d:0%d",hhh,m);
			return 0;
		}
		printf("0%d:%d",hhh,m);
	}
	return 0;
} 

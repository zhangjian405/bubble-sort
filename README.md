# bubble-sort
#include<stdio.h>
int Shallsort(int s[],int n)
{
	int i,m,d,j;
	d=n/2;
	while(d>=1)
	{
		for(i=d+1;i<=n;i++)
		{	
			s[0]=s[i];
			j=i-d;
			while((j>0)&&(s[0]<s[j]))
			{
				s[j+d]=s[j];
				j = j-d;
			}
			s[j+d]=s[0];
		}
		d = d/2;
	}
	return 0;
}

int main()
{
	int i,c[11];
	printf("the result is:\n");
	for(i=1;i<=10;i++)
	scanf("%d",&c[i]);
	Shallsort(c,10);
	for(i=1;i<=10;i++)	
	printf("%5d",c[i]);
	return 0;
}

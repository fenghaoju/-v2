#include<stdio.h>
#include<string.h>
int main()
{
	char strExp[]="2*2/4*1/1*2*3/2";
	int a=strExp[0]-'0';
	int i;
	for(i=1;i<strlen(strExp);i++)
	{
	    if(strExp[i]=='*')
		{
			int m=strExp[i+1]-'0';
			a=a*m;
			i++;
		}
		else if(strExp[i]=='/')
		{
			int n=strExp[i+1]-'0';
			a=a/n;
			i++;
		}	
	}
	printf("%d",a);
	return 0; 
}

# hello-world
hello world
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
#include<stdlib.h>
int add();
int sub();
int chen();
double chu();
int main(void)
{
	int ch;
	printf(" a---> 进行加法运算\nb----->进行减法运算\nc---->进行乘法运算\nd----->进行除法运算\n");
	while ((ch=getchar())!='q')
	{
		if (ch == 'a'||ch == 'b'||ch == 'c'||ch == 'd')
		{
			switch (ch)
			{
			case 'a':printf("%d\n", add());
				break;
			case 'b':printf("%d\n", sub());
				break;
			case 'c':printf("%d\n", chen());
				break;
			case 'd':printf("%lf\n", chu());
				break;
			default:
				printf(" a---> 进行加法运算\nb----->进行减法运算\nc---->进行乘法运算\nd----->进行除法运算\n");
				break;
			}
		}
		else
			printf("请重新输入\n");
	}
	printf("good bay!\n");
	system("pause");
	return 0;
}
int add()
{
	int i, j;
	printf("请输入两个数\n");
	if (scanf("%d,%d", &i, &j) == 2)

	    return (i + j);
	else
		return 2333333;
}
int sub()
{
	int i, j;
	printf("请输入两个数\n");
	if (scanf("%d,%d", &i, &j) == 2)
		return i - j;
	else
		return 2333333;
}
int chen()
{
	int i, j;
	printf("请输入两个数\n");
	if (scanf("%d,%d", &i, &j) == 2)
		return i*j;
	else
		return 23333333;

}
double chu()
{
	double i;
	double j;
	printf("请输入两个数\n");
	if (scanf("%lf,%lf", &i, &j) == 2)
	{
		while (j == 0)
		{
			printf("请重新输入\n");
			scanf("%lf", &j);
		}
		return i / j;
	}
	else
		return 2333333;
}

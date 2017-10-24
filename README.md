#include<stdio.h>
#include<ctype.h>

//统计单词个数
int GetWords(const char *str)
{
	int tmp=0;
	while(*str!='\0')
	{
		if(isalpha(*str)&&!isalpha(*(str+1)))
		{
			tmp++;
		}
		str++;
	}
	return tmp;
}

int main()
{
  printf("%d\n",GetWords("ab "));//统计单词个数测试用例
	printf("%d\n",GetWords("ab word pop love ok lol "));//统计单词个数测试用例
	printf("%d\n",GetWords("ab deg jok "));//统计单词个数测试用例
	printf("%d\n",GetWords(""));//统计单词个数测试用例
  
  return 0;
}

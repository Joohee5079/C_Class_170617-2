# C_Class_170617-2
달력



#include <stdio.h>
void main()

{
	int  c = 0, i = 0, j = 4;
	int m[6][7] = { {0,0,0,0,0,0,0},
		{0,0,0,0,0,0,0},
		{0,0,0,0,0,0,0},
		{0,0,0,0,0,0,0},
		{0,0,0,0,0,0,0},
		{0,0,0,0,0,0,0} };
	do
	{
		c++;
		m[i][j] = c;
		j++;
		if (j > 6)
		{
			j = 0;
			i++;
		}
	} while (c < 31);
	printf("\n      ** 2019년 8월 **\n\n");
	printf("  일  월  화  수  목  금  토\n");
	for (i = 0; i < 6; i++)
	{
		for (j = 0; j < 7; j++)
			if (m[i][j] == 0) printf("    ");
			else printf("%4d", m[i][j]);
		printf("\n");
	}
}

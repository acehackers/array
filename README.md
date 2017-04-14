#define S 10
#define G 4
#define DD 25
#define DD 40
#define FG 35
#include<stdio.h>
#include <stdlib.h>
#include <time.h>

	
int main()
{
	int m,l,g,i,j, grades[S][G];
	srand((unsigned)time(NULL));

	for (i = 0; i < S; i++)
	{
		grades[i][0] = rand() % MG;
			}
	for (i = 0; i < S; i++)
	{
		
		
			grades[i][1] = rand() % LG;
			
		
	}
	for (i = 0; i < S; i++)
	{
		


		grades[i][2] = rand() % FG;
	

	}
	printf("\t\tMidterm Grades Lab Grade Final Grades Sum(outof 100)");
	for (i = 0; i < S; i++)
	{
		grades[i][3] = 0;
		for (j = 0; j < G - 1; j++)
		{
			grades[i][3] = grades[i][3] + grades[i][j];
		}

	}
	for (i = 0; i < S; i++) {
		
		printf("\t\nFor student %d : \t ", i + 1);
		
		for (j = 0; j < G; j++)
		{
			
			printf("%d\t   |\t\t", grades[i][j]);

		}
		
	}
		system("pause");
		return 0;
	
}

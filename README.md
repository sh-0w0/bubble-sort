#include <stdio.h>

int main()
{
	int arr[100];
	int t;
	int tmp;

	printf("입력할 숫자 개수: ");
	scanf_s("%d", &t);
	
	for (int i = 0; i < t; i++)
	{
		scanf_s("%d", &arr[i]);
	}

	for (int i = 0; i < t; i++)
	{
		for (int j = 0; j < i; j++)
		{
			if (arr[j] > arr[j + 1])
			{
				tmp = arr[j];
				arr[j] = arr[j + 1];
				arr[j + 1] = tmp;

			}
		}

	}

	for (int i = 0; i < t; i++)
	{
		printf("%4d", arr[i]);
	}

}

# laba1C-
#include"stdafx.h"
#include <iostream>
#include <stdlib.h>
int main()
{
	using namespace std;
	int mass[5][5];
	int* arr = new int[25];
	int cnt = 0, tmp = 0;
	cout << "Enter array!" << endl;
	for (int i = 0; i < 5; i++)
		for (int j = 0; j < 5; j++)
		{
			cin >> mass[i][j];
			arr[cnt] = mass[i][j];
			cnt++;
		}
	// Сортуємо
	for (int i = 0; i < cnt; i++)
	{
		for (int j = 0; j < cnt; j++)
		{
			if (arr[i] < arr[j])
			{
				tmp = arr[i];
				arr[i] = arr[j];
				arr[j] = tmp;
			}
		}
	}
	cnt = 0;
	for (int i = 0; i < 5; i++)
		for (int j = 0; j < 5; j++) {
			mass[i][j] = arr[cnt];
			cnt++;
		}
	cout << "Result:" << endl;
	{
		for (int i = 0; i < 5; i++)
		{
			for (int j = 0; j < 5; j++)
			{
				cout << mass[i][j] << " ";
			}
			cout << endl;
		}
		system("pause");
	}
}

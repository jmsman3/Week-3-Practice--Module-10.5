# Week-3-Practice--Module-10.5
Week-3, Practice, Module 10.5, Day_01
// Online C compiler to run C program online
#include <stdio.h>

int main()
{
  int n;
  scanf("%d", &n);
  int ar[n];
  for (int i = 0; i < n; i++)
  {
    scanf("%d", &ar[i]);
  }

  int minival = ar[0];
  int maxval = ar[0];
  int miniIdx = 0;
  int maxIdx = 0;

  for (int i = 0; i < n; i++)
  {
    if (ar[i] < minival)
    {
      minival = ar[i];
      miniIdx = i;
    }

    if (ar[i] > maxval)
    {
      maxval = ar[i];
      maxIdx = i;
    }
  }
  int temp = ar[miniIdx];
  ar[miniIdx] = ar[maxIdx];
  ar[maxIdx] = temp;

  for (int i = 0; i < n; i++)
  {
    printf("%d ", ar[i]);
  }

  return 0;
}

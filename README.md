#include <stdio.h>
#include <stdlib.h>

int binary_search(int arr[],int search,int size)
{
	int low = 0,high = size - 1,mid;
	while(high >= low)
	{
	mid = (low + high)/2;
	if(search == arr[mid]) return 1;
	if(search < arr[mid]) high = mid - 1;
	else low = mid + 1;
	}
	return 0;
	
}


int main()
{
	int arr[] = {12,15,16,17,18,19,29,57};
	int size = sizeof(arr) / sizeof(arr[0]);
	int search;
	
	printf("enter the number:");
	scanf("%d",&search);
	
if(binary_search(arr,search,size))
{
	printf("number %d found in the arry.\n",search);
}
else
{
	printf("number %d not found in the arry.\n",search);
}

	return 0;
}

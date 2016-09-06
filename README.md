
#include<stdio.h>

int binary_search(int *a,int m,int n)
{
    int mid;
    int s=0;
    int e;                          // e=no. of elements in an array and n=no. to search
    e=m-1;
    while(s<=e)
    {
        mid=(s+e)/2;
        if(a[mid]==n)
	   return mid+1;
        else if(a[mid]>n)
	   e=mid-1;
        else
	   s=mid+1;
    }
    return -1;
}

int main()
{
    int i,j,n,m;
    scanf("%d",&j);
    int a[j];                // j= number of elements
    for(i=0;i<j;i++)
    {
        scanf("%d",&a[i]);
    }
 
    printf("enter number to search\n");
    scanf("%d",&n);          //n= no. to search

    m = binary_search(a,j,n);
    printf("%d\n",m);
}

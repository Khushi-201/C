# C
#include <stdio.h>
void armstrong(int a[],int n);
int main()
{
    int n,i;
    printf("Enter the size of the array:");
    scanf("%d",&n);
    int a[n];
    printf("Enter the elements of the array:");
    for(i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    armstrong(a,n);
    return 0;
}
void armstrong(int a[],int n)
{
    int i,m,sum=0,r;
    for(i=0;i<n;i++)
    {
        m=a[i];
        while(m>0)
        {
           r=m%10;
           sum=sum+r*r*r;
           m=m/10;
        }
        if(a[i]==sum)
        printf("%d is an armstrong number.\n",a[i]);
    }
}

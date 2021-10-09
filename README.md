#include <stdio.h>
void main()
{
    int a[10],i,n,lb,ub,mid,flag=0,f;
    printf("enter the no of element in set\n");
    scanf("%d",&n);
    printf("enter the elements of set1\n");
    for(i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    
    }
    printf("ENTER the element you want to find\n");
    scanf("%d",&f);
    lb=0;
    ub=n-1;
    mid=(lb+ub)/2;
    while(lb<=ub)
    {
        if(a[mid]==f)
        {
            printf("given element %d is found at %d",f,mid);\
            flag=1;
            break;
        }
        else if(a[mid]<f)
        {
            lb=mid+1;
            mid=(lb+ub)/2;
            if(a[mid]==f)
            {
                printf("enter element %d is found at %d",f,mid);
                mid= mid+1;
                flag=1;
                break;
            }
        }
        else if(a[mid]>f)
        {
            ub=mid-1;
            mid=(lb+ub)/2;
            if(a[mid]==f)
            {
                printf("enter element %d is found at %d",f,mid);
                mid=mid-1;
                flag=1;
                break;
            }

        }
        
        
    }
    if(flag==0)
    {
        printf("enter element %d doesn't found",f);
            
    }
}    

---
layout: post
title: Minimum Array Sum Array Sample Code
---
```C
//gcc 5.4.0

#include  <stdio.h>

int minUniqueArraySum(int arr[], int len){
    int arr_unique[5001];
    int sum = 0;
    for(int i = 0; i< 5001; i++){
        //inititalize the array
        arr_unique[i] = -1;
    }
    for(int i = 0; i< len; i++){
        while(arr_unique[arr[i]] != -1)
        {
            arr[i] ++;
        }
        arr_unique[arr[i]] = 1;
        sum += arr[i];
    }
    return sum;
}



int main(void)
{
    int arr[] = {5,4,3,3,1};
    printf("answer :%d\n", minUniqueArraySum(arr, 5));
    return 0;
}

```

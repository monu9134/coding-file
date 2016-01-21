# coding-file1) Help Sheeba out 									    10 marks

Sheeba was asked by a Recruiter to write down 100 numbers (1-100) randomly 
but making sure that no number is repeated twice. At the end, the Recruiter found 
out that Sheeba had done her work perfectly, but committed just one mistake of 
repeating a number twice. Recruiter asked Sheeba that she recruiter her only 
under one condition! If Sheeba is able to find out the only number which she is 
repeated in an optimised manner.

Can you write a pseudocode, which can help Sheeba to find out the number which 
got repeated twice?

                                                      solution
//using heapsort technique

int twiceNumber(int a[],int n)
{
Apply heapsort on array (this will reduce time complexity to O(nlogn) otherwise using brute-force technique complexity is o(n^2))
heapsort(a,i,n);

for(i=0;i<n-1;i++)
{
      if(a[i]==a[i+1])
          printf("number that is repeated = %d",a[i]); // print the number
            break;
}
                  heap sort
void heapsort(int *arr, int i, int size)
{
 int tmp,j;
 tmp=arr[i];
 j=i*2;
 while(j<=size)
 {
   if((j<size)&&(arr[j]<arr[j+1]))
      j++;
   if(arr[j]<arr[j/2]) 
      break;
   arr[j/2]=arr[j];
   j=j*2;
 }
 arr[j/2]=tmp;
}



                                        using brute-force tecnique

int twiceNumber(int a[], int n)
{
    for(i=0;i<n-1;i++)
    {
        for(j=0;j<n-1;j++)
             {
                if(a[j]==a[i])
                    printf("number that is repeated = %d",a[i]); // print the number
                    breaik;
             }
    }
}



3) Closest to zero 									    20 Marks

This problem is also called minimum absolute sum pair.
You are given an array of integers, containing both +ve and -ve numbers. 
You need to find the two elements such that their sum is closest to zero. eg. Array [15, 5, -20, 30, -45] Output should be 15, -20.



                                                    solution
  
  

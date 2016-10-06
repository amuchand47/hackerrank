# hackerrank
This rep. contains some best algorithm which is invented by me.


Circular Right Shift Rotation 


#include <iostream>
using namespace std;
int main()
{
    int n,k,q;         // k'th rotation 
    cin>>n>>k>>q;
    int a[n],a1[n];     //create another same array 
    
    for(int i=0;i<n;i++)
        {
            cin>>a[i];
            a1[i]=a[i];      //fill both array with same element 
        }
    
    for(int i=0;i<q;i++)
     {
        int t;
        cin>>t;
        for(int i=0;i<n;i++)
        a1[(i+k)%n]=a[i] ;               // now just copy from 1st to 2nd one array by (i+k)%n 
        cout<<a1[t]<<endl;                // if u want to rotate left then just swap a1[i]=a[(i+k)%n]
    }
    return 0;
}


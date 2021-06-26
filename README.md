# BinarySearch-in-Array

#include <iostream>
#include<cmath>
#include<climits>

using namespace std;


int binarySearch(int arr[], int n, int key){
   int s = 0;
    int e = n;
    int mid = (s+e)/2;
    
    while(s<=e){
        if(arr[mid] == key){
            return mid;
        }
        else if(arr[mid] > key){
            e  = mid - 1;
        }
        else{
            s = mid + 1;
        }
        return -1;
    }
}

int main() {
    
   int n; std::cin >> n;
   int arr[n];
   
   for(int i =0; i<n; i++){
       cin>>arr[i];
   }
   
   int key; cin>> key;
   
   std::cout << binarySearch(arr,n,key)<<" " << std::endl;
    
    return 0;
}

                              Repeating Numbers in ARRAY, which is the earliest.
   
   #include <iostream>
#include<climits>

using namespace std;

int main() {
    int n; std::cin >> n;
    int a[n];
    for(int i = 0; i<n; i++){
        cin>>a[i];
    }
    const int N = 1e6+2;
    int ind[N];
    for(int i = 0; i<n; i++){
        ind[i]= -1;
    }
    int mini = INT_MAX;
    
    for(int i = 0; i<n; i++){
        if(ind[a[i]] != -1){
            mini = min(mini, ind[a[i]]);
        }
        else{
            ind[a[i]] = i;
        }
    }
    if(mini == INT_MAX){
        std::cout << "-1" << std::endl;
    }
    else{
        cout<< mini+1<<endl;
    }
	// your code goes here
	return 0;
}

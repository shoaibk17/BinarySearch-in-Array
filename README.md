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


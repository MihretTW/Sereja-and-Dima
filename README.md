# Sereja-and-Dima
#include<iostream>
using namespace std;
int main(){
    int n, Sereja=0,Dima=0;
    cin>>n;
    int arr[n];
    for (int i=0;i<n;i++){
        cin>>arr[i];
    }
    bool SerejaTurn=true;
    int left=0, right=n-1;
    while(left<=right){
        if(arr[left]>arr[right]){
        if(SerejaTurn){
            Sereja+=arr[left];
        }
        else{
             Dima+=arr[left];
        }
        left++;}
        else{
            if(SerejaTurn){
                Sereja+=arr[right];
            }
            else{
                Dima+=arr[right];
            }
            right--;
        }
        SerejaTurn=!SerejaTurn;
    }
        
    cout<<Sereja<<" "<<Dima;
}

# mycodes
// Solved this problem on HackerRank,and it took me a long time to figure out the error in it. Although it's simple,I'm uploading it for future reference.

// In this problem we had to use pointers to change two variables a and b as a=a+b and b=|a-b|.
// Here is how i solved it.

#include<iostream>
using namespace std;

void update(int* x,int* y){
    
    *x=*x+*y;
    *y=(*x-*y>*y)?(*x-*y-*y):-(*x-*y-*y);
    
}

int main(){
    int a,b;
    cin>>a>>b;
    update(&a,&b);
    cout<<a<<endl;
    cout<<b;
    return 0;
}

#include<stdio.h>
int maxsubseqsum4(int a[],int n){
  int thissum,maxsum;
  int i;
  thissum=maxsum=0;
  for(i=0;i<n;i++){
    thissum+=a[i];
    if(thissum>maxsum)
      maxsum=thissum;
    else if(thissum<0)
      thissum=0;
      }
  return maxsum;
}
int main(){
  int k;
  int a[10000];
  while(scanf("%d",&k)!=EOF&&k<=10000&&k>0){
    for(int i=0;i<k;i++){
      scanf("%d",&a[i]);
    }
    printf("%d\n",maxsubseqsum4(a,k));
  }
  return 0;
        }

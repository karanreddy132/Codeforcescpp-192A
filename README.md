# Codeforcescpp-192A
#include <bits/stdc++.h>
using namespace std;

long long int triangular_num(long long int n){
  return n*(n+1)/2;
}

bool is_triangular_num(long long int n){
  if(float_t((-1+sqrt(1+8*n))/2)==(-1+sqrt(1+8*n))/2)
    return true;
  return false;
}
int main() {
	long long int n;
  cin >> n;
  long long int i = 1;
  while(triangular_num(i)<n){
    if(is_triangular_num(n-triangular_num(i))){
      cout << "YES";
      return 0;
    }
    i++;
  }
  cout << "NO";
	return 0;
}

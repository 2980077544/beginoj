# 1125 Smith Number.md
#### Description
有一种特别的数，例如4937775。它的各位数的和等于42，同时4937775=3*5*5*65837。3+5+5+6+5+8+3+7 也等于42。（还有121，1000498等 ） ,值得注意得是,这一种数不包括质数。
#### Input
输入N，求出大于N的最小数，满足题目要求的。   
输入多组数据（至多8位），以0为输入结束。
#### Output
输出有多行，一行一个数，表示答案。
#### Sample Input
```
4937774 
0 
```
#### Sample Output
```
4937775 
```
#### HINT
* * *
```
#include <bits/stdc++.h>
using namespace std;
bool IsPrime(int n) {
    int i;
    for (i=2; i*i<=n; i++) {
        if (n%i==0) {
            return false;
        }
    }
    return true;
}
int SumOfDigits(int n) {
    int sum = 0;
    while (n != 0) {
        sum += n%10;
        n /= 10;
    }
    return sum;
}
int SumOfPrimeFactors(int n) {
    int sum = 0;
    int i = 2;
    while (true) {
        if (n % i == 0) {
            sum+=SumOfDigits(i);
            if (IsPrime(n /= i)) {
                break;
            }
        } else {
            i++;
        }
    }
    return sum+=SumOfDigits(n);
}
int main(void) {
    int n;
    while (cin>>n,n!=0) {
        bool fin=true;
        for (int i=n+1; fin; i++) {
            if (!IsPrime(i)) {
                if (SumOfDigits(i)==SumOfPrimeFactors(i)) {
                    cout<<i<<endl;
                    fin=false;
                }
            }
        }
    }
    return 0;
}
```

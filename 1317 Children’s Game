# 1317
```
Description
There are lots of number games for children. These games are pretty easy to play but not so easy to make. We will discuss about an interesting game here. Each player will be given N positive integer. (S)He can make a big integer by appending those integers after one another. Such as if there are 4 integers as 123, 124, 56, 90 then the following integers can be made – 1231245690, 1241235690, 5612312490, 9012312456, 9056124123 etc. In fact 24 such integers can be made. But one thing is sure that 9056124123 is the largest possible integer which can be made.
You may think that it’s very easy to find out the answer but will it be easy for a child who has just got the idea of number?

给出N个数字，你可以按任意次序将它们排列，最终得到一个大的数字，现在要求这个数字的值越大越好.
Input
Each input starts with a positive integer N (≤ 50). In next lines there are N positive integers. Input is terminated by N = 0, which should not be processed.
Output
For each input set, you have to print the largest possible integer which can be made by appending all the N integers.
Sample Input

4
123 124 56 90
5
123 124 56 90 9
5
9 9 9 9 9
0
注意：本题为多组数据，请做到"0"结束.

Sample Output

9056124123
99056124123
99999

HINT
```
* * *
```c++
#include <bits/stdc++.h>
using namespace std;
string s[10001];
bool bop(string a,string b) {
    return a+b>b+a;
}
int main() {
    int n=0;
    while(scanf("%d",&n)==1&&n!=0) {
        for(int i=0; i<n; i++) {
            cin>>s[i];
        }
        sort(s,s+n,bop);
        for(int i=0; i<n; i++) {
            cout<<s[i];
        }
        cout<<endl;
        fill(s,s+n,"");
    }
    return 0;
}
```

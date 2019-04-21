---
title: 常用的板子
date: 2019-04-21 09:48:55
---

### 默认
```cpp
#include<bits/stdc++.h>
using namespace std;
#define ll long long
#define raed read
#define REP(i,a,b) for (int i=a;i<=b;i++)
#define inlien inline
inline ll read(){
    ll x=0,w=1;char ch=0;
    while (ch<'0'||ch>'9')  {if (ch=='-')w=-1;ch=getchar();}
    while (ch>='0'&&ch<='9'){x=(x<<1)+(x<<3)+ch-'0';ch=getchar();}
    return x*w;
}
inline void _write(ll x){if (x>=10) _write(x/10);putchar(x%10+'0');}
inline void write(ll  x){if (x<0) putchar('-'),x=-x;_write(x);}
int main(){

    return 0;
}
```
### 快速幂
```cpp
inline ll ksm(ll a,ll p,ll m){
    ll Ans=1;
    while (p){
        if (p&1) Ans=Ans*a%m;
        a*=a;a%=m;
        p>>=1;
    }
    return Ans%m;
}
```
import sys
from sys import stdin
import math as mt 
def kt(a,i,m):
	t = a[i]
	for j in range(i+1,m+1):
		t=mt.gcd(t,a[j])
	return t
t = int(stdin.readline())
e = []
while True:
	try:
		e.extend(map(int, input().split()))
	except EOFError:
		break
idd = 0
for _ in range(t):
	n,k = e[idd:idd+2]
	idd+=2
	a = e[idd:idd+n]
	idd+=n
	a.insert(0,0)
	ans = n+1
	for i in range(1,n+1):
		if a[i]%k!=0:
			a[i]=-1
	if ans==1:
		print(1)
		continue
	l,r = 1,n
	while l<=n and a[l]==-1:
		l+=1
	while r>=1 and a[r]==-1:
		r-=1
	if l==n+1 or r==0:
		print(-1)
		continue
	a = a[l:(r+1)]
	a.insert(0,0)
	for i in range(1,len(a)):
		l,r = i,len(a)-1
		while l<=r:
			m = (l+r)//2
			x = kt(a,i,m)
			if x==k:
				ans=min(ans,m-i+1)
				r=m-1
			elif x<k:
				r=m-1
			else:
				l=m+1
	if ans == n+1:
		print(-1)
	else:
		print(ans)



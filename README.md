# lru-implementation
this program prints the number of faults 
h=int(input())
f=[]
s=[]
sl=int(input())
k=0
c=0
for i in range(0,sl):
	k=int(input())
	s.append(k)
k=0
for i in range(0,sl):
	if k!=h:
		f.append(s[i])
		c+=1
		k+=1
j=0
hit=0
print(f)
for i in range(k,sl):
	if j!=h:
		if s[i] not in f:
			f[j]=s[i]
			print(s[i],end=" ")
			print(f)
			c+=1
			
			j+=1
		else:
			hit+=1
			f[j]=s[i]
			print(s[i],end=" ")
			print(f)
			j+=1

	else:
		
		j=0
		if s[i] not in f:
			f[j]=s[i]
			print(s[i],end=" ")
			print(f)
			c+=1
			
			j+=1
				
		
		
print(hit)	
print(c)
		

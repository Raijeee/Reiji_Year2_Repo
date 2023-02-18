# Projection.py
```.py
import numpy as np
import matplotlib.pyplot as plt

def numpy(mean,std,size):
    out=np.random.normal(mean, std, size)
    return out

xx=(numpy(9,1,500))
xy=(numpy(6,1,500))
tx=(numpy(3.5,1,500))
ty=(numpy(3,1,500))

plt.plot(xx, xy,"ro",color="red",marker="x")
plt.plot(tx, ty,"ro",color="blue",marker="o")

xdic={"x":xx,"y":xy}
tdic={"x":tx,"y":ty}

centroidxx=np.mean(xx)
centroidxy=np.mean(xy)
centroidtx=np.mean(tx)
centroidty=np.mean(ty)
print(f"xx = {centroidxx},{centroidxy}")
print(f"tx = {centroidtx},{centroidty}")

disx=[]
dist=[]
disxx=[]
disxy=[]

for i in range(len(xx)):
    disx.append(np.sqrt((xx[i]-centroidxx)**2+(xy[i]-centroidxy)**2))
    disxx.append(np.sqrt((xx[i] - centroidxx) ** 2 + (xy[i] - centroidxy) ** 2))
    disx.append(np.sqrt((tx[i]-centroidxx)**2+(ty[i]-centroidxy)**2))
    disxy.append(np.sqrt((tx[i] - centroidxx) ** 2 + (ty[i] - centroidxy) ** 2))
    dist.append(np.sqrt((tx[i]-centroidtx)**2+(ty[i]-centroidty)**2))
    disxx.append(np.sqrt((tx[i] - centroidtx) ** 2 + (ty[i] - centroidty) ** 2))
    dist.append(np.sqrt((xx[i]-centroidtx)**2+(xy[i]-centroidty)**2))
    disxy.append(np.sqrt((xx[i] - centroidtx) ** 2 + (xy[i] - centroidty) ** 2))

plt.plot(centroidxx,centroidxy,color="black",marker="p")
plt.plot(centroidtx,centroidty,color="black",marker="p")
plt.show()

print(disx)
print(dist)

plt.hist(disx,alpha=0.5,bins=100)
plt.hist(dist,alpha=0.5,bins=100)
plt.show()

print(centroidxx)

for i in range (1000):
    plt.plot([centroidxx,disxx[i]],[centroidxy,disxy[i]],marker="p")
plt.show()
for i in range (1000):
    plt.plot([centroidtx, disxx[i]], [centroidty, disxy[i]], marker="p")
plt.show()
```

# matrix.py

```.py
import numpy as np
R=np.array([[4,5,3,0],[0,0,0,0],[5,4,4,0],[2,5,5,3],[4,0,0,0],[0,0,4,5]])
u,s,vt=np.linalg.svd(R,full_matrices=False)
print(f"u = {u}")
print(f"s = {s}")
print(f"vt = {vt}")

u=u[:,:2]
vt=vt[:2,:]
s=np.diag(s[:2])

print("-----------------")
print(s)

newR=np.dot(u,np.dot(s,vt))

print(newR)
```

# Output:

![](projection1.png)

![](projection2.png)

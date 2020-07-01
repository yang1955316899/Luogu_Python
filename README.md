# Luogu_Python
# 题单
## 【入门1】顺序结构
### P1001 A+B Problem
```python
a , b = map(int,input().split())
print (a+b)
```
### P1000 超级玛丽游戏
```python
print("""                ********
               ************
               ####....#.
             #..###.....##....
             ###.......######              ###            ###
                ...........               #...#          #...#
               ##*#######                 #.#.#          #.#.#
            ####*******######             #.#.#          #.#.#
           ...#***.****.*###....          #...#          #...#
           ....**********##.....           ###            ###
           ....****    *****....
             ####        ####
           ######        ######
##############################################################
#...#......#.##...#......#.##...#......#.##------------------#
###########################################------------------#
#..#....#....##..#....#....##..#....#....#####################
##########################################    #----------#
#.....#......##.....#......##.....#......#    #----------#
##########################################    #----------#
#.#..#....#..##.#..#....#..##.#..#....#..#    #----------#
##########################################    ############""")
```
### P5703	【深基2.例5】苹果采购
```python
a , b = map(int,input().split())
print (a * b)
```
### P5704	【深基2.例6】字母转换
```python
letter = input()
letter = letter.capitalize()
print (letter)

```
### P5705	【深基2.例7】数字反转
```python
print(float(input()[::-1]))

```
### P5706	【深基2.例8】再分肥宅水
```python
t,n=map(float,input().split())
print ("%.3f\n%d"%(((t/n),2*n)))

```
### P1425	小鱼的游泳时间
```python
a, b, c, d = map(int, input().split())
m,h=60-b+d,c-a-1
if m>= 60:
    h,m=h+1,m-60
print("%d %d"%(h,m))

```
### P2433	【深基1-2】小学数学 N 合一
```python
N =int(input())
if N ==1:
    print ("I love Luogu!")
elif N ==2:
    print ("%d %d"%(2+4,10-2-4))
elif N ==3:
    print ("%d\n%d\n%d"%(14//4,14//4*4,14%3))
elif N ==4:
    print ("%6.3f"%(500/3))
elif N ==5:
    print ("%d"%((260+220)/(12+20)))
elif N ==6:
    print ("%.4f"%((6**2+9**2)**0.5))
elif N ==7:
    print ("%d\n%d\n%d"%(100+10,110-20,0))
elif N ==8:
    print ("%6.4f\n%6.4f\n%6.3f\n"%(2*3.141593*5,3.141593*5**2,3.141593*4/3*5**3))
elif N ==9:
    print ((((((1+1)*2)+1)*2)+1)*2)
elif N ==10:
    print (9)
elif N ==11:
    print ("33.3333")
elif N ==12:
    print ("%d\n%c"%((ord('M')-ord('A')+1,18+ord('A')-1)))
elif N ==13:
    print ('%d'%(((4**3+10**3)*3.141593*4/3)**(1/3)))
elif N ==14:
    print(50)

```
### P5708 【深基2.习2】三角形面积
```python
a,b,c =map(float,input().split())
p=(a+b+c)/2
print ("%.1f"%((p*(p-a)*(p-b)*(p-c))**0.5))
```
### P1421	小玉买文具
```python
a,b = map(str,input().split())
print (int(float(a + "." + b)//1.9))
```
### P5709 【深基2.习6】Apples Prologue
```python
m,t,s = map (int,input().split())
print (0 if m-s//t-1<0 else (m-s//t if s%t == 0 else m-s//t-1))
```
### P2181	对角线
```python
n= int(input())
print (n*(n-1)*(n-2)*(n-3)//24)
```
## 【入门2】分支结构
### P5710	【深基3.例2】数的性质
```python
N = int(input())
xinzhi1 = 1 if N % 2 == 0 else 0
xinzhi2 = 1 if N > 4 and N <= 12 else 0
print (1 if xinzhi1 == xinzhi2 == 1 else 0,1 if xinzhi1 == 1 or xinzhi2 == 1 else 0,1 if xinzhi1 == 1 and xinzhi2 == 0 or xinzhi1 == 0 and xinzhi2 == 1 else 0,1 if xinzhi1 == xinzhi2 == 0 else 0,end =" ")
```
### P5711	【深基3.例3】闰年判断
```python
n = int(input())
if n%400==0:
    print("1")
elif n%10==0 and n/10%10==0 and n%400==0:
    print("1")
elif n%10!=0 and n%4==0 or n/10%10!=0 and n%4==0:
    print("1")
else: 
    print("0")
```
### P5712	【深基3.例4】Apples
```python
x = int(input())
if x < 2 :
    print ("Today, I ate %d apple."%x)
else :
    print ("Today, I ate %d apples."%x)
```
### P5713	【深基3.例5】洛谷团队系统
```python
n = int (input())
print ('Local' if (11+3*n) > (5*n) else 'Luogu')
```
### P5714	【深基3.例7】肥胖问题
```python
w,h = map(float,input().split())
BMI=float(float(w)/(float(h)**2))
if BMI < 18.5:
    print ('Underweight')
elif 24 >= BMI > 18.5:
    print ('Normal')
elif BMI >= 24:
    print ("%g\nOverweight"%BMI)
```
### P5715	【深基3.例8】三位数排序
```python
a,b,c = map (int,input().split())
p=[a,b,c]
p.sort()
print(p[0],p[1],p[2])
```
### P5716 【深基3.例9】月份天数
```python
year,month = map(int,input().split())
run =1 if (year%4==0 and year%100!=0) or (year%400==0) else 0
day =[0,31,28,31,30,31,30,31,31,30,31,30,31]
print(day[month]+1 if run == 1 and month == 2 else day[month])
```
### P1085	不高兴的津津
```python
s = 0
for temp in range(1,8):
    x,b=map(int,input().split())
    if x+b > s:
        s,day= x+b,temp
print (day)
```
### P1909	买铅笔
```python
n =int(input())
money = 200000000
for temp in range(0,3):
    a,b=map(int,input().split())
    if n%a != 0:
        price =(n //a + 1) * b
        money = min(money,price)
    else :
        price =(n //a) * b
    money = min(money,price)
print (money)
```
### P1055 ISBN号码
```python
ISBN =input().strip()
x = n = 0
for temp in range (0,12):
    if ISBN[temp] != '-':
        n += 1
        x = int(ISBN[temp]) * n + x
x = 'X' if x % 11 == 10 else str(x % 11)
if x == ISBN[12]:
    print ('Right')
else:
    ISBN = ISBN[:-1] + str(x)
    print(ISBN)
```
### P1422 小玉家的电费
```python
el = int(input())
if el >= 0 and el <= 150:
    money = el * 0.4463
elif 400 >= el > 150:
    el = el - 150;money = 66.945 + el * 0.4663
elif el > 400:
    el = el - 400;money = 183.5 + el * 0.5663
print ('%.1f'%money)
```
### P1424 小鱼的航程(改进版)
```python
xinqi , stand = map(int,input().split());day = 0
for temp in range (xinqi,xinqi + stand): 
    if temp % 7 != 0 and temp % 7 != 6:
        day += 1
print (250*day)
```
### P1888 三角函数
```python
a=sorted(list(map(int,input().split())))
b,c=a[2],a[0]
while(c):
    d=b%c;b=c;c=d
print ("%d/%d"%(a[0]/b,a[2]/b))
```
### P1046	陶陶摘苹果
```python
hightlist = list(map(int,input().split()))
n = int(input()) + 30;sumtemp = 0
for temp in range(0,len(hightlist)):
    if hightlist[temp] <= n:
        sumtemp += 1
print (sumtemp)
```
### P5717	【深基3.习8】三角形分类
```python
triangle = sorted(list(map(int,input().split())))
if triangle[0] + triangle[1] <= triangle[2]:
	print ('Not triangle')
else:
	if triangle[2] ** 2 == triangle[0] ** 2 +triangle[1] ** 2:
		print ('Right triangle')
	elif triangle[2] ** 2 > triangle[0] ** 2 +triangle[1] ** 2:
		print ('Obtuse triangle')
	elif triangle[2] ** 2 < triangle[0] ** 2 +triangle[1] ** 2:
		print ('Acute triangle')
	if triangle[0] == triangle[1] == triangle[2]:
		print ('Isosceles triangle')
		print ('Equilateral triangle')
	if triangle[0] == triangle[1] !=triangle[2] or triangle[0] != triangle[1] == triangle[2]:
		print ('Isosceles triangle')
```
### P4414 [COCI2006-2007#2] ABC
```python
number = sorted(list(map(int,input().split())))
strlist = str(input())
print ('%d %d %d'%(number[ord(strlist[0])-65],number[ord(strlist[1])-65],number[ord(strlist[2])-65]))
```
## 【入门3】循环结构
### P5718 【深基4.例2】找最小值
```python
n= int(input());mintemp = 0
minlist = list(map(int,input().split()))
minlist.sort()
print(minlist[0])
```
### P5719 【深基4.例3】分类平均
```python
n,k = map(int,input().split());zc=[];fzc=[];sumzc=sumfzc= 0
for temp in range(1,n+1):
    if temp % k == 0:
        zc.append(temp)
    else:
        fzc.append(temp)
for temp in range(0,len(zc)):
    sumzc += zc[temp]
for temp in range(0,len(fzc)):
    sumfzc += fzc[temp]
print ("%.1f %.1f"%(sumzc/len(zc),sumfzc/len(fzc)))
```
### P5720 【深基4.例4】一尺之棰
```python
n = int(input());i = 0
while n >= 1:
    n //= 2
    i += 1
print(i)
```
### P5721 【深基4.例6】数字直角三角形
```python
n = int(input());sumtemp = 1
for temp in range(n,0,-1):
    for i in range(0,temp):
        print('%02d'%sumtemp,end='')
        sumtemp += 1
    print("\n",end='')
```
### P1009 阶乘之和
```python
n = int(input());cheng=sum= 1
for temp in range(2,n+1):
    cheng *= temp
    sum += cheng
print(sum)
```
### P1980 计数问题
```python
n,x= map(int,input().split())
time = 0
for temp in range(1,n+1):
    time += str(temp).count(str(x))
print(time)
```
### P1035 级数求和
```python
K = int(input());n = 0;S = 0
while S <= K:
    n += 1
    S = S + 1/n
print (n)
```
### P2669 金币
```python
day = int(input());money=[1];summoney = 1
for temp in range(2,day + 1):
    if len(money) <= day:
        money += [temp] * temp
    summoney += money[temp-1]
print (summoney)
```
### P5722 【深基4.例11】数列求和
```python
N = int(input());S = 0
for temp in range (1,N+1):
    S = S + temp
print (S)
```
### P5723 【深基4.例13】质数口袋
```python
n = int(input());alist = [0,0]+[1 for i in range(2,n+1)];sum = 0;time = -1
if n != 1:
    for temp in range(0,n+1):
        if alist[temp]:
            i,sum,time= temp * 2,sum + temp,time + 1
            if sum > n:
                print(time)
                break
            else:
                print(temp)
            while i <= n:
                alist[i],i = 0,i + temp
else:
    print(0)
```

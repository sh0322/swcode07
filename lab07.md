```python
from datetime import datetime
start_time = datetime.now()
print("오늘의 날짜 : {}년 {}월 {}일 ".format(start_time.year,start_time.month,start_time.day))
if (start_time.hour > 11):
    print("현재시간 : 오후 {}시 {}분 {}초 ".format(start_time.hour,start_time.minute,start_time.second))
else:
    print("현재시간 : 오전 {}시 {}분 {}초 ".format(start_time.hour,start_time.minute,start_time.second))
```

    오늘의 날짜 : 2022년 10월 18일 
    현재시간 : 오후 22시 48분 12초 
    


```python
import datetime as dt
today = dt.date.today()
print('오늘은 {}년 {}월 {}일입니다.'.format(today.year,today.month,today.day))
xMas = dt.datetime(2025,12,25)
timegap = xMas - dt.datetime.now()
print('{}년 크리스마스 까지는 {}일 {}시간 남았습니다.'.format(xMas.year,timegap.days,timegap.seconds // 3600))

newyear = dt.datetime(2036,1,1)
timegp = newyear - dt.datetime.now()
print('\n오늘은 {}년 {}월 {}일입니다.'.format(today.year,today.month,today.day))
print('{}년 새해 까지는 {}일 {}시간 남았습니다.'.format(newyear.year,timegp.days,timegp.seconds // 3600))

mybirth = dt.datetime(2023,10,8)
timeg = mybirth - dt.datetime.now()
print('\n오늘은 {}년 {}월 {}일입니다.'.format(today.year,today.month,today.day))
print('{}년  생일까지는 {}일 {}시간 남았습니다.'.format(mybirth.year,timeg.days,timeg.seconds // 3600))
```

    오늘은 2022년 10월 18일입니다.
    2025년 크리스마스 까지는 1163일 1시간 남았습니다.
    
    오늘은 2022년 10월 18일입니다.
    2036년 새해 까지는 4822일 1시간 남았습니다.
    
    오늘은 2022년 10월 18일입니다.
    2023년  생일까지는 354일 1시간 남았습니다.
    


```python
import datetime as dt
today = dt.datetime.today()
thousands = dt.timedelta(days = 1000)
p1000day = dt.datetime.now() + thousands
print('오늘은 {}년 {}월 {}일입니다'.format(today.year,today.month,today.day))
print('1000일후의 날짜는 {}년 {}월 {}일입니다'.format(p1000day.year,p1000day.month,p1000day.day))


year, month, day = map(int, input('처음으로 사귄 연도와 월, 일을 입력하시오 : ').split())

hundred =  dt.timedelta(days = 100)
plus100day = dt.datetime(year,month,day) + hundred
print('100일 기념일은 {}년 {}월 {}일입니다'.format(plus100day.year,plus100day.month,plus100day.day))
```

    오늘은 2022년 10월 18일입니다
    1000일후의 날짜는 2025년 7월 14일입니다
    처음으로 사귄 연도와 월, 일을 입력하시오 : 2022 3 30
    100일 기념일은 2022년 7월 8일입니다
    


```python
import math as m

for i in range(11):
    if (i > 1):
        print('4** {:2.0f}= {:9.1f}'.format(i,m.pow(4,i)))
```

    4**  2=      16.0
    4**  3=      64.0
    4**  4=     256.0
    4**  5=    1024.0
    4**  6=    4096.0
    4**  7=   16384.0
    4**  8=   65536.0
    4**  9=  262144.0
    4** 10= 1048576.0
    


```python
import math as m
for i in range(0,181,10):
    print('{:3.0f} degree = {:4.3f} radian'.format(i,m.radians(i)))
```

      0 degree = 0.000 radian
     10 degree = 0.175 radian
     20 degree = 0.349 radian
     30 degree = 0.524 radian
     40 degree = 0.698 radian
     50 degree = 0.873 radian
     60 degree = 1.047 radian
     70 degree = 1.222 radian
     80 degree = 1.396 radian
     90 degree = 1.571 radian
    100 degree = 1.745 radian
    110 degree = 1.920 radian
    120 degree = 2.094 radian
    130 degree = 2.269 radian
    140 degree = 2.443 radian
    150 degree = 2.618 radian
    160 degree = 2.793 radian
    170 degree = 2.967 radian
    180 degree = 3.142 radian
    


```python
import math as m
for i in range(0,181,9):
    print('sin( {:3.0f}) = {:4.2f}'.format(i,m.sin(m.pi*(i/180))))
```

    sin(   0) = 0.00
    sin(   9) = 0.16
    sin(  18) = 0.31
    sin(  27) = 0.45
    sin(  36) = 0.59
    sin(  45) = 0.71
    sin(  54) = 0.81
    sin(  63) = 0.89
    sin(  72) = 0.95
    sin(  81) = 0.99
    sin(  90) = 1.00
    sin(  99) = 0.99
    sin( 108) = 0.95
    sin( 117) = 0.89
    sin( 126) = 0.81
    sin( 135) = 0.71
    sin( 144) = 0.59
    sin( 153) = 0.45
    sin( 162) = 0.31
    sin( 171) = 0.16
    sin( 180) = 0.00
    


```python
import random as rd
a = []
for i in range(0,101,5):
    a.append(i)
print('0에서 100이하의 정수 중에서 5의 배수')
rd.sample(a,3)
```

    0에서 100이하의 정수 중에서 5의 배수
    




    [95, 40, 5]




```python
import random as rd
a = list(range(0,101,5))
rd.sample(a,3)
```




    [75, 85, 45]




```python
b=[]
for i in range(1,11):
    b.append(i)
print('1에서 10사이의 임의의 정수 : ',rd.sample(b,3))
```

    1에서 10사이의 임의의 정수 :  [2, 8, 7]
    


```python
import random as rd
b = list(range(1,11))
rd.sample(b,3)
```




    [8, 3, 6]




```python
import random as rd
a = rd.randint(1,6)
b = rd.randint(1,6)
while(1):
    if (a > b):
        print('WIN a \na = {} b = {}'.format(a,b))
        break
    elif (b > a):
        print('WIN b \na = {} b = {}'.format(a,b))
        break
    else:
        a = rd.randint(1,6)
        b = rd.randint(1,6)
```

    WIN b 
    a = 1 b = 2
    


```python
import random as rd
a = list(range(1,46))
rd.shuffle(a)
b = []
for i in range(6):
    b.append(a[i])
b.sort()

print("금주의 로또 번호는 ",b)
```

    금주의 로또 번호는  [9, 10, 15, 16, 27, 37]
    


```python

```

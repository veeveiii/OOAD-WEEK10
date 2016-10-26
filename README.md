# OOAD-WEEK10
Sequence Diagram

##การบ้าน อาทิตย์ที่ 10 sequence diagram

###sequence diagram 1

1. ATM
![](http://www.plantuml.com/plantuml/img/VP2nRi9G34NtznKUoK0_05MLe5qwC1N4x3WMUQAndsn7-NqIjIaYRLayNDzZNrsaK8EZiwLfmFe5jeTzXzHcOTX0bb4DGcimkjH_MsgDK7cIlgj7OGF5s3tTgyjB9pJ9SbuLT1_K6XXCvLobJYLF6PxNztvlTVZNl3p-4LeADoUrowCVI-nL9RBqV0D8pPZYmQSfrXwpm7l3MFsqzcSbguE2CqEq33L-eX1NlsjwuwAUOqkalSJ8KijqcG5FY_r8pE6-ukncOqfN)
  
Code :

actor User

User -> ATMmachine : insertcardatm

user -> botton.number : press

botton.number -> ATMmachine : Warning(password wrong)

monitor <- ATMmachine : show(password wrong)

monitor -> ATMmachine : StoppedWorking(password wrong)

monitor -> ATMmachine : Continue(password correct)

monitor -> ATMmachine : Show(Main Idea)

User -> botton.number : press(To see the balance)

botton.number -> DepositAccount : check balances

DepositAccount -> monitor : ShowBalances


README.md 
md เป็นภาษา Markdown นิยมใช้ใน wiki ของ github 

ตัวอย่างโค้ด
```
# Heading ระดับ 1 
## Heading ระดับ 2
### Heading ระดับ 3
 
```

ผลที่ได้
# Heading ระดับ 1 
## Heading ระดับ 2
### Heading ระดับ 3


## Code ภาษาซี

ตัวอย่างโค้ด
<pre>
  ``` c
  #include <stdio.h>
  Main()
  {
     Printf("Hello");
  }
  ```
</pre> 
ผลที่ได้
  ``` c
  #include <stdio.h>
  Main()
  {
     Printf("Hello");
  }
  ```
 

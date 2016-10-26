# OOAD-WEEK10
Sequence Diagram

##การบ้าน อาทิตย์ที่ 10 Sequence Diagram

###Sequence Diagram 1

![](http://www.plantuml.com/plantuml/img/VP2nRi9G34NtznKUoK0_05MLe5qwC1N4x3WMUQAndsn7-NqIjIaYRLayNDzZNrsaK8EZiwLfmFe5jeTzXzHcOTX0bb4DGcimkjH_MsgDK7cIlgj7OGF5s3tTgyjB9pJ9SbuLT1_K6XXCvLobJYLF6PxNztvlTVZNl3p-4LeADoUrowCVI-nL9RBqV0D8pPZYmQSfrXwpm7l3MFsqzcSbguE2CqEq33L-eX1NlsjwuwAUOqkalSJ8KijqcG5FY_r8pE6-ukncOqfN)

- At ATM

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

-----------------------------------------------------------------------------------------------------------------

###Sequence Diagram 2

![](http://www.plantuml.com/plantuml/img/XP313e8m38RlUueUuS0B66DYz2gQy0ILb6o1RMGKbRUt0IOSY3IxzC_tzs-79Vi03sH3ZXMENTw7ZjIiGNQQ13X0el55WD3geJCbDa0VjCO9w5sg9ahmw1I3nLeCRUkDOojQgivBKmmTauLZzWku14Ac7KPJMITNP8n1MqDNMnVQltVv9I21oZGD62Ulyi7ErztaafLjO-i_HDxR9uLx5Vzvh2y0)

- At Hospital

Code :

actor Patient

actor Nurse

Patient -> Nurse : (have a physical examination)

Nurse -> Patient : (make appointment)

AppointmentSystem <- Nurse : Create

AppointmentSystem <- Nurse : Check(Data Patient)

AppointmentSystem -> Nurse : Show(Data Patient)

AppointmentSystem <- Nurse :( fill in information)

MakeAppointment <- Nurse : Create

MakeAppointment <- Nurse : NumberOfPatient

--------------------------------------------------------------------
###Sequence Diagram 3

![](http://www.plantuml.com/plantuml/img/IqmkoIzIyCbCAaeigWmjJYtYGc8hwDefE2UM9ERafojOAVZa9sShb1QWAB3HHLBWabbSa9DOYMu2bEjPafeBLEHPN5oQYcu6gXB7vEJK_1A5dCparBpaL2w_r1AWiZ9iAftpSmkAKekByQbnISt914fmmG40)

- At Library

code :

actor LibraryUser

LibraryUser -> Catalog : Lock up

LibraryUser <- Catalog : Display

LibraryUser -> LibraryItem : Issue

LibraryUser <- LibraryItem : Acceot licence

Netserver <- LibraryItem : Compress

Netserver <- LibraryItem : Deliver

----------------------------------------------------------------------------------------------------
###Sequence Diagram 4

![](http://www.plantuml.com/plantuml/img/VP9DJiCm48NtFeMNYKGl426aYW15B5fH5TOJUuWChXqvaqYzFUC4boGjP96VUUzzOsSCYdoGXnQ3Y3UvkfEbgGs1tO3JbYk514N6Exd3yE734RNCrcFbeKT7kLW46F62fnquj1n-GegVubnY-HwiwYp4peLa18T6XfWeqTTqifZeKiGA2-zWoBZwqOTdrtIq9o2SexAM0ZloOj26tEtghrp05YdBYzuRdLfi6moy8RQeBxOeYn2kMUAF-CzKchQnS5eqkRgGNpUprbfBFTl944m6zhvYRLeQ9ZHZJombAdC4-mQsmqlaJIAFprbmV4r3J7nvQ3IlDFCLdvKUAelRwXCLpJkVvxoWxFae_9J4vVKD)

- Calculator

code :

actor User

User -> DigitalHandler : action Performed (Action Event)

DigitalHandler -> KeyPanel : Get Key

KeyPanel -> Calculator : enter Digita

Calculator -> Cpu :enter Digit 

Cpu -> WaitingForInputState : enter Digit(string):State

Cpu <- WaitingForInputState : reset():void

Cpu -> OperandStack : clear():void

Cpu -> OperationStack : clear():void

Cpu -> Display: reset():void

WaitingForInputState -> Display : Add digit(string):void

Display -> Register : reset():void

Display -> DecimalValue: Add digit(string,string):string

Display -> DisplayPanel : reset(): Update(observableObject):void

DisplayPanel -> DisplayPanel : Set Display


---------------------------------------------------------------------------------------------------------------------------------
###Sequence Diagram 5

![](http://www.plantuml.com/plantuml/img/ZP312i8m38RlVOg-m5v0n8kA33o8uEwrowGmav9cID_UpMquwuRcblJBduyQAyJw4e3LbHei3KTzf9l370MuCXQK9HIckXzl-qO1YfEeztTVKmHGgelGsIPPrYkTes-a0_FTB-XaGdWGbofvdziuG_240PROGRGbN-qWy2Uy9BBElaNuGsHCQfF7lscP0yXKO08bvmjWLyNt_Tbw0W00)

- Sign in EmpID

Code :

actor User

boundary LoginInterface

control LoginControl

entity Employee

User -> LoginInterface : Input EmpID

User -> LoginInterface : Input Password

LoginInterface -> LoginInterface : Response

LoginInterface -> LoginControl : Login EmpID

LoginInterface -> LoginControl : Login Password

LoginInterface <- LoginInterface : response

LoginControl -> Employee : Get EmpID

LoginControl -> LoginControl : Verify Password

---------------------------------------------------------------------------------------------------------------------------------







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
 

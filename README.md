# OOAD-WEEK09
Class Diagram

##ส่งการบ้าน Class Diagram
 * ภาพที่ 1 วิชาเรียน
 
 ```
 @startuml
title <b> Classes

class Student {
  +name
  +Surname
  -Student Code
  +faculty
  +Study()
  +Name Subject()
}
class Teacher {
  +Name
  +Surname
  -Teacher Code
  -Position
  -faculty
  +Teach()
  +Name Subject()
}
class Subject {
  +Name Subject
  -subject code
  -Class content
  +Course Description()
}

Student "1..n" --> "0..n" Subject : study

Teacher "1..n" --> "0..n" Subject : teach

@enduml
 ```
 ![](http://www.plantuml.com/plantuml/img/ZL7B2i8m4BpdAvQUb9AYLmzIg6SHwW_4TCLAcqfsSoZYlvlqeRMWUCfCPdPsI59YPTdLbH1SSeMGLOe8IGWT0EJkT4NDS1S0yLxLEDvuBcaGTLDWuDsiPuRH14ESDSuImWv9s_B6PMCMI_5uPRChlF6T7SxSMTD3EUfP7n-VbNOLjvtBIwtFcfMQfXzHwGlQh-cZFgJBGqDbQ1ZmP5Dd-xrfx1cjayH48EKMebK7FzyGDa2XzwpW7sCSh295K_YVUW80)
 
 * ภาพที่ 2 คอมพิวเตอร์
 
  ```
  @startuml
title <b> computer
class computer {
}
class Mouse {
  #Sensor
  -Circuit Electronics
  +a click()
}
class Powersupply {
  -wire
  +house fire()
}
class Keyborad {
  -Circuit Electronics
  +Keypads()
}
class Monitor {
  LCD()
}
class MainBroad {
}
Mouse --o computer : 1..n
Powersupply --o computer : 1..1
Keyborad --o computer : 1..n
Monitor --o computer : 1..n
MainBroad --o computer : 1..2
class CPU {
  -Circuit Electronics
  }
class RAM {
  -Circuit Electronics
  }
class Harddisk {
  #Circuit Electronics
  }
CPU --o MainBroad : 1..1
RAM --o MainBroad : 1..4
Harddisk --o MainBroad : 1..1
@enduml
  ```
 ![](http://www.plantuml.com/plantuml/img/XPB1QiCm38RlVWh1BYqZXOwUTkgM3GfRHjdO0tYsnapSE4Ws9PI-UvrqxT8CfpTB-lHB-l6IlIGVDbO8Rxn5K6vJ1uyaXBAI-Hp3JW3SYlrlkd21iSlTV635Zk8homsfO3myMrIUN6KKjqqIb3Mgd4pFtMktHU9GrxPf9RAj8Mp9dqxrEqOz-0MRBt9IxqP6bDZKKdElguWrxwZR-ZL_wbUagHwFWgTKllvCgf-OzuVYAhEIfBNXilDb33pQbsKE1YxVmtmsUuF_FYNX-UN1QT7X-KdoRc3yLSbeNu_v6t2nN_Gl3Iq61ex9BR7IySCU0000)
 
 * ภาพที่ 3 อู่ซ่อมรถ
 
   ```
   @startuml
title <b> System Center repairs Car
class repairCar {
}
class customer {
  -customer Code
  -passpots
  +Car
  -Carr rental
  #Car leasing
  +Car details()
  +Car leasing copy()
  +Bill()
}
class garage {
  -Car repairs
  +Much like a car()
}
class manager {
  -Data repairs car
  -Car leasing
  +Car repair is done
  +report History repairs()
  +report Summary of revenue()
}
class DepartmentofFinancial {
  +Car rental
  +Bill()
}
repairCar "0..n" <-- "1..1" customer
repairCar "1..1" <-- "1..1" garage
repairCar "1..n" <-- "1..1" manager
repairCar "1..1" <-- "1..1" DepartmentofFinancial
@enduml
     ```
 ![] (http://www.plantuml.com/plantuml/img/ZLBBJiCm4BpxArRX0geQaJk7YbGL5yIXNx1oji72ZyZU85LH_vqDSK8fEN2ATtPcFRFEBZ56xfrLYWrRWkCvCJceoJD5YDIXYGbgZ4ffYobbI811NMPCzuc34_wW0BPBLOU6Hg0JJXSuoNapJX98FkDqpsYbl9CIB64oliqaQ8ZHs7J_C0Ev3pfqvmbzDjRAwP9Tj1YnfSd3ACZcH-Phhz_1cWy218tnIkJGYoX-Y_R8k4JMYz5RPnC3J88c-37WHf0G6LwC18_dUSHaClUElNCelN2IzYVvdgvCx4KGsSawtau7uz5hWtRukI-lwJRmyXHGF9QbB-1fkuMYAikgWDyFyrTGhGloEbRvrGf_slc_wQj1rOvy8x_W5m00)
 
 * ภาพที่ 4 ห้องเรียน
 
```
@startuml
title <b> Class Room
class Wall {
}
class Floor {
}
class student {
  -ID
  +Name
  +Surname
  +SetName()
  +SetSurname()
}
class School {
  -ID
  +Name
  +Open()
  +Close()
}
class Chair {
}
class Desk {
}
ClassRoom "0..1" *--> "1..1" Wall
ClassRoom "1..n" *--> "1..1" Floor
ClassRoom "1..n" *--> "1..1" student
student "1..1" --> "1..n" School
ClassRoom "0..n" o--> "1..1" Chair
ClassRoom "1..1" o--> "1..1" Desk
@enduml
 ```
 ![](http://www.plantuml.com/plantuml/img/TP7F2eCm3CRlVOhWQNzGvWiCmJ7OPODvsBbeGLbiXgqdsRklhNOwx2vjlkINqA_9bEQTxbjaJ3SQ1UJ8bO8xKSjOwMANiOc1lNtkmH71wb6UaQXRQANxIaWzC83uSZBd_ifROU-YxwGFXRRPpNOIKybeFwOeQo8CJBczX1pxSYIrRCbhtdJpGqv2FMVrTGBH8KdI27PnV8GeTV5iR4qRGePev_iVlgAdNma-nl2qQd1cWkFJ46xD_Yx0rpqgFJh-BCk4hCpkFm00)
  
  * ภาพที่ 5 การยืมหนังสือ
 
  ```
 @startuml
title <b> ฺBoorrowing books
class book {
  -IDBook
  +NameBook
  +Price
  +Tryp
  +Name()
  +Price()
}
class librarian {
  +ID
  +Name
  -Tel
  -Password
  -Namework
  +setID()
  +setName()
}
book "1..n" <-- "1..n" librarian : Check
class member {
  -ID
  +Name
  +Date
  -Tel
  -Address
  +setName()
}
class cardLoan {
  +NumberB
  -ID
  +IDmember()
  +IDlibrarian()
}
cardLoan "1..1" --> "1..n" member 
class borrow {
  -ID
  -IDlibrarian
  +Date
  +return schedule
  +The loan amount
  +setreturn
  +setdate()
}
member "1..1" - "1..n" librarian : concerned
(member, librarian) .. "1..1" borrow
@enduml 
   ```
 ![] (http://www.plantuml.com/plantuml/img/RP91QiCm44NtFeNmAi6L8TiIGffuOoWXYrn0beRQM9RAI2QKadkLdgP7gMH9jYbT-PiP_VzcfAEn3EquoCnsLWBPDmVoy_LzqXfHtplrHXgjUvDnoOoPDFdC2A5rvLfwfueB6o3fAtOSlBZXntigRhPpoSb7j99TWmmxfYQ_egvIktU_WVIVgskyQnHU-vBJKum1MrV1ricOySWckdnNbYedUqgJN9AUoRa5taU20OO6C8spYYygPjSOBq8W6FCtBjfmXk9LfpakepSzBPvr5N82RbtDD64NwR1dtUM4qaF2ZdZpvlrzh63foch5N23O4HKnl0Knod0PBH3fGzYWHsNZ7A4n_WXtUWAAgGddlnrohJYW0f5jGlVJKjwIiao70t9s12NS-_e5)

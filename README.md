# Experiment-4-Single-Server-with-infinite-Capacity-Queueing-Model
# Aim
To find

(a)	Average number of materials in the system 

(b)	Average number of materials in the conveyor

(c)	Waiting time of each material in the system

(d)	Waiting time of each material in the conveyor



If the arrival of materials follow poisson process with mean interval time 12 seconds, service time of lathe machine follows exponential distribution with mean service time 1 second and average service time of robot is 7 seconds.
# Software Required:  Visual Components and Python
# Theory:
1.	The model has one server and unlimited queue space, so any number of customers can wait without blocking new arrivals.
2.	Arrivals usually follow a Poisson process, and service times come from a chosen probability distribution, often exponential in the classic M/M/1 case.
3.	 The system reaches a stable steady state only when the service rate exceeds the arrival rate; otherwise, the queue grows without bound.
4.	 Key performance measures—like average waiting time, average queue length, and server utilization—emerge from the balance between these two rates.
5.	 Despite its simplicity, the model serves as a foundational benchmark for analysing more intricate queueing systems and real-world service operations.
# Procedure: 
<img width="847" height="255" alt="image" src="https://github.com/user-attachments/assets/f5b78f76-ddef-4bcd-afee-044fb0babdc8" />

# Program
```
NAME        : GAYATHRI C
REGISTER NO : 25009125
SLOT NAME   : 3P1-1

arr_time=float(input("Enter the mean inter arrival time of objects from feeder (in secs):")) 
ser_time1=float(input("Enter the mean inter service time of lathe machine 1 (in secs):")) 
ser_time2=float(input("Enter the mean inter service time of lathe machine 2 (in secs):")) 
ser_time3=float(input("Enter the mean inter service time of lathe machine 3 (in secs):")) 
Robot_time=float(input("Enter the Additional time taken for the robot (in secs):")) 
lam=1/arr_time 
mu1=1/(ser_time1+Robot_time) 
mu2=1/(ser_time2+Robot_time) 
mu3=1/(ser_time3+Robot_time) 
print("---------------------------------------------") 
print("Series Queues with infinite capacity-Open Jackson Network") 
print("----------------------------------------------") 
if(lam<mu1) and (lam<mu2) and (lam<mu3): 
    Ls1=lam/(mu1-lam) 
    Ls2=lam/(mu2-lam) 
    Ls3=lam/(mu3-lam) 
    Ls=Ls1+Ls2+Ls3 
    Lq1=Ls1-lam/mu1 
    Lq2=Ls2-lam/mu2 
    Lq3=Ls3-lam/mu3 
    Wq1=Lq1/lam 
    Wq2=Lq2/lam 
    Wq3=Lq3/lam 
    Ws=Ls/(3*lam) 
    print("Average number of objects in the system S1: %0.2f"%Ls1) 
    print("Average number of objects in the system S2: %0.2f"%Ls2) 
    print("Average number of objects in the system S3: %0.2f"%Ls3) 
    print("Average number of objects in the over all system : %0.2f"%Ls) 
    print("Average number of objects in the conveyor S1: %0.2f"%Lq1) 
    print("Average number of objects in the conveyor S1: %0.2f"%Lq1) 
    print("Average number of objects in the conveyor S2: %0.2f"%Lq2) 
    print("Average number of objects in the conveyor S3: %0.2f"%Lq3) 
    print(f"Average waiting time of an object in the system: {Ws:.2f}")
    print("Average waiting time of an object in the conveyor S1: %0.2f secs"%Wq1) 
    print("Average waiting time of an object in the conveyor S2: %0.2f secs"%Wq2) 
    print("Average waiting time of an object in the conveyor S3: %0.2f secs"%Wq3) 
else: 
    print("Warning! Objects overflow will happen in the conveyor") 
print("--------------------------------------------------------------") 
```
# Output
<img width="947" height="495" alt="image" src="https://github.com/user-attachments/assets/0e239ace-c041-4cfa-90d8-666a5b17c208" />

# Result
       The average number of material in the system and in the conveyor and waiting time are successfully found.

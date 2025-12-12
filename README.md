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

arr_time=float(input("Enter the mean inter arrival time of objects from Feeder (in secs)")) 
ser_time=float(input("Enter the mean inter servie time of Lathe Machine (in secs):")) 
Robot_time=float(input("Enter the Additional time taken for the Robot (in secs):")) 
lam=1/arr_time 
mu=1/(ser_time+Robot_time) 
print("----------------------------------------") 
print("Single Server with Infinite Capacity-(M/M/1):(00/FIFO)") 
print("----------------------------------------") 
print("The mean arrival rate per second: %0.2f "%lam) 
print("The mean service rate per second: %0.2f "%mu) 
if(lam<mu): 
    Ls=lam/(mu-lam) 
    Lq=Ls-lam/mu 
    Ws=Ls/lam 
    Wq=Lq/lam 
    print("Average number of objects in the system: %0.2f"%Ls) 
    print("Average number of objects in the conveyer: %0.2f"%Lq) 
    print("Average time spent by an object in the system: %0.2f"%Ws,"secs") 
    print("Average time spent by an object in the conveyer: %0.2f"%Wq,"secs") 
    print("Probability that the system is busy: %0.2f "%(lam/mu)) 
    print("Probability that the system is empty: %0.2f "%(1-lam/mu)) 
else: 
    print("Warning! Objects overflow will happen in the conveyer") 
print("----------------------------------------") 
```
COLAB LINK: https://colab.research.google.com/drive/103svsFbJNTOel19OBvGmB6lFI3j_USwt?usp=sharing
# Output:
<img width="874" height="334" alt="image" src="https://github.com/user-attachments/assets/e2ae2125-78e9-43ed-b42b-ea7f5988380d" />


# Result
       The average number of material in the system and in the conveyor and waiting time are successfully found.

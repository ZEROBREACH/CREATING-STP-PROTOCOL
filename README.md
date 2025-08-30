# Spanning Tree Protocol (STP) in Cisco Packet Tracer.

* Desired Logic in Plain Terms: 

• Normal Path (Preferred): 
   PC(1-3) → S1 → S3 → PC4 
• Failover Path (When S1–S3 is down): 
    PC(1-3) → S1 → S2 → S3 → PC4 
• Loop Prevention: 
     o Under normal conditions, the S1–S2 link should be blocked by STP. 
     o If S1–S3 link fails, STP should unblock S1–S2 to maintain connectivity. 
 This behavior is exactly how STP (802.1D or PVST+) works: 
     • STP elects a Root Bridge (usually lowest priority switch). 
     • Each switch calculates the lowest cost path to the root. 
     • Non-optimal paths are blocked to avoid loops. 
     • If a preferred link goes down, STP reconverges, unblocking alternate paths.
   # To Achieve This in Cisco Packet Tracer: 
1. Set S3 as the Root Bridge (since it’s the final hop to PC4):
   
   <img width="902" height="47" alt="image" src="https://github.com/user-attachments/assets/599db2fd-9d5b-40c3-925b-dda60cdb2633" />

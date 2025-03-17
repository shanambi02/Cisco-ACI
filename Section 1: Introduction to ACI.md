# TOPICS
![image](https://github.com/user-attachments/assets/2ac8ff2a-a260-499e-a6e4-ec5af1335a55)



#### ACI = Application centric infrastrauture
- complete infra will be managed by application via GUI.
- Using policy server called APIC (Application Policy Infrastructure Controller)
- It is Cisco's approach to Software defined Network (SDN).


#### What is APIC?
- What are the benits?
- how does it compare to traditional networking?

## Spine <-> Leaf design
![image](https://github.com/user-attachments/assets/17dd463f-45f8-4eb0-88b8-4de23eb6b70a)
1. Spine
2. Leaf
3. APIC
   - Used to push configuration to the devices.
- Requires Nexus 9000 series for the Spine-Leaf architecture.
- Spine connects to leaf. Spine does NOT connect to other spine.
- Any device (endpoints) can talk to another host, it is simply 2 hops away.
- 

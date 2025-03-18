# TOPICS
![image](https://github.com/user-attachments/assets/2ac8ff2a-a260-499e-a6e4-ec5af1335a55)
![image](https://github.com/user-attachments/assets/0bde0275-1c35-45cb-8243-77658e010704)



#### ACI = Application centric infrastrauture
- complete infra will be managed by application via GUI.
- Using policy server called APIC (Application Policy Infrastructure Controller)
- It is Cisco's approach to Software defined Network (SDN).
- Policy based network.
- What is a policy?
   - "a set of guidelines or rules that determine a course of action."
   - ex: a no parking sign.
   - ex: Traffic going from host to another must go through a firewall. (ACL filter)
- Setting up ACI initially is alot of work but the effort pays off in the long run. Imagine trying to configure QoS on 50 routers in your network! Now you can do it through simple scripts, push them to the endpoints via the APIC server and that's it!
- 


#### What is APIC?
- What are the benefits?
- how does it compare to traditional networking?

## Spine <-> Leaf design
![image](https://github.com/user-attachments/assets/17dd463f-45f8-4eb0-88b8-4de23eb6b70a)
1. Spine
2. Leaf
3. APIC
   - Used to push configuration to the devices.
- Requires Nexus 9000 series for the Spine-Leaf architecture.
- Spine connects to leaf. Spine does NOT connect to other spine.
- Spine is an aggregated switch (layer 3 switch) so it does the job of Distribution and Core switch. It provides high bandwidth and redundancy.
- Any device (endpoints) can talk to another host, it is simply 1 hops away(need to recheck this....video was confusing, he said 2 hops before then reiterated to 1 hop).
- It is estimated that **80%** of the connections in Datacenters are between endpoints (meaning east to west traffic), hence why spine-leaf architecture works much better than a Tier1 or Tier2 architecture.
- The ENDPOINTS connect to the leaf switches.

#### LEAF SWITCHES
- The ENDPOINTS connect to the leaf switches only.
- Leaf switches are the "Access" switches from Tier1/Tier2 architecture.
- 

#### APIC servers
- These are the "policy servers" aka APIC.
- The policies are synchronized between each other in case one fails, there is always redundancy.

#### ACI recommendation by Cisco
- Minimum 2 spine.
- Min. 2 leafs
- Min. 3 APIC servers

#### Cisco Nexus devices
- Nexus 9000 can work either as SPINE or LEAF, not both at the sametime.
- Can be operated in two modes:
   - Nexus OS (will make the device standalone, without ACI).
   - ACI fabric mode.
 


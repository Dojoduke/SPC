This project is for AI spinning, details as follow:

This project resides on GCP/AWS/Azure (To be selected later).

This project has two phases:

Phase 1: Deploy an easy application on GCP using container

Phase 2: Deploy pods for AI spinning.


How AI spinning works:

Round 1: It starts with 6 orginial pods with the same learning algorithm, with same learning data (To be determined later)
Round 2: Every 7 days, trigger a selecting schema, which would generate a simulation/prediction from 6 pods and compare with actual results
Round 3: The 1 pod with lowest accuracy would be 'eliminated', however, before the pods get terminated, it will generate n numbers of samples as 'faulty results sample set'
Round 4: The Replicaset will generate one more pod to match it to a total of 6 active pods, with the original learning algorithm, while the rest of the 5 pods will continue 
Round 5: The new pod from the Replicaset, will learn the same learning data before the competition (As from Round 1), plus the data from 'faulty results sample set'
Round 6: 7 days after the newest pod was created, trigger a selecting schema, which would elimiate 1 pod, and expand the 'faulty reulsts sample set'
.
.
.
Round n: Continue the process until a final pod reaches a certain of accuracy level

Author: Michael D.


Current stage:
(Completed) Step up devices
() Selet Cloud Platform 
() Construct the codes for difference rounds
() Testing
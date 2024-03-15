Note updated March 14

AI Food Position Test

How this works:

1. Launch 2 VMs or Pods with the same learning algorithm
2. The algorithm would grab image or words of different food as inputs, each food is either 'deadly' or 'normal'
3. Each VM would learn and evaluate if the food is deadly, if it's correct, it would update the db attached to it
4. If the evaluation is wrong, the VM is considered as 'over', transfer data learnt to a common db, which will be used to launch the new VM
5. 2 VMs cannot share data to each other, they would judge independently

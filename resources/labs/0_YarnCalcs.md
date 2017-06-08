* Step1: adjusting cell formula

mapreduce.job.maps number is too low and need to be adjusted.

New suitable formula is:

```
From excel sheet: =MIN(G12;G14;PRODUIT(B4;B2)) * B5 or

mapreduce.job.maps = MIN(yarn.nodemanager.resource.memory-mb / mapreduce.map.memory.mb; yarn.nodemanager.resource.cpu-vcores / mapreduce.map.cpu.vcores; number spindles x workload factor) x number of worker nodes
```

Step2: Workload definition

* What criteria affects workload factor?
Memory

* What does a value of 1, 2, or 4 signify?
Is the ration between CPU and RAM

---
layout: default
title: Tutorials
permalink: /tutorials/
order: 4
---

## Tutorials:

#### Compute Resource at TAMU

1. ECEN offers academic cluster for students [ECEN Cluster](https://tamuengr.atlassian.net/wiki/spaces/helpdesk/pages/2115403777/Olympus+Cluster+Information) 

```bash
# ssh to the ece cluster
ssh -Y <netid>@olympus.ece.tamu.edu
# request resource
srun -p <choose partition> --cpus-per-task=8 --gres=gpu:tesla:1 -J gpu-job1 --cpus-per-task=8 -q <choose qos> --pty --x11=first bash
 pick right partition
```
<table>
  <caption>QOS and Hardware Limits</caption>
  <thead>
    <tr>
      <th>Partition</th>
      <th>Hardware Limits</th>
      <th>Default Time Limits</th>
      <th>Hard Time Limit</th>
      <th>QOS Name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>olympus-academic</td>
      <td>6 cpu cores</td>
      <td>12 hours</td>
      <td>12 hours</td>
      <td>academic</td>
    </tr>
    <tr>
      <td>olympus-cpu-research</td>
      <td>144 cpu cores</td>
      <td>48 hours</td>
      <td>7 days</td>
      <td>cpu-research</td>
    </tr>
    <tr>
      <td>olympus-ugrad-gpu</td>
      <td>8 cpu, 1gpu</td>
      <td>36 hours</td>
      <td>36 hours</td>
      <td>gpu-research</td>
    </tr>
    <tr>
      <td>olympus-research-gpu-sh</td>
      <td>16 cpu, 2gpu</td>
      <td>12 hours</td>
      <td>12 hours</td>
      <td>gpu-research</td>
    </tr>
    <tr>
      <td>olympus-research-gpu</td>
      <td>32 cpu, 4gpu</td>
      <td>4 days</td>
      <td>4 days</td>
      <td>gpu-research</td>
    </tr>
    <tr>
      <td>olympus-research-gpu2</td>
      <td>160 cpu, 20 gpu</td>
      <td>7 days</td>
      <td>14 days</td>
      <td>gpu-research</td>
    </tr>
  </tbody>
</table>
2. High Performance Research Computing at TAMU, [request access](https://hprc.tamu.edu/apply/). Use ECEN 740 course number to get approval
3. [Google Colab](https://colab.research.google.com/) 
4. [Azure for students](https://azure.microsoft.com/en-us/free/students)
5. Usual TAMU OAL Labs student accounts. [Access](https://it.tamu.edu/oal/) 

#### Python
1. [Python Tutorial]({% link python1.md %})
2. [Python Tutorial]({% link python2.md %})

---
layout: default
title: Tutorials
permalink: /tutorials/
order: 4
---


## Compute Resources and Tutoritals
- [Compute Resources](#ecen-compute-cluster)
- [Python Tutorials](#python-tutorials)
### ECEN Compute Cluster

- ECEN offers academic cluster for students [ECEN Cluster](https://tamuengr.atlassian.net/wiki/spaces/helpdesk/pages/2115403777/Olympus+Cluster+Information) 
 - Following are the steps to run experiments in the cluster.
    1. SSH using vscode
    2. Request resource, and choose right partition and qos
    3. Import your files, and create a python env and kick start experiments
    4. Following commands help

```bash
# ssh to the ece cluster
ssh -Y <netid>@olympus.ece.tamu.edu
# request resource
srun -p <choose partition> --cpus-per-task=8 --gres=gpu:tesla:1 -J gpu-job1 --cpus-per-task=8 -q <choose qos> --pty --x11=first bash
 pick right partition frob the table below
```


<style>

  table {
    border-collapse: collapse;
    width: 80%;
  }
  th, td {
    border: 1px solid #cccccc;
    text-align: left;
    padding: 8px;
  }
  th {
    background-color: #f2f2f2;
  }
  table.center {
    margin-left: auto;
    margin-right: auto;
  }
</style>

<table class = "center">
  <caption>QOS and Hardware Limits</caption>
  <thead>
    <tr>
      <th>QoS Name</th>
      <th>Hardware Limits</th>
      <th>Default Time Limits</th>
      <th>Hard Time Limit</th>
      <th>Partition</th>
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

### HPC TAMU

- High Performance Research Computing at TAMU, [request access](https://hprc.tamu.edu/apply/). Use ECEN 740 course number to get approval

### Public Cloud
- [Google Colab](https://colab.research.google.com/) 

- [Azure for students](https://azure.microsoft.com/en-us/free/students)

- Usual TAMU OAL Labs student accounts. [Access](https://it.tamu.edu/oal/) 

## Python Tutorials

- [Python Tutorial]({% link python1.md %}) Basics of Python
- [Python Tutorial]({% link python2.md %}) PyTorch and TensorFlow
<br>
<br>
<br>
<br>
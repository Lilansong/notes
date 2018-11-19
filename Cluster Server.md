## Cluster Server
"A computer cluster is a set of loosely or tightly connected computers that work together so that, in many respects, they can be viewed as a single system. Unlike grid computers, computer clusters have each node set to perform the same task, controlled and scheduled by software." (Wikipedia)
### The General Concepts
* A computer cluster is a group of tightly coupled computers that work together closely so that it can be viewed as a single computer.

* Clusters are commonly connected through fast local area networks.

* Clusters have evolved to support applications ranging from e-commerce, to high performance database applications.
### Cluster Computing

* A group of interconnected WHOLE COMPUTERS (A system that can refer run on its own apart from the cluster, used in server systems) works together as a unified computing resource that can create the illusion of being one machine having parallel processing.

Why is Clusters than single 1’ s?
* **Price/Performance**

  The reason for the growth in use of clusters is that they have significantly reduced the cost of processing power.
* **Availability**

  Single points of failure can be eliminated, if any one system componentgoes down, the system as a whole stay highly available.
* **Scalability**

  HPC clusters can grow in overall capacity because processors and nodes can be added as demand increases.
### Cluster Catagorization
* **High Availability Clusters**

   Avoid single point of failure
  
   This requires at least two nodes - a primary and a backup.
  
   Always with redundancy
  
   Almost all load balancing cluster are with HA capability.
* **Load Balancing Clusters**

   PC cluster deliver load balancing performance
  
   Commonly used with busy ftp and web servers with large client base
  
   Large number of nodes to share load
* **High Performance Clusters**

   Start from 1994
  
   Donald Becker of NASA assembled this cluster.
  
   Also called Beowulf cluster
  
   Applications like data mining, simulations, parallel processing, weather modeling, etc.
### Design and Configuration
One of the issues in designing a cluster is how tightly coupled the individual nodes may be. For instance, a single computer job may require frequent communication among nodes: this implies that the cluster shares a dedicated network, is densely located, and probably has homogeneous nodes. The other extreme is where a computer job uses one or few nodes, and needs little or no inter-node communication, approaching grid computing.

In a Beowulf cluster, the application programs never see the computational nodes (also called slave computers) but only interact with the "Master" which is a specific computer handling the scheduling and management of the slaves. In a typical implementation the Master has two network interfaces, one that communicates with the private Beowulf network for the slaves, the other for the general purpose network of the organization. The slave computers typically have their own version of the same operating system, and local memory and disk space. However, the private slave network may also have a large and shared file server that stores global persistent data, accessed by the slaves as needed.

A special purpose 144-node DEGIMA cluster is tuned to running astrophysical N-body simulations using the Multiple-Walk parallel treecode, rather than general purpose scientific computations.

Due to the increasing computing power of each generation of game consoles, a novel use has emerged where they are repurposed into High-performance computing (HPC) clusters. Some examples of game console clusters are Sony PlayStation clusters and Microsoft Xbox clusters. Another example of consumer game product is the Nvidia Tesla Personal Supercomputer workstation, which uses multiple graphics accelerator processor chips. Besides game consoles, high-end graphics cards too can be used instead. The use of graphics cards (or rather their GPU's) to do calculations for grid computing is vastly more economical than using CPU's, despite being less precise. However, when using double-precision values, they become as precise to work with as CPU's and are still much less costly (purchase cost).

Computer clusters have historically run on separate physical computers with the same operating system. With the advent of virtualization, the cluster nodes may run on separate physical computers with different operating systems which are painted above with a virtual layer to look similar.

The cluster may also be virtualized on various configurations as maintenance takes place. An example implementation is Xen as the virtualization manager with Linux-HA.
### Data Sharing and Communication
* **Data sharing**

  As the computer clusters were appearing during the 1980s, so were supercomputers. One of the elements that distinguished the three classes at that time was that the early supercomputers relied on shared memory. To date clusters do not typically use physically shared memory, while many supercomputer architectures have also abandoned it.
  
  However, the use of a clustered file system is essential in modern computer clusters. Examples include the IBM General Parallel File System, Microsoft's Cluster Shared Volumes or the Oracle Cluster File System.
  
* **Message passing and communication**

  Two widely used approaches for communication between cluster nodes are MPI (Message Passing Interface) and PVM (Parallel Virtual Machine).
  
  PVM was developed at the Oak Ridge National Laboratory around 1989 before MPI was available. PVM must be directly installed on every cluster node and provides a set of software libraries that paint the node as a "parallel virtual machine". PVM provides a run-time environment for message-passing, task and resource management, and fault notification. PVM can be used by user programs written in C, C++, or Fortran, etc.
  
  MPI emerged in the early 1990s out of discussions among 40 organizations. The initial effort was supported by ARPA and National Science Foundation. Rather than starting anew, the design of MPI drew on various features available in commercial systems of the time. The MPI specifications then gave rise to specific implementations. MPI implementations typically use TCP/IP and socket connections. MPI is now a widely available communications model that enables parallel programs to be written in languages such as C, Fortran, Python, etc. Thus, unlike PVM which provides a concrete implementation, MPI is a specification which has been implemented in systems such as MPICH and Open MPI.
  
### Cluster Management
One of the challenges in the use of a computer cluster is the cost of administrating it which can at times be as high as the cost of administrating N independent machines, if the cluster has N nodes.
In some cases this provides an advantage to shared memory architectures with lower administration costs.
This has also made virtual machines popular, due to the ease of administration.

* **Task scheduling**

  When a large multi-user cluster needs to access very large amounts of data, task scheduling becomes a challenge. In a heterogeneous CPU-GPU cluster with a complex application environment, the performance of each job depends on the characteristics of the underlying cluster. Therefore, mapping tasks onto CPU cores and GPU devices provides significant challenges. This is an area of ongoing research; algorithms that combine and extend MapReduce and Hadoop have been proposed and studied.
* **Node failure management**
  When a node in a cluster fails, strategies such as "fencing" may be employed to keep the rest of the system operational.  Fencing is the process of isolating a node or protecting shared resources when a node appears to be malfunctioning. There are two classes of fencing methods; one disables a node itself, and the other disallows access to resources such as shared disks.
  
  The STONITH method stands for "Shoot The Other Node In The Head", meaning that the suspected node is disabled or powered off. For instance, power fencing uses a power controller to turn off an inoperable node.
  
  The resources fencing approach disallows access to resources without powering off the node. This may include persistent reservation fencing via the SCSI3, fibre channel fencing to disable the fibre channel port, or global network block device (GNBD) fencing to disable access to the GNBD server.
  
## Exam Style Questions
* Define the term **Cluster Servers**

* Define the term **Whole Computers**

* Write down two types of clusters servers

* Outline 3 benefits of **Cluster Computing**

* Outline the significance of **Cluster Management**

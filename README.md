[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/IAASVEAZ)

# CSIT5970 Assignment-1: EC2 Measurement (2 questions, 4 marks)

### Deadline: 11:59PM, Feb, 28, Friday

---

### Name: LIU, Zhenxin
### Student Id: 21072331
### Email: zliugi@connect.ust.hk

---

## Question 1: Measure the EC2 CPU and Memory performance

1. (1 mark) Report the name of measurement tool used in your measurements (you are free to choose *any* open source measurement software as long as it can measure CPU and memory performance). Please describe your configuration of the measurement tool, and explain why you set such a value for each parameter. Explain what the values obtained from measurement results represent (e.g., the value of your measurement result can be the execution time for a scientific computing task, a score given by the measurement tools or something else).

    > The benchmarking tool used in this experiment is the **Phoronix Test Suite**
    >
    > ```shell
    > wget https://phoronix-test-suite.com/releases/repo/pts.debian/files/phoronix-test-suite_10.8.4_all.deb
    > sudo dpkg -i phoronix*.deb
    > ```
    >
    > - **CPU Performance Test**
    >
    > The specific test used was the `pts/compress-7zip` (7-Zip algorithm). This test measures both compression and decompression speeds in MIPS. The results reflect CPU performance under a realistic workload.
    >
    > ```shell
    > sudo apt-get install php-zip
    > phoronix-test-suite run pts/compress-7zip
    > ```
    > - **Memory Performance Test**
    >
    > The specific test used was the `pts/ramspeed` . This test measures memory performance through multiple operations (**Add/Copy/Scale/Triad/Average**) in MB/s The results indicates memory throughput  under operations stress.
    >
    > ```shell
    > phoronix-test-suite run pts/ramspeed
    > ```
    > - **Network Performance Test**
    >
    > `iPerf` and `Ping` were used to measure TCP bandwidth and Round-Trip Time (RTT). The tools assess the network's ability to handle data transfer and latency.
    >
    > ```shell
    > sudo apt-get update
    > sudo apt-get install iperf
    > iperf -s -w <Window_Size>
    > iperf -c <Server_IP> -w <Window_Size>
    > ping <Target_IP>
    > ```
    >
    > The relevant test data below are recorded in the `test_data.md` file.


2. (1 mark) Run your measurement tool on general purpose `t2.micro`, `t2.medium`, and `c5d.large` Linux instances, respectively, and find the performance differences among these instances. Launch all the instances in the **US East (N. Virginia)** region. Does the performance of EC2 instances increase commensurate with the increase of the number of vCPUs and memory resource?

    In order to answer this question, you need to complete the following table by filling out blanks with the measurement results corresponding to each instance type.

    | Size        | CPU performance (MIPS) | Memory performance (MB/s) |
    | ----------- | --------------- | ------------------ |
    | `t2.micro` | 3597 | 10919/11168/10354/10900/2669 |
    | `t2.medium`  | 9641 | 19558/20587/19039/20005/19691 |
    | `c5d.large` | 7417 | 13883/13569/13554/13635/13532 |

    > Region: US East (N. Virginia). Use `Ubuntu Server 22.04 LTS (HVM)` as AMI.

## Question 2: Measure the EC2 Network performance

1. (1 mark) The metrics of network performance include **TCP bandwidth** and **round-trip time (RTT)**. Within the same region, what network performance is experienced between instances of the same type and different types? In order to answer this question, you need to complete the following table.

    > Instances of the same type generally exhibit better network performance, while communication between different instance types tends to show decreased performance.

    | Type                      | TCP b/w (Mbps) | RTT (ms) |
    | :------------------------ | -------------- | -------- |
    | `t3.medium` - `t3.medium` | 3626           | 0.260    |
    | `m5.large` - `m5.large`   | 4966           | 0.177    |
    | `c5n.large` - `c5n.large` | 4946           | 0.158    |
    | `t3.medium` - `c5n.large` | 2453           | 0.756    |
    | `m5.large` - `c5n.large`  | 3413           | 0.466    |
    | `m5.large` - `t3.medium`  | 339            | 1.005    |

    > Region: US East (N. Virginia). Use `Ubuntu Server 22.04 LTS (HVM)` as AMI. Note: Use private IP address when using iPerf within the same region. You'll need iPerf for measuring TCP bandwidth and Ping for measuring Round-Trip time.

2. (1 mark) What about the network performance for instances deployed in different regions? In order to answer this question, you need to complete the following table.

    > Network performance decreases significantly due to geographical distance and reliance on cross-region internet connections.

    | Connection                | TCP b/w (Mbps) | RTT (ms) |
    | ------------------------- | -------------- | -------- |
    | N. Virginia - Oregon      | 32             | 59.900   |
    | N. Virginia - N. Virginia | 4943           | 0.167    |
    | Oregon - Oregon           | 4936           | 0.163    |

    > Region: US East (N. Virginia), US West (Oregon). Use `Ubuntu Server 22.04 LTS (HVM)` as AMI. All instances are `c5.large`. Note: Use public IP address when using iPerf within the same region.

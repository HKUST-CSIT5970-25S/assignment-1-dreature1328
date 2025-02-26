## CPU And Memory Performance Test

### `t2.micro`

#### System Information

```shell
  PROCESSOR:              Intel Xeon E5-2686 v4
    Core Count:           1                                        
    Extensions:           SSE 4.2 + AVX2 + AVX + RDRAND + FSGSBASE 
    Cache Size:           45 MB                                    
    Microcode:            0xd0003f6                                
    Core Family:          Broadwell                                

  GRAPHICS:               Cirrus Logic GD 5446
    Vulkan:               1.3.255          

  MOTHERBOARD:            Xen HVM domU
    BIOS Version:         4.11.amazon             
    Chipset:              Intel 440FX 82441FX PMC 

  MEMORY:                 1024MB

  DISK:                   8GB
    File-System:          ext4                                  
    Mount Options:        discard errors=remount-ro relatime rw 
    Disk Details:         Block Size: 4096                      

  OPERATING SYSTEM:       Ubuntu 22.04
    Kernel:               6.8.0-1021-aws (x86_64)                                                                                         
    Compiler:             GCC 11.4.0                                                                                                      
    System Layer:         Xen HVM domU 4.11.amazon                                                                                        
    Security:             gather_data_sampling: Not affected                                                                              
                          + itlb_multihit: KVM: Mitigation of VMX unsupported                                                             
                          + l1tf: Mitigation of PTE Inversion                                                                             
                          + mds: Vulnerable: Clear buffers attempted no microcode; SMT Host state unknown                                 
                          + meltdown: Mitigation of PTI                                                                                   
                          + mmio_stale_data: Vulnerable: Clear buffers attempted no microcode; SMT Host state unknown                     
                          + reg_file_data_sampling: Not affected                                                                          
                          + retbleed: Not affected                                                                                        
                          + spec_rstack_overflow: Not affected                                                                            
                          + spec_store_bypass: Vulnerable                                                                                 
                          + spectre_v1: Mitigation of usercopy/swapgs barriers and __user pointer sanitization                            
                          + spectre_v2: Mitigation of Retpolines; STIBP: disabled; RSB filling; PBRSB-eIBRS: Not affected; BHI: Retpoline 
                          + srbds: Not affected                                                                                           
                          + tsx_async_abort: Not affected     
```

#### Compress-7zip


    Test 1 of 1
    Estimated Trial Run Count:    3                      
    Estimated Time To Completion: 18 Minutes [11:23 UTC] 
        Started Run 1 @ 11:06:39
        Started Run 2 @ 11:07:28
        Started Run 3 @ 11:08:16
    
    Test: Compression Rating:
        3584
        3613
        3594
    
    Average: 3597 MIPS
    Deviation: 0.41%
    
    Comparison of 2,089 OpenBenchmarking.org samples since 10 May 2024; median result: 96179 MIPS. Box plot of samples:
    [--#####!#########--------------------------*----------------------*-*--*-*-----------------------|      *      ]
                     2 x AMD EPYC 9275F: 507917 ^       AMD EPYC 9845: 857791 ^   2 x AMD EPYC 9655: 1219921 ^
                                               2 x Intel Xeon 6980P: 833643 ^
                                               2 x AMD EPYC 9754: 799824 ^
                                            2 x AMD EPYC 9684X: 782439 ^


    Test: Decompression Rating:
        3066
        3076
        3053
    
    Average: 3065 MIPS
    Deviation: 0.38%
    
    Comparison of 2,052 OpenBenchmarking.org samples since 10 May 2024; median result: 77728 MIPS. Box plot of samples:
    [-####!#######---------------------------------------*-------------*---*-*--------*--------------|             *]
                                Intel Xeon 6980P: 751750 ^ 2 x AMD EPYC 9645: 1160147 ^ 2 x AMD EPYC 9825: 1557636 ^
                                                  2 x AMD EPYC 9565: 1021036 ^
                                                     AMD EPYC 9965: 998566 ^
                                             2 x AMD EPYC 9534: 949019 ^  

#### RAMspeed

```
RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Add - Benchmark: Integer]
    Test 1 of 10
    Estimated Trial Run Count:    3                             
    Estimated Test Run-Time:      7 Minutes                     
    Estimated Time To Completion: 1 Hour, 3 Minutes [16:02 UTC] 
        Started Run 1 @ 15:00:30
        Started Run 2 @ 15:03:15
        Started Run 3 @ 15:06:01

    Type: Add - Benchmark: Integer:
        10944.9
        10885.26
        10929.5

    Average: 10919.89 MB/s
    Deviation: 0.28%

    Comparison of 5,244 OpenBenchmarking.org samples since 26 February 2011; median result: 20288 MB/s. Box plot of samples:
    [     |-----------------*----################!###############-*-*-*--*---------------------------------*----------------|   *   *   *  *           ]
                            ^ This Result (18th Percentile): 10920
                                 8 x 8192 MB DDR4-2400MHz Samsung: 31119 ^     4 x 8 GB DDR4-3600MT: 46451 ^   2 x 32GB DDR5-5600MT: 60836 ^
                                       2 x 8192 MB DDR4-3600MT: 29632 ^                                    2 x 16 GB DDR5-7200MT: 59275 ^
                                       8 x 64 GB DDR4-2666MT: 28938 ^                                   2 x 16GB DDR5-6000MT: 57599 ^
                                        8 x GB DDR4-3200MT: 27743 ^                               32 x 64 GB DDR4-3200MT: 55633 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Copy - Benchmark: Integer]
    Test 2 of 10
    Estimated Trial Run Count:    3                              
    Estimated Test Run-Time:      9 Minutes                      
    Estimated Time To Completion: 1 Hour, 13 Minutes [16:21 UTC] 
        Started Run 1 @ 15:08:53
        Started Run 2 @ 15:11:38
        Started Run 3 @ 15:14:23

    Type: Copy - Benchmark: Integer:
        11177.94
        11167.86
        11159.27

    Average: 11168.36 MB/s
    Deviation: 0.08%

    Comparison of 6,165 OpenBenchmarking.org samples since 26 February 2011; median result: 19014 MB/s. Box plot of samples:
    [    |--*------------*-#############!############-------*----*-*--*----------------------------------*-*------|      *          *              *   ]
                         ^ This Result (19th Percentile): 11168
            ^ 8 x 2048 MB SDRAM: 4490    2 x 16 GB DDR5-4400MT: 35119 ^    32 x 64 GB DDR4-3200MT: 53731 ^            1 x 480GB DRAM-6400MT: 75690 ^
                                      8 x 16 GB DDR4-2667MT: 33438 ^                                    2 x 32GB DDR5-5600MT: 68005 ^
                                     2 x 16GB DDR5-5600MT: 32497 ^                           2 x 16GB DDR5-8000MT: 61883 ^
                              12 x 32 GB DDR4-3200MT: 29730 ^                 2 x 16 GB DDR5-7200MT: 54685 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Scale - Benchmark: Integer]
    Test 3 of 10
    Estimated Trial Run Count:    3                             
    Estimated Test Run-Time:      9 Minutes                     
    Estimated Time To Completion: 1 Hour, 5 Minutes [16:22 UTC] 
        Started Run 1 @ 15:17:15
        Started Run 2 @ 15:20:01
        Started Run 3 @ 15:22:46

    Type: Scale - Benchmark: Integer:
        10383.58
        10342.54
        10337.74

    Average: 10354.62 MB/s
    Deviation: 0.24%

    Comparison of 5,195 OpenBenchmarking.org samples since 26 February 2011; median result: 18527 MB/s. Box plot of samples:
    [    *|--------------*---#############!##############---*--*------*-*------------------------------*---*-------*|  *                        *      ]
                         ^ This Result (18th Percentile): 10355
         ^ 2 x 1024 MB DDR2-800MHz: 2657 4 x 8192 MB DDR4-3200MT: 33077 ^      2 x 16 GB 6000MT: 48069 ^            2 x 32GB DDR5-5600MT: 68064 ^
                                          2 x 16GB DDR5-5600MT: 31937 ^                   2 x 16 GB DDR4-3733MT: 55622 ^
                               6 x 16384 MB DDR4-2933MT: 28756 ^                      2 x 16 GB DDR5-7200MT: 53837 ^
                                  8 x GB DDR4-3200MT: 27328 ^                  2 x 16GB DDR5-6400MT: 49973 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Triad - Benchmark: Integer]
    Test 4 of 10
    Estimated Trial Run Count:    3                      
    Estimated Test Run-Time:      9 Minutes              
    Estimated Time To Completion: 57 Minutes [16:22 UTC] 
        Started Run 1 @ 15:25:38
        Started Run 2 @ 15:28:23
        Started Run 3 @ 15:31:09

    Type: Triad - Benchmark: Integer:
        10896.5
        10886.89
        10919.33

    Average: 10900.91 MB/s
    Deviation: 0.15%

    Comparison of 5,089 OpenBenchmarking.org samples since 26 February 2011; median result: 19952 MB/s. Box plot of samples:
    [     |-----------------*---###############!#############*-*-*-*----------------------------------*---------------*-|      *  *     *              ]
                            ^ This Result (18th Percentile): 10901
                                   8 x 16384 MB DDR4-2666MT: 29099 ^      4 x 8 GB DDR4-3600MT: 45415 ^     2 x 16GB DDR5-8000MT: 61293 ^
                                    2 x 16 GB DDR4-3200MT: 28245 ^                                   2 x 16 GB DDR5-7200MT: 58466 ^
                       8 x 8192 MB DDR4-2400MHz Samsung: 27290 ^                                 32 x 64 GB DDR4-3200MT: 56806 ^
                           16 x 16384 MB DDR3-1866MHz: 26540 ^                                2 x 16 GB 6000MT: 52752 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Average - Benchmark: Integer]
    Test 5 of 10
    Estimated Trial Run Count:    3                      
    Estimated Test Run-Time:      9 Minutes              
    Estimated Time To Completion: 49 Minutes [16:22 UTC] 
        Started Run 1 @ 15:34:00
        Started Run 2 @ 15:36:46
        Started Run 3 @ 15:53:44
        Started Run 4 @ 16:17:50 *
        Started Run 5 @ 16:41:34 *
        Started Run 6 @ 17:05:18 *
        Started Run 7 @ 17:29:02 *
        Started Run 8 @ 17:52:47 *
        Started Run 9 @ 18:16:31 *

    Type: Average - Benchmark: Integer:
        10835.26
        4562.32
        1216.53
        1234.63
        1234.54
        1234.59
        1234.85
        1235.5
        1239.11

    Average: 2669.70 MB/s
    Deviation: 121.89%
    Samples: 9

    Comparison of 6,102 OpenBenchmarking.org samples since 26 February 2011; median result: 17744 MB/s. Box plot of samples:
    [    |*---------------################!#####*##########--------*----*----*--*-------------------------------*|            *     *    *    *        ]
          ^ This Result (2nd Percentile): 2670
               8 x 16384 MB DDR3-1333MHz: 20627 ^  2 x 16 GB DDR5-4400MT: 35585 ^  1 x 480GB DRAM-6400MT: 50139 ^ 2 x 32GB DDR5-5600MT: 64433 ^
                                              16 x 128 GB DDR4-3200MT: 34141 ^                               2 x 16GB DDR5-8000MT: 61691 ^
                                         4 x 4096 MB DDR4-3200MT: 31750 ^                               2 x 16GB DDR5-6000MT: 59714 ^
                                      6 x 16 GB DDR4-2933MT: 29341 ^                             2 x 16 GB DDR5-7200MT: 56620 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Add - Benchmark: Floating Point]
    Test 6 of 10
    Estimated Trial Run Count:    3                              
    Estimated Test Run-Time:      19 Minutes                     
    Estimated Time To Completion: 1 Hour, 35 Minutes [20:14 UTC] 
        Started Run 1 @ 18:40:21
```

### `t2.medium`

#### System Information

```shell
  PROCESSOR:              Intel Xeon E5-2686 v4
    Core Count:           2                                        
    Extensions:           SSE 4.2 + AVX2 + AVX + RDRAND + FSGSBASE 
    Cache Size:           45 MB                                    
    Microcode:            0xd0003f6                                
    Core Family:          Broadwell                                

  GRAPHICS:               Cirrus Logic GD 5446

  MOTHERBOARD:            Xen HVM domU
    BIOS Version:         4.11.amazon             
    Chipset:              Intel 440FX 82441FX PMC 

  MEMORY:                 4096MB

  DISK:                   7GB
    File-System:          ext4                                            
    Mount Options:        commit=30 discard errors=remount-ro relatime rw 
    Disk Details:         Block Size: 4096                                

  OPERATING SYSTEM:       Ubuntu 24.04
    Kernel:               6.8.0-1021-aws (x86_64)                                                                                         
    Compiler:             GCC 13.3.0                                                                                                      
    System Layer:         Xen HVM domU 4.11.amazon                                                                                        
    Security:             gather_data_sampling: Not affected                                                                              
                          + itlb_multihit: KVM: Mitigation of VMX unsupported                                                             
                          + l1tf: Mitigation of PTE Inversion                                                                             
                          + mds: Vulnerable: Clear buffers attempted no microcode; SMT Host state unknown                                 
                          + meltdown: Mitigation of PTI                                                                                   
                          + mmio_stale_data: Vulnerable: Clear buffers attempted no microcode; SMT Host state unknown                     
                          + reg_file_data_sampling: Not affected                                                                          
                          + retbleed: Not affected                                                                                        
                          + spec_rstack_overflow: Not affected                                                                            
                          + spec_store_bypass: Vulnerable                                                                                 
                          + spectre_v1: Mitigation of usercopy/swapgs barriers and __user pointer sanitization                            
                          + spectre_v2: Mitigation of Retpolines; STIBP: disabled; RSB filling; PBRSB-eIBRS: Not affected; BHI: Retpoline 
                          + srbds: Not affected                                                                                           
                          + tsx_async_abort: Not affected  
```

#### Compress-7zip

```shell
7-Zip Compression 24.05:
    pts/compress-7zip-1.11.0
    Test 1 of 1
    Estimated Trial Run Count:    3                      
    Estimated Time To Completion: 17 Minutes [15:08 UTC] 
        Started Run 1 @ 14:51:43
        Started Run 2 @ 14:52:20
        Started Run 3 @ 14:52:58

    Test: Compression Rating:
        9639
        9692
        9593

    Average: 9641 MIPS
    Deviation: 0.51%

    Comparison of 2,089 OpenBenchmarking.org samples since 10 May 2024; median result: 96179 MIPS. Box plot of samples:
    [|---######!############-----*----*--*-*---------------------------------------*--------------*--*----*----*---------------------|        *        ]
                    AMD EPYC 8534P: 348211 ^  2 x INTEL XEON PLATINUM 8592: 702712 ^     AMD EPYC 9755: 947960 ^   2 x AMD EPYC 9655: 1219921 ^
                 AMD EPYC 8534PN: 325245 ^                                     2 x AMD EPYC 9475F: 899868 ^
                                      ^ 2 x AMD EPYC 9184X: 302466             AMD EPYC 9845: 857791 ^
                                 ^ 2 x AMD EPYC 9124: 255210         2 x Intel Xeon 6980P: 833643 ^


    Test: Decompression Rating:
        5784
        5816
        5868

    Average: 5823 MIPS
    Deviation: 0.73%

    Comparison of 2,052 OpenBenchmarking.org samples since 10 May 2024; median result: 77728 MIPS. Box plot of samples:
    [--####!#########----------------------------*-*--*--*---------------------------*-----------*-*------------*-*----------------|                 * ]
                    AMD Ryzen Threadripper 7980X: 573118 ^     AMD EPYC 9755: 874231 ^ 2 x AMD EPYC 9654: 1178644 ^       2 x AMD EPYC 9825: 1557636 ^
                           2 x AMD EPYC 9374F: 538475 ^                              2 x AMD EPYC 9645: 1160147 ^
                            AMD EPYC 9575F: 508509 ^                    2 x AMD EPYC 9565: 1021036 ^
                       2 x AMD EPYC 9365: 484433 ^                         AMD EPYC 9965: 998566 ^

sh: 1: kill: No such process
```

#### RAMspeed


```
RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3
    Memory Test Configuration
        1: Copy
        2: Scale
        3: Add
        4: Triad
        5: Average
        6: Test All Options
        ** Multiple items can be selected, delimit by a comma. **
        Type: 6


        1: Integer
        2: Floating Point
        3: Test All Options
        ** Multiple items can be selected, delimit by a comma. **
        Benchmark: 3


Phoronix Test Suite v10.8.4
System Information


  PROCESSOR:              Intel Xeon E5-2686 v4
    Core Count:           2                                        
    Extensions:           SSE 4.2 + AVX2 + AVX + RDRAND + FSGSBASE 
    Cache Size:           45 MB                                    
    Microcode:            0xd0003f6                                
    Core Family:          Broadwell                                

  GRAPHICS:               Cirrus Logic GD 5446

  MOTHERBOARD:            Xen HVM domU
    BIOS Version:         4.11.amazon             
    Chipset:              Intel 440FX 82441FX PMC 

  MEMORY:                 4096MB

  DISK:                   7GB
    File-System:          ext4                                            
    Mount Options:        commit=30 discard errors=remount-ro relatime rw 
    Disk Details:         Block Size: 4096                                

  OPERATING SYSTEM:       Ubuntu 24.04
    Kernel:               6.8.0-1021-aws (x86_64)                                                                                         
    Compiler:             GCC 13.3.0                                                                                                      
    System Layer:         Xen HVM domU 4.11.amazon                                                                                        
    Security:             gather_data_sampling: Not affected                                                                              
                          + itlb_multihit: KVM: Mitigation of VMX unsupported                                                             
                          + l1tf: Mitigation of PTE Inversion                                                                             
                          + mds: Vulnerable: Clear buffers attempted no microcode; SMT Host state unknown                                 
                          + meltdown: Mitigation of PTI                                                                                   
                          + mmio_stale_data: Vulnerable: Clear buffers attempted no microcode; SMT Host state unknown                     
                          + reg_file_data_sampling: Not affected                                                                          
                          + retbleed: Not affected                                                                                        
                          + spec_rstack_overflow: Not affected                                                                            
                          + spec_store_bypass: Vulnerable                                                                                 
                          + spectre_v1: Mitigation of usercopy/swapgs barriers and __user pointer sanitization                            
                          + spectre_v2: Mitigation of Retpolines; STIBP: disabled; RSB filling; PBRSB-eIBRS: Not affected; BHI: Retpoline 
                          + srbds: Not affected                                                                                           
                          + tsx_async_abort: Not affected                                                                                 

    Would you like to save these test results (Y/n): n

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Add - Benchmark: Integer]
    Test 1 of 10
    Estimated Trial Run Count:    3                              
    Estimated Test Run-Time:      5 Minutes                      
    Estimated Time To Completion: 1 Hour, 17 Minutes [05:40 UTC] 
        Started Run 1 @ 04:23:51
        Started Run 2 @ 04:25:24
        Started Run 3 @ 04:26:57

    Type: Add - Benchmark: Integer:
        19444.42
        19626.49
        19603.92

    Average: 19558.28 MB/s
    Deviation: 0.51%

    Comparison of 5,245 OpenBenchmarking.org samples since 26 February 2011; median result: 20288 MB/s. Box plot of samples:
    [  |-*--------#######*!#######-----------------------------|* * * *    ]
                         ^ This Result (47th Percentile): 19558
         ^ 8 x 4096 MB DDR2-667MHz: 5011  2 x 32GB DDR5-5600MT: 60836 ^
                                       2 x 16 GB DDR5-7200MT: 59275 ^
                                      2 x 16GB DDR5-6000MT: 57599 ^
                                  32 x 64 GB DDR4-3200MT: 55633 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Copy - Benchmark: Integer]
    Test 2 of 10
    Estimated Trial Run Count:    3                              
    Estimated Test Run-Time:      5 Minutes                      
    Estimated Time To Completion: 1 Hour, 13 Minutes [05:40 UTC] 
        Started Run 1 @ 04:28:36
        Started Run 2 @ 04:30:08
        Started Run 3 @ 04:31:40

    Type: Copy - Benchmark: Integer:
        20358.33
        20972.66
        20430.84

    Average: 20587.28 MB/s
    Deviation: 1.63%

    Comparison of 6,166 OpenBenchmarking.org samples since 26 February 2011; median result: 19021 MB/s. Box plot of samples:
    [  |------*######!#*#####----------------------------*|  *    *      * ]
                       ^ This Result (56th Percentile): 20587
              ^ 1 x 8 GB DDR4-2667MT: 11144 1 x 480GB DRAM-6400MT: 75690 ^
                                      2 x 32GB DDR5-5600MT: 68005 ^
                                 2 x 16GB DDR5-8000MT: 61883 ^
                            2 x 16 GB DDR4-3733MT: 58210 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Scale - Benchmark: Integer]
    Test 3 of 10
    Estimated Trial Run Count:    3                             
    Estimated Test Run-Time:      5 Minutes                     
    Estimated Time To Completion: 1 Hour, 8 Minutes [05:40 UTC] 
        Started Run 1 @ 04:33:19
        Started Run 2 @ 04:34:51
        Started Run 3 @ 04:36:24

    Type: Scale - Benchmark: Integer:
        18986.33
        18944.92
        19186.22

    Average: 19039.16 MB/s
    Deviation: 0.68%

    Comparison of 5,196 OpenBenchmarking.org samples since 26 February 2011; median result: 18542 MB/s. Box plot of samples:
    [  |-----*--#######*#######-----------------------*---*|*           *  ]
                       ^ This Result (51st Percentile): 19039
             ^ 1 x 8192 MB 2133MT: 9190     2 x 32GB DDR5-5600MT: 68064 ^
                               2 x 16 GB DDR4-3733MT: 55622 ^
                             2 x 16 GB DDR5-7200MT: 53837 ^
                          2 x 16GB DDR5-6400MT: 49973 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Triad - Benchmark: Integer]
    Test 4 of 10
    Estimated Trial Run Count:    3                             
    Estimated Test Run-Time:      5 Minutes                     
    Estimated Time To Completion: 1 Hour, 3 Minutes [05:40 UTC] 
        Started Run 1 @ 04:38:03
        Started Run 2 @ 04:39:36
        Started Run 3 @ 04:41:09

    Type: Triad - Benchmark: Integer:
        19810.29
        20038.53
        20168.52

    Average: 20005.78 MB/s
    Deviation: 0.91%

    Comparison of 5,089 OpenBenchmarking.org samples since 26 February 2011; median result: 19952 MB/s. Box plot of samples:
    [  |---------########*#######------------------------*-*-|   *  *      ]
                         ^ This Result (50th Percentile): 20006
                                        2 x 16GB DDR5-8000MT: 61293 ^
                                    2 x 16 GB DDR5-7200MT: 58466 ^
                                   2 x 16 GB 6000MT: 52752 ^
                            2 x 32 GB DDR5-4800MT: 50261 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Average - Benchmark: Integer]
    Test 5 of 10
    Estimated Trial Run Count:    3                      
    Estimated Test Run-Time:      5 Minutes              
    Estimated Time To Completion: 59 Minutes [05:40 UTC] 
        Started Run 1 @ 04:42:48
        Started Run 2 @ 04:44:20
        Started Run 3 @ 04:45:53

    Type: Average - Benchmark: Integer:
        19717.12
        19800.02
        19557.48

    Average: 19691.54 MB/s
    Deviation: 0.63%

    Comparison of 6,102 OpenBenchmarking.org samples since 26 February 2011; median result: 17744 MB/s. Box plot of samples:
    [  |------*########!#*#####--------------------------|     *  *  * *   ]
                         ^ This Result (55th Percentile): 19692
              ^ 8 x 4096 MB 1333MHz: 9918  2 x 32GB DDR5-5600MT: 64433 ^
                                         2 x 16GB DDR5-8000MT: 61691 ^
                                      2 x 16GB DDR5-6000MT: 59714 ^
                                  2 x 16 GB DDR5-7200MT: 56620 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Add - Benchmark: Floating Point]
    Test 6 of 10
    Estimated Trial Run Count:    3                      
    Estimated Test Run-Time:      5 Minutes              
    Estimated Time To Completion: 54 Minutes [05:40 UTC] 
        Started Run 1 @ 04:47:33
        Started Run 2 @ 04:49:05
        Started Run 3 @ 04:50:37

    Type: Add - Benchmark: Floating Point:
        19732.29
        20066.16
        19811.71

    Average: 19870.05 MB/s
    Deviation: 0.88%

    Comparison of 4,847 OpenBenchmarking.org samples since 26 February 2011; median result: 19781 MB/s. Box plot of samples:
    [  |*---------#######!*#######--------------------------*|* *    *     ]
                          ^ This Result (50th Percentile): 19870
        ^ 2 x 2048 MB DDR2-667MHz: 3765  2 x 32GB DDR5-5600MT: 59971 ^
                                  32 x 64 GB DDR4-3200MT: 55341 ^
                                      2 x 16 GB 6000MT: 53362 ^
                               2 x 16 GB DDR4-3733MT: 51828 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Copy - Benchmark: Floating Point]
    Test 7 of 10
    Estimated Trial Run Count:    3                      
    Estimated Test Run-Time:      5 Minutes              
    Estimated Time To Completion: 49 Minutes [05:41 UTC] 
        Started Run 1 @ 04:52:17
        Started Run 2 @ 04:53:50
        Started Run 3 @ 04:55:23

    Type: Copy - Benchmark: Floating Point:
        20272.91
        20301.34
        19527.41

    Average: 20033.89 MB/s
    Deviation: 2.19%

    Comparison of 4,994 OpenBenchmarking.org samples since 26 February 2011; median result: 16624 MB/s. Box plot of samples:
    [  |-------####!##*######-------------*-----------*--*|    *          *]
                      ^ This Result (62nd Percentile): 20034
             2 x 16 GB DDR5-5600MT: 41388 ^  1 x 480GB DRAM-6400MT: 75954 ^
                                   2 x 32GB DDR5-5600MT: 64018 ^
                            2 x 16 GB DDR4-3733MT: 57729 ^
                         2 x 16 GB DDR5-7200MT: 54755 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Scale - Benchmark: Floating Point]
    Test 8 of 10
    Estimated Trial Run Count:    3                      
    Estimated Test Run-Time:      5 Minutes              
    Estimated Time To Completion: 45 Minutes [05:41 UTC] 
        Started Run 1 @ 04:57:03
        Started Run 2 @ 04:58:36
        Started Run 3 @ 05:00:09

    Type: Scale - Benchmark: Floating Point:
        17754.32
        17670.67
        17852.61

    Average: 17759.20 MB/s
    Deviation: 0.51%

    Comparison of 4,848 OpenBenchmarking.org samples since 26 February 2011; median result: 16253 MB/s. Box plot of samples:
    [  |*------####!#*######-------------------------| * * *         *     ]
                     ^ This Result (59th Percentile): 17759
        ^ 4 x 2048 MB 800MT: 4383        2 x 32GB DDR5-5600MT: 67793 ^
                              2 x 16 GB DDR4-3733MT: 58047 ^
                            2 x 16 GB DDR5-7200MT: 55403 ^
                           2 x 16GB DDR5-6000MT: 53514 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Triad - Benchmark: Floating Point]
    Test 9 of 10
    Estimated Trial Run Count:    3                      
    Estimated Test Run-Time:      19 Minutes             
    Estimated Time To Completion: 40 Minutes [05:41 UTC] 
        Started Run 1 @ 05:01:48
        Started Run 2 @ 05:03:21
        Started Run 3 @ 05:04:54

    Type: Triad - Benchmark: Floating Point:
        20743.65
        20826.27
        20782.48

    Average: 20784.13 MB/s
    Deviation: 0.20%

    Comparison of 4,858 OpenBenchmarking.org samples since 26 February 2011; median result: 19641 MB/s. Box plot of samples:
    [  |----------########!*######---------------------------*|*  * *      ]
                           ^ This Result (54th Percentile): 20784
                                       2 x 16 GB DDR5-7200MT: 58372 ^
                                    32 x 64 GB DDR4-3200MT: 55960 ^
                                   2 x 16GB DDR5-6000MT: 53382 ^
                                2 x 16 GB DDR4-3733MT: 51870 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Average - Benchmark: Floating Point]
    Test 10 of 10
    Estimated Trial Run Count:    3                      
    Estimated Time To Completion: 22 Minutes [05:28 UTC] 
        Started Run 1 @ 05:06:33
        Started Run 2 @ 05:08:06
        Started Run 3 @ 05:09:40
        Started Run 4 @ 05:14:35 *
        Started Run 5 @ 05:21:32 *
        Started Run 6 @ 05:28:22 *

    Type: Average - Benchmark: Floating Point:
        19625.88
        19353.67
        9996.21
        4293.6
        4395.09
        4390.91

    Average: 10342.56 MB/s
    Deviation: 71.69%
    Samples: 6

    Comparison of 6,022 OpenBenchmarking.org samples since 26 February 2011; median result: 16644 MB/s. Box plot of samples:
    [  |------#*######!########-----------*---------------|   * * *     *  ]
               ^ This Result (26th Percentile): 10343
              2 x 16GB DDR5-5600MT: 35048 ^ 2 x 32GB DDR5-5600MT: 62896 ^
                                     2 x 16 GB DDR5-7200MT: 56908 ^
                                   2 x 16 GB DDR4-3733MT: 54726 ^
                                  2 x 16GB DDR5-6000MT: 53422 ^

    Percentile Classification Of Current Benchmark Run
    MEMORY
        RAMspeed SMP
            Add - Integer:             47th
            Copy - Integer:            56th
            Scale - Integer:           51st
            Triad - Integer:           50th
            Average - Integer:         55th
            Add - Floating Point:      50th
            Copy - Floating Point:     62nd
            Scale - Floating Point:    59th
            Triad - Floating Point:    54th
            Average - Floating Point:  26th
                                       OpenBenchmarking.org Percentile
```

### `c5d.large`

#### System Infomation

```shell
  PROCESSOR:              Intel Xeon Platinum 8124M
    Core Count:           1                                                   
    Thread Count:         2                                                   
    Extensions:           SSE 4.2 + AVX512CD + AVX2 + AVX + RDRAND + FSGSBASE 
    Cache Size:           24.8 MB                                             
    Microcode:            0x2007006                                           
    Core Family:          Cascade Lake                                        

  GRAPHICS:               simpledrmdrmfb
    Vulkan:               1.3.255          
    Screen:               800x600          

  MOTHERBOARD:            Amazon EC2 c5d.large
    BIOS Version:         1.0                     
    Chipset:              Intel 440FX 82441FX PMC 
    Network:              Amazon Elastic          

  MEMORY:                 4096MB

  DISK:                   9GB Amazon Elastic Block Store + 50GB Amazon EC2 NVMe Instance Storage
    File-System:          ext4                                  
    Mount Options:        discard errors=remount-ro relatime rw 
    Disk Scheduler:       NONE                                  
    Disk Details:         Block Size: 4096                      

  OPERATING SYSTEM:       Ubuntu 22.04
    Kernel:               6.8.0-1021-aws (x86_64)                                                                                         
    Compiler:             GCC 11.4.0                                                                                                      
    System Layer:         amazon                                                                                                          
    Security:             gather_data_sampling: Unknown: Dependent on hypervisor status                                                   
                          + itlb_multihit: KVM: Mitigation of VMX unsupported                                                             
                          + l1tf: Mitigation of PTE Inversion                                                                             
                          + mds: Vulnerable: Clear buffers attempted no microcode; SMT Host state unknown                                 
                          + meltdown: Mitigation of PTI                                                                                   
                          + mmio_stale_data: Vulnerable: Clear buffers attempted no microcode; SMT Host state unknown                     
                          + reg_file_data_sampling: Not affected                                                                          
                          + retbleed: Vulnerable                                                                                          
                          + spec_rstack_overflow: Not affected                                                                            
                          + spec_store_bypass: Vulnerable                                                                                 
                          + spectre_v1: Mitigation of usercopy/swapgs barriers and __user pointer sanitization                            
                          + spectre_v2: Mitigation of Retpolines; STIBP: disabled; RSB filling; PBRSB-eIBRS: Not affected; BHI: Retpoline 
                          + srbds: Not affected                                                                                           
                          + tsx_async_abort: Not affected      
```



#### Compress-7zip

```shell
7-Zip Compression 24.05:
    pts/compress-7zip-1.11.0
    Test 1 of 1
    Estimated Trial Run Count:    3                     
    Estimated Time To Completion: 2 Minutes [05:48 UTC] 
        Started Run 1 @ 05:46:16
        Started Run 2 @ 05:46:59
        Started Run 3 @ 05:47:41

    Test: Compression Rating:
        7377
        7443
        7432

    Average: 7417 MIPS
    Deviation: 0.48%

    Comparison of 2,124 OpenBenchmarking.org samples since 10 May 2024; median result: 96179 MIPS. Box plot of samples:
    [--######!##########----------------------------*--------------------------*--*--*---*-------------------|         *     ]
                         2 x AMD EPYC 9275F: 507917 ^         2 x AMD EPYC 9475F: 899868 ^  2 x AMD EPYC 9655: 1219921 ^
                                                               AMD EPYC 9845: 857791 ^
                                                     2 x Intel Xeon 6980P: 833643 ^
                                                     2 x AMD EPYC 9754: 799824 ^


    Test: Decompression Rating:
        4980
        4935
        4936

    Average: 4950 MIPS
    Deviation: 0.52%

    Comparison of 2,087 OpenBenchmarking.org samples since 10 May 2024; median result: 77377 MIPS. Box plot of samples:
    [-####!#######----------------------------------------------*------------*--*-*-----------*--------------|             * ]
                                   2 x Intel Xeon 6766E: 776612 ^  2 x AMD EPYC 9654: 1178644 ^ 2 x AMD EPYC 9825: 1557636 ^
                                                       2 x AMD EPYC 9565: 1021036 ^
                                                     2 x AMD EPYC 9575F: 990954 ^
                                                   2 x AMD EPYC 9534: 949019 ^
```



#### RAMspeed

```shell
RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Add - Benchmark: Integer]
    Test 1 of 10
    Estimated Trial Run Count:    3                             
    Estimated Test Run-Time:      7 Minutes                     
    Estimated Time To Completion: 1 Hour, 2 Minutes [05:31 UTC] 
        Started Run 1 @ 04:29:57
        Started Run 2 @ 04:32:08
        Started Run 3 @ 04:34:19

    Type: Add - Benchmark: Integer:
        13818.41
        13896.09
        13936.19

    Average: 13883.56 MB/s
    Deviation: 0.43%

    Comparison of 5,245 OpenBenchmarking.org samples since 26 February 2011; median result: 20288 MB/s. Box plot of samples:
    [    |------------------#*##########*!#*#*#*######------------------------------*------------------|  *   *  *  *        ]
                             ^ This Result (27th Percentile): 13884
                2 x 8192 MB DDR4-2667MT: 23668 ^       2 x 16 GB DDR5-5600MT: 43424 ^   2 x 32GB DDR5-5600MT: 60836 ^
                16 x 16384 MB 2133MHz: 22584 ^                                      2 x 16 GB DDR5-7200MT: 59275 ^
                                           ^ 2 x 8192 MB DDR4-2133MT: 21421       2 x 16GB DDR5-6000MT: 57599 ^
                 1 x 7908 MB RAM: 19906 ^                                   32 x 64 GB DDR4-3200MT: 55633 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Copy - Benchmark: Integer]
    Test 2 of 10
    Estimated Trial Run Count:    3                      
    Estimated Test Run-Time:      7 Minutes              
    Estimated Time To Completion: 58 Minutes [05:33 UTC] 
        Started Run 1 @ 04:36:36
        Started Run 2 @ 04:38:47
        Started Run 3 @ 04:40:58

    Type: Copy - Benchmark: Integer:
        13629.31
        13597.69
        13482.79

    Average: 13569.93 MB/s
    Deviation: 0.57%

    Comparison of 6,166 OpenBenchmarking.org samples since 26 February 2011; median result: 19021 MB/s. Box plot of samples:
    [   |--------------*#*########!##########---*-*---*------------------------------*---*-----|    *         *           *  ]
                         ^ This Result (28th Percentile): 13570
                     12 x 16384 MB DDR4-3200MT: 32455 ^  2 x 16GB DDR5-6400MT: 51947 ^       1 x 480GB DRAM-6400MT: 75690 ^
                    12 x 32 GB DDR4-3200MT: 29730 ^                               2 x 32GB DDR5-5600MT: 68005 ^
                      8 x GB DDR4-3200MT: 28432 ^                       2 x 16GB DDR5-8000MT: 61883 ^
                       ^ 2 x 4096: 12524                    2 x 16 GB DDR5-7200MT: 54685 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Scale - Benchmark: Integer]
    Test 3 of 10
    Estimated Trial Run Count:    3                      
    Estimated Test Run-Time:      7 Minutes              
    Estimated Time To Completion: 52 Minutes [05:34 UTC] 
        Started Run 1 @ 04:43:16
        Started Run 2 @ 04:45:28
        Started Run 3 @ 04:47:41

    Type: Scale - Benchmark: Integer:
        13552.93
        13523.42
        13588.53

    Average: 13554.96 MB/s
    Deviation: 0.24%

    Comparison of 5,196 OpenBenchmarking.org samples since 26 February 2011; median result: 18542 MB/s. Box plot of samples:
    [    |---------------##*#######!############--*--*----*-*-------------------------*--*-----*-|*                     *    ]
                           ^ This Result (27th Percentile): 13555
                             4 x 8192 MB DDR4-3200MT: 33077 ^ 2 x 16 GB 6000MT: 48069 ^     2 x 32GB DDR5-5600MT: 68064 ^
                              2 x 16GB DDR5-5600MT: 31937 ^          2 x 16 GB DDR4-3733MT: 55622 ^
                     6 x 16384 MB DDR4-2933MT: 28756 ^            2 x 16 GB DDR5-7200MT: 53837 ^
                        8 x GB DDR4-3200MT: 27328 ^          2 x 16GB DDR5-6400MT: 49973 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Triad - Benchmark: Integer]
    Test 4 of 10
    Estimated Trial Run Count:    3                      
    Estimated Test Run-Time:      7 Minutes              
    Estimated Time To Completion: 45 Minutes [05:34 UTC] 
        Started Run 1 @ 04:49:59
        Started Run 2 @ 04:52:11
        Started Run 3 @ 04:54:24

    Type: Triad - Benchmark: Integer:
        13660.7
        13648.26
        13596.43

    Average: 13635.13 MB/s
    Deviation: 0.25%

    Comparison of 5,089 OpenBenchmarking.org samples since 26 February 2011; median result: 19952 MB/s. Box plot of samples:
    [    |-----------------#*##########*!###*#*#*###--------------------------*-------------------*-|    *  *    *           ]
                            ^ This Result (26th Percentile): 13635
                4 x 16384 MB DDR3-1866MT: 24858 ^ 2 x 8 GB DDR4-4400MT: 41416 ^      2 x 16GB DDR5-8000MT: 61293 ^
                      16 x 16GB 1600MT: 23842 ^                                2 x 16 GB DDR5-7200MT: 58466 ^
               16 x 16384 MB 2133MHz: 22707 ^                              32 x 64 GB DDR4-3200MT: 56806 ^
                                       ^ 2 x 16384 MB DDR4-2133MT: 19777  2 x 16 GB 6000MT: 52752 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Average - Benchmark: Integer]
    Test 5 of 10
    Estimated Trial Run Count:    3                      
    Estimated Test Run-Time:      7 Minutes              
    Estimated Time To Completion: 39 Minutes [05:35 UTC] 
        Started Run 1 @ 04:56:43
        Started Run 2 @ 04:58:56
        Started Run 3 @ 05:01:09

    Type: Average - Benchmark: Integer:
        13539.81
        13526.78
        13529.61

    Average: 13532.07 MB/s
    Deviation: 0.05%

    Comparison of 6,102 OpenBenchmarking.org samples since 26 February 2011; median result: 17744 MB/s. Box plot of samples:
    [  *|-------------######*######!############*---*-*-*------------------------------*------|         *     *  *    *      ]
                            ^ This Result (34th Percentile): 13532
       ^ 1 x 512: 1893     6 x 16 GB DDR4-2933MT: 29341 ^  4 x 8 GB DDR4-3600MT: 46831 ^  2 x 32GB DDR5-5600MT: 64433 ^
                         4 x 64 GB DDR4-2933MT: 27962 ^                              2 x 16GB DDR5-8000MT: 61691 ^
                        2 x 16GB DDR4-3200MT: 27363 ^                             2 x 16GB DDR5-6000MT: 59714 ^
                 6 x 4096 MB DDR4-2666MT: 24994 ^                          2 x 16 GB DDR5-7200MT: 56620 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Add - Benchmark: Floating Point]
    Test 6 of 10
    Estimated Trial Run Count:    3                      
    Estimated Test Run-Time:      7 Minutes              
    Estimated Time To Completion: 33 Minutes [05:35 UTC] 
        Started Run 1 @ 05:03:28
        Started Run 2 @ 05:05:41
        Started Run 3 @ 05:07:54

    Type: Add - Benchmark: Floating Point:
        13706.61
        13642.25
        13443.51

    Average: 13597.46 MB/s
    Deviation: 1.01%

    Comparison of 4,847 OpenBenchmarking.org samples since 26 February 2011; median result: 19781 MB/s. Box plot of samples:
    [     |------------------*##########!###*#*#*###*-------------------------------*--------------*-|*   *       *          ]
                             ^ This Result (24th Percentile): 13597
                    12 x 8192 MB DDR4-2666MT: 26381 ^  2 x 16 GB DDR5-5600MT: 43605 ^ 2 x 32GB DDR5-5600MT: 59971 ^
                2 x 16384 MB DDR4-2667MT: 24184 ^                           32 x 64 GB DDR4-3200MT: 55341 ^
             8 x 16384 MB DDR4-2400MHz: 23073 ^                               2 x 16 GB 6000MT: 53362 ^
               12 x 32GB DDR4-2934MT: 21522 ^                         2 x 16 GB DDR4-3733MT: 51828 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Copy - Benchmark: Floating Point]
    Test 7 of 10
    Estimated Trial Run Count:    3                      
    Estimated Test Run-Time:      7 Minutes              
    Estimated Time To Completion: 26 Minutes [05:36 UTC] 
        Started Run 1 @ 05:10:16
        Started Run 2 @ 05:12:33
        Started Run 3 @ 05:14:48

    Type: Copy - Benchmark: Floating Point:
        12898.43
        13059.24
        13322.22

    Average: 13093.30 MB/s
    Deviation: 1.63%

    Comparison of 4,994 OpenBenchmarking.org samples since 26 February 2011; median result: 16624 MB/s. Box plot of samples:
    [   |-------------##*#####!##############-----*-*-*-*-----------------------------*--*----*-|      *                  *  ]
                        ^ This Result (28th Percentile): 13093
                           8 x 16 GB DDR4-2667MT: 33188 ^ 2 x 16GB DDR5-6000MT: 53003 ^      1 x 480GB DRAM-6400MT: 75954 ^
                          2 x 16GB DDR5-5600MT: 32470 ^                    2 x 32GB DDR5-5600MT: 64018 ^
                       4 x 16 GB DDR4-2933MT: 31031 ^            2 x 16 GB DDR4-3733MT: 57729 ^
                    12 x 32 GB DDR4-3200MT: 29655 ^         2 x 16 GB DDR5-7200MT: 54755 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Scale - Benchmark: Floating Point]
    Test 8 of 10
    Estimated Trial Run Count:    3                      
    Estimated Test Run-Time:      7 Minutes              
    Estimated Time To Completion: 20 Minutes [05:36 UTC] 
        Started Run 1 @ 05:17:08
        Started Run 2 @ 05:19:21
        Started Run 3 @ 05:21:34

    Type: Scale - Benchmark: Floating Point:
        13374.75
        13386.49
        13432.43

    Average: 13397.89 MB/s
    Deviation: 0.23%

    Comparison of 4,848 OpenBenchmarking.org samples since 26 February 2011; median result: 16253 MB/s. Box plot of samples:
    [   *|*-*----------###*###!#############------------------------------*-------------| *  *    *              *           ]
                          ^ This Result (29th Percentile): 13398
            ^ 8 x 4096 MB DDR2-667MHz: 4909  4 x 32 GB DDR5-4400MT: 43237 ^          2 x 32GB DDR5-5600MT: 67793 ^
          ^ 4 x 4096 MB DDR: 3984                                    2 x 16 GB DDR4-3733MT: 58047 ^
        ^ 2 x 1024 MB DDR2-800MHz: 2663                         2 x 16 GB DDR5-7200MT: 55403 ^
                                                              2 x 16GB DDR5-6000MT: 53514 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Triad - Benchmark: Floating Point]
    Test 9 of 10
    Estimated Trial Run Count:    3                      
    Estimated Test Run-Time:      7 Minutes              
    Estimated Time To Completion: 14 Minutes [05:36 UTC] 
        Started Run 1 @ 05:23:54
        Started Run 2 @ 05:26:06
        Started Run 3 @ 05:28:19

    Type: Triad - Benchmark: Floating Point:
        13649.63
        13659.13
        13590.98

    Average: 13633.25 MB/s
    Deviation: 0.27%

    Comparison of 4,858 OpenBenchmarking.org samples since 26 February 2011; median result: 19641 MB/s. Box plot of samples:
    [     |------------------*###########!#*#*#*####*#----------------------------*------------------|  *    * * *           ]
                             ^ This Result (25th Percentile): 13633
                    4 x 16384 MB DDR4-2666MT: 25962 ^ 2 x 8 GB DDR4-4400MT: 41660 ^ 2 x 16 GB DDR5-7200MT: 58372 ^
              8 x 16384 MB DDR4-2400MHz: 23098 ^                                   2 x 32GB DDR5-5600MT: 57377 ^
             8 x 8192 MB DDR4-2400MHz: 22130 ^                                 32 x 64 GB DDR4-3200MT: 55960 ^
                   16 x 16GB 1600MT: 21113 ^                                2 x 16GB DDR5-6000MT: 53382 ^

RAMspeed SMP 3.5.0:
    pts/ramspeed-1.4.3 [Type: Average - Benchmark: Floating Point]
    Test 10 of 10
    Estimated Trial Run Count:    3                     
    Estimated Time To Completion: 7 Minutes [05:37 UTC] 
        Started Run 1 @ 05:30:39
        Started Run 2 @ 05:32:52
        Started Run 3 @ 05:35:05

    Type: Average - Benchmark: Floating Point:
        13500.77
        13479.74
        13498.67

    Average: 13493.06 MB/s
    Deviation: 0.09%

    Comparison of 6,022 OpenBenchmarking.org samples since 26 February 2011; median result: 16644 MB/s. Box plot of samples:
    [    |------------#######*#####!##########*#-*-*---*-----------------------------*----------|        * * *          *    ]
                             ^ This Result (36th Percentile): 13493
                             8 x GB DDR4-3200MT: 27533 ^ 4 x 8 GB DDR4-3600MT: 44002 ^      2 x 32GB DDR5-5600MT: 62896 ^
                   4 x 16384 MB DDR4-2666MT: 25697 ^                            2 x 16 GB DDR5-7200MT: 56908 ^
                8 x 16384 MB DDR4-1866MHz: 24459 ^                            1 x 480GB DRAM-6400MT: 55854 ^
              4 x 16384 MB DDR3-1866MT: 23000 ^                             2 x 16 GB DDR4-3733MT: 54726 ^

    Percentile Classification Of Current Benchmark Run
    MEMORY
        RAMspeed SMP
            Add - Integer:             27th
            Copy - Integer:            28th
            Scale - Integer:           27th
            Triad - Integer:           26th
            Average - Integer:         34th
            Add - Floating Point:      24th
            Copy - Floating Point:     28th
            Scale - Floating Point:    29th
            Triad - Floating Point:    25th
            Average - Floating Point:  36th
                                       OpenBenchmarking.org Percentile
```

## Network Performance Test

### `t3.medium` - `t3.medium`

```
[  1] local 172.31.40.119 port 5001 connected with 172.31.32.44 port 45004
[ ID] Interval       Transfer     Bandwidth
[  1] 0.0000-10.0014 sec  4.05 GBytes  3.48 Gbits/sec
[  2] local 172.31.40.119 port 5001 connected with 172.31.32.44 port 52804
[ ID] Interval       Transfer     Bandwidth
[  2] 0.0000-10.0006 sec  4.12 GBytes  3.54 Gbits/sec
[  3] local 172.31.40.119 port 5001 connected with 172.31.32.44 port 35554
[ ID] Interval       Transfer     Bandwidth
[  3] 0.0000-10.0049 sec  4.50 GBytes  3.86 Gbits/sec
```

```shell
64 bytes from 172.31.40.119: icmp_seq=1 ttl=64 time=0.248 ms
64 bytes from 172.31.40.119: icmp_seq=2 ttl=64 time=0.250 ms
64 bytes from 172.31.40.119: icmp_seq=3 ttl=64 time=0.254 ms
64 bytes from 172.31.40.119: icmp_seq=4 ttl=64 time=0.253 ms
64 bytes from 172.31.40.119: icmp_seq=5 ttl=64 time=0.240 ms
64 bytes from 172.31.40.119: icmp_seq=6 ttl=64 time=0.254 ms
64 bytes from 172.31.40.119: icmp_seq=7 ttl=64 time=0.249 ms
64 bytes from 172.31.40.119: icmp_seq=8 ttl=64 time=0.351 ms
64 bytes from 172.31.40.119: icmp_seq=9 ttl=64 time=0.242 ms
64 bytes from 172.31.40.119: icmp_seq=10 ttl=64 time=0.260 ms
```

### `m5.large - m5.large`

```
[  1] local 172.31.18.201 port 5001 connected with 172.31.31.157 port 53150
[ ID] Interval       Transfer     Bandwidth
[  1] 0.0000-10.0006 sec  5.78 GBytes  4.96 Gbits/sec
[  2] local 172.31.18.201 port 5001 connected with 172.31.31.157 port 39378
[ ID] Interval       Transfer     Bandwidth
[  2] 0.0000-10.0006 sec  5.78 GBytes  4.97 Gbits/sec
[  3] local 172.31.18.201 port 5001 connected with 172.31.31.157 port 60436
[ ID] Interval       Transfer     Bandwidth
[  3] 0.0000-10.0009 sec  5.78 GBytes  4.97 Gbits/sec
```

```
64 bytes from 172.31.18.201: icmp_seq=1 ttl=64 time=0.227 ms
64 bytes from 172.31.18.201: icmp_seq=2 ttl=64 time=0.165 ms
64 bytes from 172.31.18.201: icmp_seq=3 ttl=64 time=0.158 ms
64 bytes from 172.31.18.201: icmp_seq=4 ttl=64 time=0.210 ms
64 bytes from 172.31.18.201: icmp_seq=5 ttl=64 time=0.160 ms
64 bytes from 172.31.18.201: icmp_seq=6 ttl=64 time=0.164 ms
64 bytes from 172.31.18.201: icmp_seq=7 ttl=64 time=0.172 ms
64 bytes from 172.31.18.201: icmp_seq=8 ttl=64 time=0.175 ms
64 bytes from 172.31.18.201: icmp_seq=9 ttl=64 time=0.163 ms
64 bytes from 172.31.18.201: icmp_seq=10 ttl=64 time=0.171 ms
```

### `c5n.large - c5n.large`

```
[  1] local 172.31.7.136 port 5001 connected with 172.31.14.167 port 39760
[ ID] Interval       Transfer     Bandwidth
[  1] 0.0000-10.0006 sec  5.76 GBytes  4.95 Gbits/sec
[  2] local 172.31.7.136 port 5001 connected with 172.31.14.167 port 40370
[ ID] Interval       Transfer     Bandwidth
[  2] 0.0000-10.0004 sec  5.74 GBytes  4.93 Gbits/sec
[  3] local 172.31.7.136 port 5001 connected with 172.31.14.167 port 47916
[ ID] Interval       Transfer     Bandwidth
[  3] 0.0000-10.0008 sec  5.77 GBytes  4.96 Gbits/sec
```

```
64 bytes from 172.31.7.136: icmp_seq=1 ttl=64 time=0.140 ms
64 bytes from 172.31.7.136: icmp_seq=2 ttl=64 time=0.158 ms
64 bytes from 172.31.7.136: icmp_seq=3 ttl=64 time=0.167 ms
64 bytes from 172.31.7.136: icmp_seq=4 ttl=64 time=0.155 ms
64 bytes from 172.31.7.136: icmp_seq=5 ttl=64 time=0.158 ms
64 bytes from 172.31.7.136: icmp_seq=6 ttl=64 time=0.149 ms
64 bytes from 172.31.7.136: icmp_seq=7 ttl=64 time=0.163 ms
64 bytes from 172.31.7.136: icmp_seq=8 ttl=64 time=0.166 ms
64 bytes from 172.31.7.136: icmp_seq=9 ttl=64 time=0.158 ms
64 bytes from 172.31.7.136: icmp_seq=10 ttl=64 time=0.168 ms
```



### `t3.medium - c5n.large`

```
[ 10] local 172.31.7.136 port 5001 connected with 172.31.38.104 port 44950
[ ID] Interval       Transfer     Bandwidth
[ 10] 0.0000-10.0004 sec  2.79 GBytes  2.39 Gbits/sec
[ 11] local 172.31.7.136 port 5001 connected with 172.31.38.104 port 54922
[ ID] Interval       Transfer     Bandwidth
[ 11] 0.0000-10.0008 sec  2.99 GBytes  2.57 Gbits/sec
[ 12] local 172.31.7.136 port 5001 connected with 172.31.38.104 port 59766
[ ID] Interval       Transfer     Bandwidth
[ 12] 0.0000-10.0007 sec  2.79 GBytes  2.40 Gbits/sec
```

```
64 bytes from 172.31.7.136: icmp_seq=1 ttl=64 time=0.973 ms
64 bytes from 172.31.7.136: icmp_seq=2 ttl=64 time=1.45 ms
64 bytes from 172.31.7.136: icmp_seq=3 ttl=64 time=0.607 ms
64 bytes from 172.31.7.136: icmp_seq=4 ttl=64 time=0.586 ms
64 bytes from 172.31.7.136: icmp_seq=5 ttl=64 time=0.759 ms
64 bytes from 172.31.7.136: icmp_seq=6 ttl=64 time=0.741 ms
64 bytes from 172.31.7.136: icmp_seq=7 ttl=64 time=0.606 ms
64 bytes from 172.31.7.136: icmp_seq=8 ttl=64 time=0.626 ms
64 bytes from 172.31.7.136: icmp_seq=9 ttl=64 time=0.600 ms
64 bytes from 172.31.7.136: icmp_seq=10 ttl=64 time=0.614 ms
```



### `m5.large - c5n.large`

```
[  4] local 172.31.7.136 port 5001 connected with 172.31.31.154 port 37720
[ ID] Interval       Transfer     Bandwidth
[  4] 0.0000-10.0007 sec  4.00 GBytes  3.44 Gbits/sec
[  5] local 172.31.7.136 port 5001 connected with 172.31.31.154 port 36166
[ ID] Interval       Transfer     Bandwidth
[  5] 0.0000-10.0009 sec  3.90 GBytes  3.35 Gbits/sec
[  6] local 172.31.7.136 port 5001 connected with 172.31.31.154 port 60466
[ ID] Interval       Transfer     Bandwidth
[  6] 0.0000-10.0011 sec  4.02 GBytes  3.45 Gbits/sec
```

```
PING 172.31.7.136 (172.31.7.136) 56(84) bytes of data.
64 bytes from 172.31.7.136: icmp_seq=1 ttl=64 time=0.510 ms
64 bytes from 172.31.7.136: icmp_seq=2 ttl=64 time=0.463 ms
64 bytes from 172.31.7.136: icmp_seq=3 ttl=64 time=0.450 ms
64 bytes from 172.31.7.136: icmp_seq=4 ttl=64 time=0.453 ms
64 bytes from 172.31.7.136: icmp_seq=5 ttl=64 time=0.501 ms
64 bytes from 172.31.7.136: icmp_seq=6 ttl=64 time=0.441 ms
64 bytes from 172.31.7.136: icmp_seq=7 ttl=64 time=0.475 ms
64 bytes from 172.31.7.136: icmp_seq=8 ttl=64 time=0.458 ms
64 bytes from 172.31.7.136: icmp_seq=9 ttl=64 time=0.450 ms
64 bytes from 172.31.7.136: icmp_seq=10 ttl=64 time=0.457 ms
```

### `m5.large - t3.medium`

```
[  1] local 172.31.31.154 port 5001 connected with 172.31.38.104 port 53220
[ ID] Interval       Transfer     Bandwidth
[  1] 0.0000-10.0024 sec   441 MBytes   369 Mbits/sec
[  2] local 172.31.31.154 port 5001 connected with 172.31.38.104 port 42058
[ ID] Interval       Transfer     Bandwidth
[  2] 0.0000-10.0035 sec   368 MBytes   309 Mbits/sec
[  3] local 172.31.31.154 port 5001 connected with 172.31.38.104 port 39496
[ ID] Interval       Transfer     Bandwidth
[  3] 0.0000-10.0032 sec   407 MBytes   341 Mbits/sec
```

```
64 bytes from 172.31.31.154: icmp_seq=1 ttl=64 time=1.01 ms
64 bytes from 172.31.31.154: icmp_seq=2 ttl=64 time=0.991 ms
64 bytes from 172.31.31.154: icmp_seq=3 ttl=64 time=0.991 ms
64 bytes from 172.31.31.154: icmp_seq=4 ttl=64 time=0.996 ms
64 bytes from 172.31.31.154: icmp_seq=5 ttl=64 time=0.995 ms
64 bytes from 172.31.31.154: icmp_seq=6 ttl=64 time=0.995 ms
64 bytes from 172.31.31.154: icmp_seq=7 ttl=64 time=0.989 ms
64 bytes from 172.31.31.154: icmp_seq=8 ttl=64 time=1.00 ms
64 bytes from 172.31.31.154: icmp_seq=9 ttl=64 time=1.08 ms
64 bytes from 172.31.31.154: icmp_seq=10 ttl=64 time=1.00 ms
```

### `N. Virginia - Oregon`

```
[  1] local 172.31.20.52 port 5001 connected with 54.184.124.15 port 54700
[ ID] Interval       Transfer     Bandwidth
[  1] 0.0000-10.0307 sec  38.8 MBytes  32.4 Mbits/sec
[  2] local 172.31.20.52 port 5001 connected with 54.184.124.15 port 39614
[ ID] Interval       Transfer     Bandwidth
[  2] 0.0000-10.0588 sec  40.8 MBytes  34.0 Mbits/sec
[  3] local 172.31.20.52 port 5001 connected with 54.184.124.15 port 59204
[ ID] Interval       Transfer     Bandwidth
[  3] 0.0000-10.0161 sec  38.8 MBytes  32.5 Mbits/sec
```

```
64 bytes from 54.197.151.189: icmp_seq=1 ttl=58 time=59.9 ms
64 bytes from 54.197.151.189: icmp_seq=2 ttl=58 time=59.9 ms
64 bytes from 54.197.151.189: icmp_seq=3 ttl=58 time=59.9 ms
64 bytes from 54.197.151.189: icmp_seq=4 ttl=58 time=59.9 ms
64 bytes from 54.197.151.189: icmp_seq=5 ttl=58 time=59.9 ms
64 bytes from 54.197.151.189: icmp_seq=6 ttl=58 time=59.9 ms
64 bytes from 54.197.151.189: icmp_seq=7 ttl=58 time=59.9 ms
64 bytes from 54.197.151.189: icmp_seq=8 ttl=58 time=59.9 ms
64 bytes from 54.197.151.189: icmp_seq=9 ttl=58 time=59.9 ms
64 bytes from 54.197.151.189: icmp_seq=10 ttl=58 time=59.9 ms
```

### `N. Virginia - N. Virginia`

```
[  4] local 172.31.20.52 port 5001 connected with 172.31.31.115 port 40028
[ ID] Interval       Transfer     Bandwidth
[  4] 0.0000-10.0004 sec  5.77 GBytes  4.96 Gbits/sec
[  5] local 172.31.20.52 port 5001 connected with 172.31.31.115 port 60472
[ ID] Interval       Transfer     Bandwidth
[  5] 0.0000-10.0007 sec  5.74 GBytes  4.93 Gbits/sec
[  6] local 172.31.20.52 port 5001 connected with 172.31.31.115 port 54020
[ ID] Interval       Transfer     Bandwidth
[  6] 0.0000-10.0005 sec  5.75 GBytes  4.94 Gbits/sec
```

```
64 bytes from 172.31.20.52: icmp_seq=1 ttl=64 time=0.183 ms
64 bytes from 172.31.20.52: icmp_seq=2 ttl=64 time=0.171 ms
64 bytes from 172.31.20.52: icmp_seq=3 ttl=64 time=0.164 ms
64 bytes from 172.31.20.52: icmp_seq=4 ttl=64 time=0.161 ms
64 bytes from 172.31.20.52: icmp_seq=5 ttl=64 time=0.159 ms
64 bytes from 172.31.20.52: icmp_seq=6 ttl=64 time=0.168 ms
64 bytes from 172.31.20.52: icmp_seq=7 ttl=64 time=0.171 ms
64 bytes from 172.31.20.52: icmp_seq=8 ttl=64 time=0.162 ms
64 bytes from 172.31.20.52: icmp_seq=9 ttl=64 time=0.165 ms
64 bytes from 172.31.20.52: icmp_seq=10 ttl=64 time=0.165 ms
```

### `Oregon - Oregon`

```
[  1] local 172.31.20.163 port 5001 connected with 172.31.16.116 port 34544
[ ID] Interval       Transfer     Bandwidth
[  1] 0.0000-10.0006 sec  5.73 GBytes  4.92 Gbits/sec
[  2] local 172.31.20.163 port 5001 connected with 172.31.16.116 port 47196
[ ID] Interval       Transfer     Bandwidth
[  2] 0.0000-10.0006 sec  5.78 GBytes  4.96 Gbits/sec
[  3] local 172.31.20.163 port 5001 connected with 172.31.16.116 port 35996
[ ID] Interval       Transfer     Bandwidth
[  3] 0.0000-10.0002 sec  5.74 GBytes  4.93 Gbits/sec
```

```
64 bytes from 172.31.20.163: icmp_seq=1 ttl=64 time=0.164 ms
64 bytes from 172.31.20.163: icmp_seq=2 ttl=64 time=0.179 ms
64 bytes from 172.31.20.163: icmp_seq=3 ttl=64 time=0.232 ms
64 bytes from 172.31.20.163: icmp_seq=4 ttl=64 time=0.156 ms
64 bytes from 172.31.20.163: icmp_seq=5 ttl=64 time=0.142 ms
64 bytes from 172.31.20.163: icmp_seq=6 ttl=64 time=0.177 ms
64 bytes from 172.31.20.163: icmp_seq=7 ttl=64 time=0.142 ms
64 bytes from 172.31.20.163: icmp_seq=8 ttl=64 time=0.142 ms
64 bytes from 172.31.20.163: icmp_seq=9 ttl=64 time=0.143 ms
64 bytes from 172.31.20.163: icmp_seq=10 ttl=64 time=0.151 ms
```


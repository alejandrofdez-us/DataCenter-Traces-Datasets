# DataCenter-Traces-Datasets
Public datasets organized for machine learning or artificial intelligence usage. The following dasets can be used:

## Alibaba 2018 machine usage
Processed from the original files found at:
https://github.com/alibaba/clusterdata/tree/master/cluster-trace-v2018

This repository dataset of machine usage includes the following columns:
```Bash
+--------------------------------------------------------------------------------------------+
| Field            | Type       | Label | Comment                                            |
+--------------------------------------------------------------------------------------------+
| cpu_util_percent | bigint     |       | [0, 100]                                           |
| mem_util_percent | bigint     |       | [0, 100]                                           |
| net_in           | double     |       | normarlized in coming network traffic, [0, 100]    |
| net_out          | double     |       | normarlized out going network traffic, [0, 100]    |
| disk_io_percent  | double     |       | [0, 100], abnormal values are of -1 or 101         |
+--------------------------------------------------------------------------------------------+
```![assigned_mem_month](https://user-images.githubusercontent.com/19324988/202569814-26cbda84-4c1b-425a-bc15-58378f24765e.png)

Three sampled datasets are found: average value of each column grouped every 10 seconds as original, and downsampled to 30 seconds and 300 seconds as well.
Every column includes the average utilization of the whole data center.

### Figures
Some figures were generated from these datasets

![cpu_util_percent_usage_days_1_to_8_grouped_10_seconds](https://user-images.githubusercontent.com/19324988/202569296-3bb72ad4-92e7-4200-a19d-ef6fc26722ce.png)
Figure: CPU utilization sampled every 10 seconds

![mem_util_percent_usage_days_1_to_8_grouped_300_seconds](https://user-images.githubusercontent.com/19324988/202569501-7840c0a0-b4e8-4f7d-bb92-875e38c616e8.png)![cpu_usage_day_09](https://user-images.githubusercontent.com/19324988/202570243-1390bf7c-5dc2-4c35-86c6-b7d74ae4dd44.png)
Figure: Memory utilization sampled every 300 seconds


## Google 2019 instance usage
Processed from the original dataset and queried using Big Query. More information available at:
https://research.google/tools/datasets/google-cluster-workload-traces-2019/

This repository dataset of instance usage includes the following columns:
```Bash
+--------------------------------------------------------------------------------------------+
| Field                         | Type       | Label | Comment                               |
+--------------------------------------------------------------------------------------------+
| avg_cpu                       | double     |       | [0, 1]                                |
| avg_mem                       | double     |       | [0, 1]                                |
| avg_assigned_mem              | double     |       | [0, 1]                                |
| avg_cycles_per_instruction    | double     |       | [0, _]                                |
+--------------------------------------------------------------------------------------------+
```
One sampled dataset is found: average value of each column grouped every 300 seconds as original.
Every column includes the average utilization of the whole data center.

### Figures
Some figures were generated from these datasets

![cpu_usage_day_26](https://user-images.githubusercontent.com/19324988/202570580-6be32fd7-3e39-4e0a-bc8e-abda05c5edd2.png)
Figure: CPU usage day 26

![mem_usage_day_26](https://user-images.githubusercontent.com/19324988/202570586-388eafcd-a70e-40d3-8a80-9cdab0ef6236.png)
Figure: Mem usage day 26

![assigned_mem_day_26](https://user-images.githubusercontent.com/19324988/202570579-6d9744f8-97fb-42d2-bb9a-b9c7cf88bdb4.png)
Figure: Assigned mem day 26

![cycles_per_instruction_day_26](https://user-images.githubusercontent.com/19324988/202570583-e28bae12-8540-4a69-845b-12cfc9be8c33.png)
Figure: Cycles per instruction day 26




## Azure v2 virtual machine workload
Processed from the original dataset. More information available at:
https://github.com/Azure/AzurePublicDataset/blob/master/AzurePublicDatasetV2.md

This repository dataset of instance usage includes the following columns:
```Bash
+--------------------------------------------------------------------------------------------+
| Field                         | Type       | Label | Comment                               |
+--------------------------------------------------------------------------------------------+
| cpu_usage                     | double     |       | [0, _]                                |
| assigned_mem                  | double     |       | [0, _]                                |
+--------------------------------------------------------------------------------------------+
```
One sampled dataset is found: sum value of each column grouped every 300 seconds as original.
Every column includes the total consumption of the whole data center virtual machines.

![cpu_usage_month](https://user-images.githubusercontent.com/19324988/202569892-50ceb7d1-7892-4c36-bd81-ab2b3398bf58.png)
CPU total usage by virtual machines sampled every 300 seconds.

![assigned_mem_month](https://user-images.githubusercontent.com/19324988/202569860-c85fe1da-4604-435f-8315-7d6b828a8ba2.png)
Total assigned memory for virtual machines sampled every 300 seconds.


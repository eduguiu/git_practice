# Table to compare results (NB: 01_Pets). 

 | Instance  | Model |  BS | Time(frozen) | ErrRate.15 | Time(Unfrz) | ErrRate.27 | Cost($/hour) | Total | 
 | --- | --- | --- | --- | --- | --- | --- | --- | --- |
 | g2.2xlarge | Resnet34 | 64 | 19m | 0.10 | 27m | 0.08 | 0.8 | |
 | g2.2xlarge | Resnet50 | 32 | 19m | 0.10 | 27m | 0.12 | 0.32 | |
 | g2.8xlarge | Resnet34 | 64 | 8m | 0.12 | -- | -- | 2.9 | |
 | g2.8xlarge | Resnet34 | 128 | 7m | 0.10 | 13m | 0.12 | 2.9 | |
 | g2.8xlarge | Resnet50 | 64 | 10m | 0.08 | 27m | 0.37 | 2.9 | |
 | m5a.8xlarge | Resnet34 | 256 | 5m | 0.13 | 8m | 0.08 | 1.38 | 3hores|
 | m5a.8xlarge | Resnet50 | 256 | 20m | 0.8 | 25m | 0.36 | 1.38 | " |
 | p2.xlarge | Resnet34 | 64 | 18m | 0.10 | 26m | 0.08 | 7.2 | |
 | p2.xlarge | Resnet50 | 32 |  | -- | -- | -- | 7.2 | |




# Connecting several machines in parallel
 - $ ssh -i .ssh/id_rsa -L localhost:8888:localhost:8888 ubuntu@IP_1st_system
 - $ ssh -i .ssh/id_rsa -L localhost:*8889*:localhost:8888 ubuntu@IP_2nd_system



This table states Instances that can be used for our FastAI training. We would favor Large CPU'd instances for DL1, whereas for the DL2 (usage of CUDA) we will favor GPU based instances. Therefore:
- for DL1, we will choose something north of M5 instances (>32 CPUs) with ca. $1/hour
- for DL2, we will choose something north of P2.xlarge instances (>32 CPUs) with ca. $1/hour

NB: using a G2 instance or P2 instance in the DL1 part of the course won't be useful since they are limited in terms of CPU, but they are priced for a GPU that DL1 will never use. 




 | Instance  | GPU | GPU_mem | CUDA | Memory | vCPUs | Cost($/hour) | NtBook | Time | 
 | --- | --- | --- | --- | --- | --- | --- | --- | --- |
 | g2.2xlarge | GRID K530 | 4 | 3.0| 15 | 8 | 0.65 | 01_Pets | 2hores |
 | g2.8xlarge | GRID K520 | 32 | 3.0| 60 | 32 | 2.90 | 01_Pets | 2hores |
 | m5a.8xlarge | -  | - | - | 128 | 32 | 1.38 | 01_Pets | -- |
 | m5a.12xlarge | -  | - | - | 192 | 48 | 2.1 | 01_Pets | -- |
 | g3.4xlarge | TESLA M60 | 8 | 5.2| 122 | 16 | 1.14 | 01_Pets | -- |
 | g3.8xlarge | TESLA M60 x2 | 16 | 5.2 | 244 | 32 | 2.28 | 01_Pets | -- |
 | p2.xlarge | TESLA K80 | 12 | 3.7| 61 | 4 | 0.90 | 01_Pets |-- |
 | p2.8xlarge | TESLA K80 | 96 | 3.7 | 488 | 32 | 7.20 | 01_Pets | -- |
 | p3.2xlarge | TESLA V100 | 16 | 7.0 | 61 | 8 | 3.6 | 01_Pets | -- |
 | p3.8xlarge | TESLA V100x4 | 64 | 7.0 | 244 | 32 | 12.24 | 01_Pets | -- |
 
 - source: https://www.ec2instances.info/?filter=p3&region=us-west-2


https://mc.ai/setup-tensorflow-gpu-with-aws-ec2-on-ubuntu-16-04-in-10-minutes/

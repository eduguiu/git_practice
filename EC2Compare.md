# Table to compare results (NB: 01_Pets). 

 | Instance  | Model |  BS | Time(frozen) | ErrRate.15 | Time(Unfrz) | ErrRate.27 | Cost($/hour) | Total | 
 | --- | --- | --- | --- | --- | --- | --- | --- | --- |
 | g2.2xlarge | Resnet34 | 64 | 19m | 0.10 | 27m | 0.08 | 0.8 | |
 | g2.2xlarge | Resnet50 | 32 | 19m | 0.10 | 27m | 0.12 | 0.32 | |
 | g2.8xlarge | Resnet34 | 64 | 8m | 0.12 | -- | -- | 2.9 | |
 | g2.8xlarge | Resnet34 | 128 | 7m | 0.10 | 13m | 0.12 | 2.9 | |
 | g2.8xlarge | Resnet50 | 64 | 10m | 0.08 | 27m | 0.37 | 2.9 | |
 | m5a.8xlarge | Resnet34 | 256 | 5m | 0.13 | 8m | 0.08 | 1.38 | |
 | m5a.8xlarge | Resnet50 | 256 |  | 0.13 | 15m | 0.0 | 1.38 | |
 | p2.xlarge | Resnet34 | 64 | 17m | 0.13 | 8m | 0.08 | 7.2 | |
 | p2.xlarge | Resnet50 | 32 |  | 0.13 | -- | -- | 7.2 | |




# Connecting several machines in parallel
 - $ ssh -i .ssh/id_rsa -L localhost:8888:localhost:8888 ubuntu@IP_1st_system
 - $ ssh -i .ssh/id_rsa -L localhost:*8889*:localhost:8888 ubuntu@IP_2nd_system




 | Instance  | GPU | GPU_mem | CUDA | Memory | vCPUs | Cost($/hour) | NtBook | Time | 
 | --- | --- | --- | --- | --- | --- | --- | --- | --- |
 | g2.2xlarge | GRID K530 | 4 | 3.0| 15 | 8 | 0.08 | 01_Pets | 2hores |
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

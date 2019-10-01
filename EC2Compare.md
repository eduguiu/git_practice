# Table to compare results. 

 | Instance  | NB | Model |  BS | Time(frozen) | ErrRate.15 | Time(Unfrz) | ErrRate.27 | Cost($/hour) | Total | 
 | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
 | g2.2xlarge | 01_Pets| Resnet34 | 64 | 19m | 0.10 | 27m | 0.08 | 0.8 | |
 | g2.2xlarge | 01_Pets| Resnet50 | 32 | 19m | 0.10 | 27m | 0.12 | 0.32 | |
 | g2.8xlarge | 01_Pets| Resnet34 | 64 | 8m | 0.12 | -- | -- | 2.9 | |
 | g2.8xlarge | 01_Pets| Resnet34 | 128 | 7m | 0.10 | 13m | 0.12 | 2.9 | |




# Connecting several machines in parallel
 - $ ssh -i .ssh/id_rsa -L localhost:8888:localhost:8888 ubuntu@IP_1st_system
 - $ ssh -i .ssh/id_rsa -L localhost:*8889*:localhost:8888 ubuntu@IP_2nd_system




 | Instance  | GPU | CUDA | Memory | vCPUs | Cost($/hour) | NtBook | Time | 
 | --- | --- | --- | --- | --- | --- | --- | --- |
 | g2.2xlarge | 15 | 8 | 0.08 | 01_Pets | 2hores |
 | g2.8xlarge | 60 | 32 | 2.90 | 01_Pets | 2hores |
 | g3.8xlarge | 60 | 32 | 2.90 | 01_Pets | 2hores |
 | g2.8xlarge | 60 | 32 | 2.90 | 01_Pets | 2hores |
 | g2.8xlarge | 60 | 32 | 2.90 | 01_Pets | 2hores |
 | g2.8xlarge | 60 | 32 | 2.90 | 01_Pets | 2hores |
 | g2.8xlarge | 60 | 32 | 2.90 | 01_Pets | 2hores |
 | g2.8xlarge | 60 | 32 | 2.90 | 01_Pets | 2hores |

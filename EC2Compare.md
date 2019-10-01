# Table to compare results. 

 | Instance  | NB | Model |  BS | Time(frozen) | ErrRate.15 | Time(Unfrz) | ErrRate.27 | Cost($/hour) |
 | --- | --- | --- | --- | --- | --- | --- | --- | --- | 
 | g2.2xlarge | 01_Pets| Resnet34 | 64 | 19m | 0.10 | 27m | 0.12 | 0.32 |


# Connecting several machines in parallel
 - $ ssh -i .ssh/id_rsa -L localhost:8888:localhost:8888 ubuntu@IP_1st_system
 - $ ssh -i .ssh/id_rsa -L localhost:*8889*:localhost:8888 ubuntu@IP_2nd_system



Mapping EC2 Instance Types to IBM Cloud Instance Profiles

IBM's new Generation 2 VM Service has new profiles (flavors), this maps common EC2 types to a similar type in IBM Cloud.

> Note this is not official don't sue me. This is for quick reference only, always check what you're doing yourself.

| AWS EC2      | IBM Equivalent |  vCPU(IBM) | Memory(G)(IBM) | Notes   |
|---|---|---|---|---|
| m4.large     | bx2-2x8        |          2 |              8 | "Balanced"  | 
| m4.xlarge    | bx2-4x16       |          4 |             16 |  "Balanced"  |
| m4.2xlarge   | bx2-8x32       |          8 |             32 |  "Balanced"  |
| m4.4xlarge   | bx2-16x64      |         16 |             64 |  "Balanced"  |
| m4.10xlarge  | bx2-32x128     |         32 |            128 |  "Balanced", AWS values differ |
| m4.16xlarge  | bx2-48x192     |         48 |            192 |  "Balanced", AWS values differ  |
| c4.large     | cx2-2x4        |          2 |              4 | "Compute"  | 
| c4.xlarge    | cx2-4x8        |          4 |              8 | "Compute"  | 
| c4.2xlarge   | cx2-8x16       |          8 |             16 | "Compute"  | 
| c4.4xlarge   | cx2-16x32      |         16 |             32 | "Compute"  | 
| c4.8xlarge   | cx2-32x64      |         32 |             64 | "Compute", AWS values differ  | 
| c4.8xlarge   | cx2-48x96      |         48 |             96 | "Compute", duplicate, AWS values differ | 
| r4.large     | mx2-2x16       |          2 |             16 | "Memory"  | 
| r4.xlarge    | mx2-4x32       |          4 |             32 |  "Memory"  |
| r4.2xlarge   | mx2-8x64       |          8 |             64 |  "Memory"  |
| r4.4xlarge   | mx2-16x128     |         16 |            128 |  "Memory"  |
| r4.8xlarge   | mx2-32x256     |         32 |            256 |  "Memory", AWS values differ |
| r4.16xlarge  | mx2-48x384     |         48 |            385 |  "Memory", AWS values differ  |


Get a view of IBM Cloud Gen 2 VPC Infrastructure instance profiles with this command:Com

```
$ ibmcloud is in-prs
Listing instance profiles for generation 2 compute in region us-south under account Cloud Open Source as user skrum@us.ibm.com...
Name         Architecture   Family     vCPUs   Memory(G)   Network Performance (Gbps)   GPUs
bx2-2x8      amd64          balanced   2       8           4                            -
bx2-4x16     amd64          balanced   4       16          8                            -
bx2-8x32     amd64          balanced   8       32          16                           -
bx2-16x64    amd64          balanced   16      64          32                           -
bx2-32x128   amd64          balanced   32      128         64                           -
bx2-48x192   amd64          balanced   48      192         80                           -
cx2-2x4      amd64          compute    2       4           4                            -
cx2-4x8      amd64          compute    4       8           8                            -
cx2-8x16     amd64          compute    8       16          16                           -
cx2-16x32    amd64          compute    16      32          32                           -
cx2-32x64    amd64          compute    32      64          64                           -
cx2-48x96    amd64          compute    48      96          80                           -
mx2-2x16     amd64          memory     2       16          4                            -
mx2-4x32     amd64          memory     4       32          8                            -
mx2-8x64     amd64          memory     8       64          16                           -
mx2-16x128   amd64          memory     16      128         32                           -
mx2-32x256   amd64          memory     32      256         64                           -
mx2-48x384   amd64          memory     48      384         80                           -
```


Sources:

* [aws ec2 docs](https://aws.amazon.com/ec2/instance-types/)


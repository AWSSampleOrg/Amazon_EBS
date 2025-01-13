# Formula

```
Throughput (MiB/s) = IOPS x IO size (KiB I/O) / 1024
```

# I/O

- https://docs.aws.amazon.com/ebs/latest/userguide/ebs-io-characteristics.html#ebs-io-iops

SSD volumes support a maximum I/O size of 256 KiB.
HDD volumes support a maximum I/O size of 1024 KiB or 1 MiB.

```
                                    Sum(VolumeReadOps) + Sum(VolumeWriteOps)
Estimated average IOPS in ops/s = ----------------------------------------
                                        Period - Sum(VolumeIdleTime)
```

```
                                        (Sum(VolumeReadBytes) + Sum(VolumeWriteBytes)) / 1024
Estimated average throughput in KiB/s = -----------------------------------------------------
                                                Period - Sum(VolumeIdleTime)
```

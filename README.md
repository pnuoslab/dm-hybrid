# dm-hybrid

`dm-hybrid` is a modified Linux Device Mapper target designed to improve random-write handling on Zoned Namespace (ZNS) SSDs.

## Features

### Hybrid Mapping

Allows multiple logical chunks to share a single random zone, improving random-zone utilization and reducing unnecessary reclaim operations.

### Chunk-Snapshot Reclaim

Performs reclaim at the logical-chunk level using a snapshot of mapping information, allowing write and reclaim operations to proceed concurrently.

## Installation

Copy the provided `dm-hybrid` source files into the Linux kernel Device Mapper directory.

```bash
cp <dm-hybrid-source-files> /path/to/linux/drivers/md/
```

Then configure and compile the Linux kernel.

After compilation, boot the system using the newly built kernel.

## Note

`dm-hybrid` is intended for research and experimental use with ZNS SSDs.

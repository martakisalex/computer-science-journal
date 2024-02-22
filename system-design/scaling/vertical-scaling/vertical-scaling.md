# Vertical Scaling

<img src="https://www.freecodecamp.org/news/content/images/size/w600/2022/06/02vertical-scaling-software-scalability.jpg" height="100">

## Overview

Vertical scaling, also known as scaling up, refers to adding more power (CPU, RAM, Storage) to an existing machine or replacing it with a more powerful one. Unlike horizontal scaling, where capacity is increased by adding more machines, vertical scaling focuses on increasing the capacity of a single machine.

## Key Features

- **Simplicity**: Does not require significant changes to the application's architecture or the addition of more instances.
- **Immediate Impact**: Enhancements in hardware specifications lead to an immediate improvement in performance.
- **No Distribution Overhead**: Eliminates the complexities associated with distributed systems, such as network latency and data consistency issues.

## Advantages

- **Ease of Implementation**: Less complex than horizontal scaling as it involves upgrading existing hardware.
- **Lower Initial Cost**: Initially more cost-effective for small to medium-sized applications that do not require the infrastructure of multiple machines.
- **Latency Reduction**: Can reduce latency by avoiding the overhead associated with communication between distributed nodes.

## Use Cases

- **Legacy Systems**: Suitable for legacy applications where horizontal scaling may not be possible due to architectural constraints.
- **Small to Medium Databases**: Effective for databases that can benefit from faster CPUs or more memory without needing to be distributed.
- **Monolithic Applications**: Ideal for monolithic applications where application components are closely integrated and difficult to scale out.

Vertical scaling provides a straightforward approach to enhance system capacity, suitable for applications with limitations on distribution or for those not yet requiring the complexity of horizontal scaling.

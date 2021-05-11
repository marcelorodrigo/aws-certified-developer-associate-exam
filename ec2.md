# EC2
## Instances Purchase Options
- On-Demand
- Reserved
  - 1 year minimum
  - Convertible: long workloads with flexible instances types over time
  - Scheduled: for a repeated time scheduled reservation
- Spot: short jobs with cheap instances. But you can easily lose the instance due to the pricing model.
- Dedicated
  - Dedicated Host
    - A physical server just for you
    - Helps you to meet **compliance requirements**
    - Reduce costs by allowing you to use your **server-bound licenses**
    - Allocated to your account for 3y
  - Dedicated Instance
    - Hardware is dedicated to you, you may share the hardware with other instances in your account
    - No control over which your dedicated hardware your instance will be running.
- Instance Store: provides temporary block-level storage for your instance. This storage is located on disks that are physically attached to the host computer.

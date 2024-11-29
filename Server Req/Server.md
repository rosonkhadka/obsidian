Application Server (Prod):

    Total of 200GB RAM and 512GB-1TB storage.
    Instead of a single server, we propose creating four to five virtual machines (VMs) with:
        40-50GB RAM each.
        Shared storage of 512GB-1TB.
        12-14 vCPUs per VM.
    This setup will enable us to build a robust cluster, ensuring high availability and facilitating zero-downtime deployments to production.

MinIO Server:

    A dedicated VM with:
        2-4TB storage.
        32GB RAM.
        4-6 vCPUs to support our object storage needs.

Website Server:

    A dedicated VM specifically for hosting websites, requiring:
        25-32GB RAM.
        30GB storage.
        4-6 vCPUs to handle website operations efficiently.

DEV and TEST Servers:

    Dedicated VMs for development and testing environments for all websites and applications to run simultaneously:
        150 GB RAM across the environment.
        300GB storage.
        6-8 vCPUs per VM to support concurrent workloads.

Database Server:

    A dedicated VM optimized for database workloads, requiring:
        100GB RAM.
        Adequate storage to support database operations (to be discussed based on requirements).
        8-12 vCPUs to handle high read/write operations efficiently.
        
Storage - 500GB - 1TB

Singe Server - VM

Docker Isolation
1. Prod
2. Demo / Test

----
NAS

RAM - 550 GB - MIN
Storage - 5TB - MIN




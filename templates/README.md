# CMG Simulation Templates

## SPE Job Template

This template is introduced to run a conventional CMG job in Azure Batch in a Linux environment. It creates a pool and submits a job to the pool, and then a task which performs a simple CMG simulation in Azure Batch account.

## MPI Job Template

This template is introduced to run an MPI command in Azure Batch in a Linux environment. It creates a pool with MPI/RDMA enabled virtual machines, then submits a job to the pool. The task will perform a CMG MPI simulation in Azure Batch account.

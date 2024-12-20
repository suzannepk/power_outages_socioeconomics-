Here is a summary of what each script set does:

**eaglei_mpi.py**

This Python code performs parallel data processing using the mpi4py library to calculate the total number of blackouts from a set of CSV files, each containing data for a specific year (from 2014 to 2022). Here's a step-by-step breakdown of what the code does:

Initialize MPI Communication:

The MPI.COMM_WORLD object is initialized, which represents the group of all parallel processes.

The rank of each process is retrieved using comm.Get_rank(). The rank uniquely identifies each process (e.g., rank 0, rank 1, etc.).

Data File Mapping:

A list file_nums contains the years corresponding to the files.

Each process reads a specific CSV file, determined by its rank. For example, rank 0 will read eaglei_outages_2014.csv, rank 1 will read eaglei_outages_2015.csv, and so on.

Read CSV File:

Each process reads its assigned CSV file into a Pandas DataFrame using pd.read_csv.

Calculate Local Blackout Sum:


The sum column in the DataFrame contains the blackout counts for that year. The script calculates the sum of these counts using blackouts.sum().

Reduce Operation:

The comm.reduce operation is used to combine the local sums from all processes into a single global total.
The reduction uses the MPI.SUM operation to sum up the values across all processes, and the result is collected by the process with rank 0 (the root process).

Timing:

The script records the execution time using the time module. It measures the time from the start (t1) to the end (t2) of the script.

Output Results (Root Process Only):

If the process is rank 0, it prints the total execution time and the total number of blackouts across all years.

Assumptions:

The script assumes there are 9 processes, corresponding to the 9 years of data. This must be ensured when running the script (e.g., mpirun -np 9).

The CSV files are located in the ../data/eaglei_outages/ directory and are named eaglei_outages_<year>.csv.

The sum column exists in the CSV files and contains the blackout counts.

Output Example (for rank 0):

The total execution time of the script.

The total number of blackouts across all years.

Parallel Efficiency:

By distributing the reading and processing of files among multiple processes, the script speeds up the computation, especially if the data files are large.


Scripts for submitting batch parameter sweeps via qsub

You can run these scripts using octave or matlab to generate your batch submission job.

create_run
This function creates a set of iterative calls to some function with varying inputs
Generally: create_run(run_id,function_name,arg1,arg2,...,argn)
run_id is some unique identifier
function_name is passed as a string to the execution step
arg1...argn are parameter matricies eg:
arg1=[0:1:50]
arg2=[1:1:3]
Runs 150 times for the combis
1,1
1,2
1,3
2,1
2,2
2,3.....
Numerical ARG only

To use:
Edit the qsub_args, exec_dir in the header of the file create_run.m
If you're using MATLAB, great, if not, then you're on your own for data reduction

Edit the create_script file:
The store_file is where the script ends up, ignore that

The exec_str is the string format combination of inputs eg "1,2" along with the function name:
called create_run(555,"my_script_file",[1:50],[1:3])
End up with exec_str:
my_script_file(1,2)
my_script_file(39,1)
...

The exec_dir is from the header of create_run, where the code should run
The data_dir is also from the header, and used to create save_file, where the data is stored
run_id is 555/etc
job_id is 1...50*3 , whatever the number of combinations are


Using this you should be able to create a call (if not to octave, to python, etc) repetitively
If you are not using the exec_run in matlab, then you must save your data manually


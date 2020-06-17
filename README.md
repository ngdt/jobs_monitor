**chkjob** is a command line application written in Shell based on **qstat** for monitoring jobs for SGE QSUB.

## Problem

**qstat** does not show the full path of the jobs.

```
$ qstat -u username

                                                            Req'd  Req'd   Elap
Job ID          Username Queue    Jobname    SessID NDS TSK Memory Time  S Time
--------------- -------- -------- ---------- ------ --- --- ------ ----- - -----
4170003.tsurugi xyz      qM       Nb@oG14     32635  36 864 4464gb 48:00 R 06:41
```

## Resolve and Usage
```
$ chkjob
```

	+------------+-----------------+---------+---------+
	| queue name | submitting jobs | running | waiting |
	+------------+-----------------+---------+---------+
	|    qM      |       2         |    2    |    -    |
	|    qS      |       -         |    -    |    -    |
	|    qA      |       -         |    -    |    -    |
	|    qD      |       -         |    -    |    -    |
	|    qL      |       -         |    -    |    -    |
	+------------+-----------------+---------+---------+
	                                                            Req'd  Req'd   Elap
	    Job ID          Username Queue    Jobname    SessID NDS TSK Memory Time  S Time
	    --------------- -------- -------- ---------- ------ --- --- ------ ----- - -----
     1  4170000.tsurugi username qM       test        25511   1  24  124gb 48:00 R 00:02
        cd /home/username/work/STO/charg_1/job_1
        +------------------------------------------------------------------------------+
     2  4170001.tsurugi username qM       test        21490   1  24  124gb 48:00 R 00:01
        cd /home/username/work/STO/charg_2/job_2
        +------------------------------------------------------------------------------+

## Installation

```
$ git clone https://github.com/ngoducthien/chkjob.git
```

* Modify field '**user**' in the file chkjob

* Upload to **/bin** directory on your supercomputer server

```
$ cd bin
$ chmod u+x chkjob
```

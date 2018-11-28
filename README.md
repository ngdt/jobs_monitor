**chkjob** is a command line application written in Shell based on **qstat** for monitoring jobs on NIMS supercomputer (Tsukuba, Japan).

## Problem

**qstat** does not show the full path of the jobs.

```
$ qstat -u username

                                                            Req'd  Req'd   Elap
Job ID          Username Queue    Jobname    SessID NDS TSK Memory Time  S Time
--------------- -------- -------- ---------- ------ --- --- ------ ----- - -----
4172355.tsurugi xyz      qM       Nb@oG14     32635  36 864 4464gb 48:00 R 06:41
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
     1  4172680.tsurugi username qM       test        25511   1  24  124gb 48:00 R 00:02
        cd /home/username/work/STO/charged/mo_c
        +------------------------------------------------------------------------------+
     2  4172681.tsurugi username qM       test        21490   1  24  124gb 48:00 R 00:01
        cd /home/username/work/STO/charged5/w_c
        +------------------------------------------------------------------------------+

## Installation

```
$ git clone https://github.com/thienducngo/chkjob.git

Upload to /bin directory on NIMS supercomputer server

$ cd bin
$ chmod u+x chkjob
```

## Lisense
MIT

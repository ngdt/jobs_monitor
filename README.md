# chkjobs
Jobs monitor for NIMS supercomputer

**Default command**

> qstat -u username

```
                                                            Req'd  Req'd   Elap
Job ID          Username Queue    Jobname    SessID NDS TSK Memory Time  S Time
--------------- -------- -------- ---------- ------ --- --- ------ ----- - -----
4172355.tsurugi xyz      qM       Nb@oG14     32635  36 864 4464gb 48:00 R 06:41
```

**New style**

> my_jobs

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

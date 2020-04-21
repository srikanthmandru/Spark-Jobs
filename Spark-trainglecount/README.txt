
Spark Jobs for HW3- SPRING 2020 semester

Code author
-----------
Srikanth Babu Mandru

Execution
---------
All of the build & execution commands are organized in the Makefile.
1) Unzip project file.
2) Open command prompt.
3) Navigate to directory where project files unzipped.
4) Edit the Makefile to customize the environment at the top.
	Sufficient for standalone: hadoop.root, jar.name, local.input

Set "local.option_or_max" = max_filter value for filtering edges

Set "jar.name" accordingly for running correct program. I mentioned jar.name for different programs below in this file.

	Other defaults acceptable for running standalone.
5) Standalone Hadoop:
	make switch-standalone		-- set standalone Hadoop environment (execute once)
	make local
6) Pseudo-Distributed Hadoop: (https://hadoop.apache.org/docs/current/hadoop-project-dist/hadoop-common/SingleCluster.html#Pseudo-Distributed_Operation)
	make switch-pseudo			-- set pseudo-clustered Hadoop environment (execute once)
	make pseudo					-- first execution
	make pseudoq				-- later executions since namenode and datanode already running 
7) AWS EMR Hadoop: (you must configure the emr.* config parameters at top of Makefile)
	make upload-input-aws		-- only before first execution
	make aws					-- check for successful execution with web interface (aws.amazon.com)
	download-output-aws			-- after successful execution & termination





Input:
-------------------------
For input, Create "input" directory and place the dataset into that directory for execution



Log files description:
-------------------------
Log files are provided in "HW3/logs/" directory. I have printed the output "number of triangles" and "number of PATH2" in the syslog files (named as "* from container").


Report file :
-------------------------
Report is placed at "HW3/Srikanth_Mandru_HW3.pdf"


Output file description:
-------------------------
For the output files, I have included in HW3/output/


jar.name :
---------------------------

For twitter follower spark/scala programs:

wc.FollowerCount_RDDG - For running, Follower count program in "RDD-G" configuration

wc.FollowerCount_RDDR - For running, Follower count program in "RDD-R" configuration

wc.FollowerCount_RDDF - For running, Follower count program in "RDD-F" configuration

wc.FollowerCount_RDDA - For running, Follower count program in "RDD-A" configuration

wc.FollowerCount_DSET - For running, Follower count program in "DSET" configuration


For twitter triangles spark/scala programs execution:

wc.TriangleCount_RSR - For running, Follower count program in "RS-R" configuration\

wc.TriangleCount_RSD - For running, Follower count program in "RS-D" configuration

wc.TriangleCount_RepR - For running, Follower count program in "Rep-R" configuration

wc.TriangleCount_RepD - For running, Follower count program in "Rep-D" configuration







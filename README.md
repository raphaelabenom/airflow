# Apache Airflow
<p>Apache Airflow™ is an open-source platform for developing, scheduling, and monitoring batch-oriented workflows.</p> 

# Core components
- ***Web server:*** Flask server with gunicorn serving the UI
- ***Scheduler:*** Daemon in charge of scheduling workflows
- ***Metastore:*** Database where metastore are stored
- ***Triggerer:*** Manager deferrable operators
- ***Executor:*** Class defining how your tasks should be executed
- ***Worker:*** Process/subprocess executing your task


## Secrets webserver and the scheduler
With the Scheduler:

***min_file_process_interval***

Number of seconds after which a DAG file is parsed. The DAG file is parsed every ***min_file_process_interval*** number of seconds. Updates to DAGs are reflected after this interval.

***dag_dir_list_interval***

How often (in seconds) to scan the DAGs directory for new files. Default to 5 minutes.

Those 2 settings tell you that you have to wait up 5 minutes before your DAG gets detected by the scheduler and then it is parsed every 30 seconds by default.
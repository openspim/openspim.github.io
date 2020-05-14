### File Commands

| ls              | directory listing                                                                                            |
| :-------------- | ------------------------------------------------------------------------------------------------------------ |
| ls -al          | formatted listing with hidden files                                                                          |
| cd dir          | change directory to *dir*                                                                                    |
| cd              | change to home                                                                                               |
| pwd             | show current directory                                                                                       |
| mkdir dir       | create a directory *dir*                                                                                     |
| rm file         | delete *file*                                                                                                |
| rm -r dir       | delete directory *dir*                                                                                       |
| rm -f file      | force remove *file*                                                                                          |
| rm -rf dir      | force remove directory *dir* (\!)                                                                            |
| cp file1 file2  | copy *file1* to *file2*                                                                                      |
| cp -r dir1 dir2 | copy *dir1* to *dir2*; create *dir2* if it doesn't exist                                                     |
| mv file1 file2  | rename or move *file1* to *file2*; if *file2* is an existing directory, moves *file1* into directory *file2* |
| ln -s file link | create symbolic link *link* to *file*                                                                        |
| touch file      | create or update *file*                                                                                      |
| cat \> file     | places standard input into *file*                                                                            |
| more file       | output the contents of *file*                                                                                |
| head file       | output the first 10 lines of *file*                                                                          |
| tail file       | output the last 10 lines of *file*                                                                           |
| tail -f file    | output the contents of *file* as it grows, starting with the last 10 lines                                   |

### Process Management

| ps           | display your currently active processes                                  |
| :----------- | ------------------------------------------------------------------------ |
| top          | display all running processes                                            |
| kill pid     | kill process id *pid*                                                    |
| killall proc | kill all processes named *proc* (\!)                                     |
| bg           | lists stopped or background jobs; resume a stopped job in the background |
| fg           | brings the most recent job to foreground                                 |
| fg n         | brings job *n* to the foreground                                         |

### File Permissions

| chmod <symbol> file        | change the permissions of *file* to *<symbol>*; the format of a *<symbol>* is `[ugoa...][[+-=][perms...]...]`, where perms is either zero or more letters from the set `rwxXst`, or a single letter from the set `ugo`. ,see *man chmod* for further details |
| :------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| chmod a+rwx file           | change the permissions of *file* to *rwx* for everyone                                                                                                                                                                                                       |
| chmod u=rwx,g=rx,o=rx file | change the permissions of *file* to *rwx* for owner, and *rx* for group and world                                                                                                                                                                            |

### Working Remotely

| ssh user@host                   | securely connect to remote host *host* as user *user*                                                                        |
| :------------------------------ | ---------------------------------------------------------------------------------------------------------------------------- |
| scp user@host:/home/user/file . | securely copy file /home/user/file on remote host *host* (as user *user*) to the current directory                           |
| scp file user@host:/home/user/  | securely copy (as user *user*) the file file in the current directory to the directory /home/user/ on the remote host *host* |

### LSF Job Submission and Monitoring

| bjobs                             | view status of all jobs currently submitted by user                                                         |
| :-------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| bjobs -q name                     | view status of all jobs currently submitted by user to queue *name*                                         |
| bjobs -r                          | view status of all running jobs submitted by user                                                           |
| bqueues                           | view status of of all queues in the batch system                                                            |
| bsub -q qname command             | submit the *command* to queue *qname* (*command* may contain flags, options and arguments)                  |
| bsub -q qname -J my\_name command | submit the *command* to queue *qname* given the name *my\_name*                                             |
| bsub -q qname -o file command     | submit the *command* to queue *qname*, LSF will write all command line output (stderr and stdout) to *file* |
| bsub \< file                      | submit a job by reading the contents of *file*                                                              |
| bkill jobid                       | kill the job with ID *jobid* by the current user                                                            |
| bkill 0                           | kill all jobs submitted by the current user                                                                 |
| bpeek pid                         | monitor job *pid* state                                                                                     |
| bpeek -f pid                      | real time monitor job *pid* state                                                                           |

=== File Commands ===

{|
!align=left|ls
|directory listing
|-
!align=left|ls -al
|formatted listing with hidden files
|-
!align=left|cd dir
|change directory to ''dir''
|-
!align=left|cd
|change to home
|-
!align=left|pwd
|show current directory
|-
!align=left|mkdir dir
|create a directory ''dir''
|-
!align=left|rm file
|delete ''file''
|-
!align=left|rm -r dir
|delete directory ''dir''
|-
!align=left|rm -f file
|force remove ''file''
|-
!align=left|rm -rf dir
|force remove directory ''dir'' (!)
|-
!align=left|cp file1 file2
|copy ''file1'' to ''file2''
|-
!align=left|cp -r dir1 dir2
|copy ''dir1'' to ''dir2''; create ''dir2'' if it doesn't exist
|-
!align=left|mv file1 file2
|rename or move ''file1'' to ''file2''; if ''file2'' is an existing directory, moves ''file1'' into directory ''file2''
|-
!align=left|ln -s file link
|create symbolic link ''link'' to ''file''
|-
!align=left|touch file
|create or update ''file''
|-
!align=left|cat > file
|places standard input into ''file''
|-
!align=left|more file
|output the contents of ''file''
|-
!align=left|head file
|output the first 10 lines of ''file''
|-
!align=left|tail file
|output the last 10 lines of ''file''
|-
!align=left|tail -f file
|output the contents of ''file'' as it grows, starting with the last 10 lines
|}

=== Process Management ===

{|
!align=left|ps
|display your currently active processes
|-
!align=left|top
|display all running processes
|-
!align=left|kill pid
|kill process id ''pid''
|-
!align=left|killall proc
|kill all processes named ''proc'' (!)
|-
!align=left|bg
|lists stopped or background jobs; resume a stopped job in the background
|-
!align=left|fg
|brings the most recent job to foreground
|-
!align=left|fg n
|brings job ''n'' to the foreground
|}

=== File Permissions ===

{|
!align=left|chmod <symbol> file
|change the permissions of ''file'' to ''<symbol>''; the  format of a ''<symbol>'' is <tt>[ugoa...][[+-=][perms...]...]</tt>, where perms is either zero or more letters from the set <tt>rwxXst</tt>, or a single letter from the set  <tt>ugo</tt>. ,see ''man chmod'' for further details
|-
!align=left|chmod a+rwx file
|change the permissions of ''file'' to ''rwx'' for everyone
|-
!align=left|chmod u=rwx,g=rx,o=rx file
|change the permissions of ''file'' to ''rwx'' for owner, and ''rx'' for group and world
|}

=== Working Remotely ===

{|
!align=left|ssh user@host
|securely connect to remote host ''host'' as user ''user''
|-
!align=left|scp user@host:/home/user/file .
|securely copy file /home/user/file on remote host ''host'' (as user ''user'') to the current directory
|-
!align=left|scp file user@host:/home/user/
|securely copy (as user ''user'') the file file in the current directory to the directory /home/user/ on the remote host ''host''
|}

=== LSF Job Submission and Monitoring ===

{|
!align=left|bjobs
|view status of all jobs currently submitted by user
|-
!align=left|bjobs -q name
|view status of all jobs currently submitted by user to queue ''name''
|-
!align=left|bjobs -r
|view status of all running jobs  submitted by user
|-
!align=left|bqueues
|view status of of all queues in the batch system 
|-
!align=left|bsub -q qname command
|submit the ''command'' to queue ''qname'' (''command'' may contain flags, options and arguments)
|-
!align=left|bsub -q qname -J my_name command
|submit the ''command'' to queue ''qname'' given the name ''my_name'' 
|-
!align=left|bsub -q qname -o file command
|submit the ''command'' to queue ''qname'', LSF will write all command line output (stderr and stdout) to ''file'' 
|-
!align=left|bsub < file
|submit a job by reading the contents of ''file''
|-
!align=left|bkill jobid
|kill the job with ID ''jobid'' by the current user
|-
!align=left|bkill 0
|kill all jobs submitted by the current user
|-
!align=left|bpeek pid
|monitor job ''pid'' state
|-
!align=left|bpeek -f pid
|real time monitor job ''pid'' state
|}

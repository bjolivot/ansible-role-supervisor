supervisor
==========

Deploy supervisor and add command to be managed by.


Role Variables
--------------

Mandatory vars: 
 - sv_program_name: will be used to define your program in supervisor
 - sv_user_name: user executing the task in supervisor
 - sv_command: command to be executed
 - sv_log_dir: log directory
 


 Default vars:
  - sv_umask: 0002      #umask of the user
  - sv_autostart: true   
  - sv_autorestart: true 
  - sv_stderr_logfile: /{{sv_user_name}}/log/{{sv_program_name}}.supervisor.err.log
  - sv_stdout_logfile: /{{sv_user_name}}/log/{{sv_program_name}}.supervisor.out.log
  - sv_environment: "" 
  - sv_apt_update_cache: true
  - sv_apt_cache_lifetime: 3600


How to use 
----------

    - hosts: server
      roles:
         - supervisor

License
-------

Licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


Author Information
------------------

See my other "work on my computer" ansible things on https://www.github.com/bjolivot


pm2_nagios
==========

Nagios plugin for pm2 checking

# Examples

Command defintion

    define command {
      command_name check_pm2
      command_line $USER1$/check_pm2 --host=$HOSTADDRESS$ --name=$1
    }

Nagios service example check for a service named hello_world

    define service{
      use tech-service
      host_name server1,server2,server_n
      service_description node.js pm2 - hello_world
      check_command check_pm2!hello world
    }

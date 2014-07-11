pm2_nagios
==========

Nagios plugin for pm2 checking

# Examples

Command defintion of a service named hello_world

`define command {
  command_name check_pm2
  command_line $USER1$/check_pm2 --host=$HOSTADDRESS --name=hello_world
}`

Nagios service example check for a service named hello_world

`define service{
  use tech-service
  host_name server_name
  service_description pm2 hello_world
  check_command check_pm2
}`

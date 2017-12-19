# check_symlink Plugin for Icinga

You can "install" this plugin by placing it anywhere you want.
If you use the nagios-plugins, the best place might be at 
/usr/lib/nagios/plugins/ or /usr/local/nrpe/libexec/

***Make sure the Plugin is executeable:***

```chmod +x check_symlink```

***Possible NRPE command:***

```command[check_symlink]=/usr/local/nrpe/libexec/check_symlink -s /my/symlink```

***Possible Service***

```
apply Service "check symlink" {
  import "generic-service"
  display_name = "Check Symlink"
  check_command = "check_nrpe"
  vars.sla = host.vars.sla
  vars.nrpe_command = "check_symlink"
  vars.alarm = "no"
  assign where match("*symlink*", host.vars.services)
}
```

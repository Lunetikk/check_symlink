check_symlink Plugin for Icinga

You can "install" this plugin by placing it anywhere you want.
If you use the nagios-plugins, the best place might be at 
/usr/lib/nagios/plugins/ or /usr/local/nrpe/libexec/

Make sure the Plugin is executeable: chmod +x check_symlink

Possible NRPE command:
command[check_symlink]=/usr/local/nrpe/libexec/check_symlink -s /my/symlink

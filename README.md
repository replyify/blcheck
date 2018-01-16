# blcheck

A powerful script for testing a domain or an IP against mailing black lists.  
Script will use dig if it is found. If dig is not found script will use host.


Features
--------------------

* More then __100 black lists__ already included!
* Automatic distinction between __domain or IP__
* Performs __PTR validation__ (only if domain is supplied, does not work for IP)
* 3 verbose (-v) levels and a quiet (-q) mode
* The result of script is the number of servers which blacklisted the domain, so it can be used for any kind of __automated scripts or cronjobs__
* Informative and pleasant output


Requirements
--------------------

* Any Unix/Linux with POSIX shell.
* Either dig or host command available.


Usage
--------------------

blcheck [options] <domain\_or\_IP>

Supplied domain must be full qualified domain name.  
If the IP is supplied, the PTR check cannot be executed and will be skipped.

-d dnshost  Use host as DNS server to make lookups  
-l file     Load blacklists from file, separated by space or new line  
-c          Warn if the top level domain of the blacklist has expired  
-v          Verbose mode, can be used multiple times (up to -vvv)  
-q          Quiet modem with absolutely no output (useful for scripts)  
-p          Plain text output (no coloring, no interactive status)  
-h          The help you are just reading  

Result of the script is the number of blacklisted entries. So if the supplied
IP is not blacklisted on any of the servers the result is 0.


TODO
--------------------
1. Handle domains with multiple DNS entries.


Credits
--------------------
Script has been written by the [Intellex](http://intellex.rs/en) team.  
Contributors:
	[Darko Poljak](https://github.com/darko-poljak)



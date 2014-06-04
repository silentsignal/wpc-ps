Windows Privesc Check - Powershell 
==================================

After trying to fix the code of the original Windows Privesc Check tool and crying rivers of blood I decided to look for a more appropriate tool for the task. This is an experiment to implement similar functionality in Powershell, that is available by default in every Windows installation since Windows 7/Server 2008 R2. 

This is my first Powershell project, but I still hope that my code will be better than the monolithic Python-Pyinstaller-ASCIIonly predecessor. Pull requests/Issue reports are welcome of course.

Current functionality
---------------------

* Check insecure permissions on
  * Service binaries
  * Directories in %PATH%
  * Files under %SYSTEMROOT%
  * Service related registry keys

TODO
----

I just try to list the most important things here:

* Checks for DLL hijacking (will need PowerShell [PETools](https://github.com/mattifestation/PowerSploit/tree/master/PETools))
* Checks for [Group Policy Preferences](http://rewtdance.blogspot.hu/2012/06/exploiting-windows-2008-group-policy.html)
* Checks for [Unattended.xml](http://rewtdance.blogspot.hu/2012/11/windows-deployment-services-clear-text.html)
* Checks for unquoted service binary paths
* Checks for registry key linking
* Checks for Autorun and Startup scripts
* Password policy checks

Similar tools
-------------

Similar functionality is implemented by the following tools:

* [Windows Privesc Check](https://code.google.com/p/windows-privesc-check/)
  * No unicode support ([attempt to fix this](https://github.com/silentsignal/wpc))
  * Awful code base
* [Windows Privesc Check 2.0](https://github.com/silentsignal/wpc/tree/wpc-2.0)
  * Code is still very hard to maintain
  * Still painful to use on non-English systems
* [PowerUp](https://github.com/HarmJ0y/PowerUp)
  * Smart PowerShell cmdlets
  * Offensive approach
  * Checks only the privileges of the executing user

Thanks
------

[@andrew\_kabai](https://twitter.com/andrew_kabai) for pointing me to PowerUp

[@Carlos\_Perez](https://twitter.com/Carlos_Perez) for his fine tutorials: http://www.darkoperator.com/powershellbasics/

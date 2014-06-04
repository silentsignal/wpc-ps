Windows Privesc Check - Powershell version
==========================================

After trying to fix the code of the original Windows Privesc Check tool and crying rivers of blood I decided to look for a more appropriate tool for the task. This is a try implementing similar functionality in Powershell, that is available by default in every Windows installation since Windows 7/Server 2008 R2. 

This is my first Powershell project, but I still hope that my code will be better than the monolithic Python-Pyinstaller-ASCIIonly predecessor.

Similar tools
-------------

Similar functionality is implemented by the following tools:

* [Windows Privesc Check](https://code.google.com/p/windows-privesc-check/)
  * No unicode support ([attempt to fix this](https://github.com/silentsignal/wpc))
  * Awful code base
* [Windows Privesc Check 2.0](https://github.com/silentsignal/wpc/tree/wpc-2.0)
  * Still painful to use on non-English systems
* PowerUp
  * Smart PowerShell cmdlets
  * Offensive approach
  * Checks only the privileges of the executing user

Thanks
------

[@andrew\_kabai](https://twitter.com/andrew_kabai) for pointing me to PowerUp

[@Carlos\_Perez](https://twitter.com/Carlos_Perez) for his fine tutorials: http://www.darkoperator.com/powershellbasics/

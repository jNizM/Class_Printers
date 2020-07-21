# Class_Printers
 AutoHotkey wrapper for Print Spooler API Functions


## Examples

**Retrieves the printer name of the default printer for the current user on the local computer.**
```AutoHotkey
MsgBox % Printers.GetDefault()
```

**Sets the printer name of the default printer for the current user on the local computer.**
```AutoHotkey
Printers.SetDefault("\\192.168.10.1\PRINTER_A")
```

**Adds a connection to the specified printer for the current user.**
```AutoHotkey
Printers.AddConnection("\\192.168.10.1\PRINTER_A")
```

**Deletes a connection to a printer that was established by a call to AddPrinterConnection or ConnectToPrinterDlg.**
```AutoHotkey
Printers.DeleteConnection("\\192.168.10.1\PRINTER_A")
```

**Deletes the specified printer object.**
```AutoHotkey
Printers.Delete("HP DeskJet")
```

**Enumerates available printers, print servers, domains, or print providers.**
```AutoHotkey
; 0x2 -> LOCAL | 0x4 -> CONNECTIONS
for k, v in Printers.Enum(0x2|0x4)
    MsgBox % v.PrinterName
```

**Retrieves information about a specified printer.**
```AutoHotkey
MsgBox % Printers.GetInfo("\\192.168.10.1\PRINTER_A").Location
```


## Questions / Bugs / Issues
Report any bugs or issues on the [AHK Thread](https://www.autohotkey.com/boards/viewtopic.php?f=6&t=62955). Same for any questions.


## Copyright and License
[The Unlicense](LICENSE)


## Donations (PayPal)
[Donations are appreciated if I could help you](https://www.paypal.me/smithz)
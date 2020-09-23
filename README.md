<div align="center">

## getstr


</div>

### Description

If an alphanumeric string is provided in the form 123,33,44,556 , my function

seperates the numbers seperated by any character in this case a (,)comma so we get num1=123 , num2 = 33 , num3=44 and so on.The function uses an array to store

these numbers.DO mail me on how well this code works.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Pratim Guha Biswas](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/pratim-guha-biswas.md)
**Level**          |Unknown
**User Rating**    |4.7 (14 globes from 3 users)
**Compatibility**  |VB 3\.0, VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[String Manipulation](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/string-manipulation__1-5.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/pratim-guha-biswas-getstr__1-1858/archive/master.zip)

### API Declarations

```
Dim saved As String
Dim counted, def, i, res As Integer
Dim arr(20) ' This array holds the seperated numbers
```


### Source Code

```
Sub getstr()
saved = "123,45,6789,99" 'save contents of string to a variable
i = 1      ' Counter variable for array
       'location identifiers for comma
res = 1
def = 1
'loop to seperate sub-string numbers from string
Do While res > 0 ' loop until no comma is found
res = InStr(def, saved, ",")
If InStr(def + 1, saved, ",") = 0 Then
counted = Len(saved)
Else
counted = InStr(def + 1, saved, ",") - def
End If
arr(i) = Mid(saved, def, counted)
label1.Caption = Str(res)
def = res + 1
i = i + 1
Loop
label1.Caption = "The numbers are "
Do While i > 0
label1.Caption = label1.Caption + " " + arr(i)
i = i - 1
Loop
' The numbers are stored in Array { arr(i) }
End Sub
```


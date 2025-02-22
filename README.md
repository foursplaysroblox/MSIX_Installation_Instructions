# MSIX Installation Instructions (FIle Explorer Properties Method)
Instructions for MSIX Bundle / AppxBundle install
Windows Prompts an error saying that app is untrusted what should you do?

1. Right click the msix file / AppxBundle and click properties
2. Go to the digital certificates tab
3. then select the name of the software dev ![image](https://user-images.githubusercontent.com/82078139/226300901-52bb44d8-9c80-47cb-be0a-e502832c1c15.png)
4. Next pop up screen select view certificates
5. Next pop up screen click "Install Certificate"
6. Click local machine once it shows (UAC prompt click "yes")
7. select place all certificates in following store then click browse then select trusted people
8. click ok and then next
9. click on that msix / AppxBundle app you want to install

# MSIX Installation Instructions (Powershell Unsigned Method)
If you do not like doing the first method above or the certificate expired maybe this method would work for you
Instructions
1. Click the msix file you want to install and copy the file location of it (you will need it later)
2. Go to the Windows search area and search "Powershell" this can be legacy Powershell (Default) or Powershell 7 ![tutorial](https://github.com/user-attachments/assets/e4ad209e-494a-4214-9bd4-62b62a7158bd)
3. copy this NOTE: Replace the C:\Path\to\File.AppxBundle with the file path DO NOT renove the quotation marks
```sh
Add-AppxPackage -Path "C:\Path\to\File.AppxBundle" -AllowUnsigned
```
4. Paste the command
5. Go back to the msix or AppxBundle file in your file manager and click it to install it.

That ends the tutorial! Write an issue if you need help or found another method to install MSIX Bundle / AppxBundle files

Credits: 
[Rise-Software](https://github.com/Rise-Software/Rise-Media-Player) 

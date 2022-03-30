# nim-windows-test
Test repository for playing with Nim with Windows


## Code signing

Generate self-signed certificate in PowerShell:

```powershell
New-SelfSignedCertificate -DnsName email@yourdomain.com -Type CodeSigning -CertStoreLocation cert:\CurrentUser\My
```

Sign using signtool.exe:

```
signtool sign /a test.exe
```

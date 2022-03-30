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
or PowerShell:
```powershell
$cert=Get-ChildItem -Path Cert:\CurrentUser\My -CodeSigningCert
Set-AuthenticodeSignature -FilePath test.exe -Certificate $cert
```

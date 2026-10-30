https://www.microsoft.com/en-us/download/details.aspx?id=49117

++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

New-Item -ItemType Directory -Path "C:\Office2019" -Force | Out-Null

$xml = @'
<Configuration>
  <Add OfficeClientEdition="64" Channel="PerpetualVL2019">
    <Product ID="ProPlus2019Volume">
      <Language ID="fr-fr" />
    </Product>
  </Add>
  <Display Level="Full" AcceptEULA="TRUE" />
</Configuration>
'@

Set-Content -Path "C:\Office2019\configuration.xml" -Value $xml -Encoding UTF8

Get-Content "C:\Office2019\configuration.xml"

++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

cd C:\Office2019
Test-Path "C:\Office2019\setup.exe"


+++++++++++++++++++++++++++++++++


.\setup.exe /download configuration.xml


++++++++++++++++++++++++++++++++++++++++

Get-ChildItem "C:\Office2019\Office" -Recurse |
Select-Object -First 10 FullName

++++

cd C:\Office2019
.\setup.exe /configure configuration.xml

************************************************************************************************







$ProgressPreference = 'SilentlyContinue'
Invoke-WebRequest `
  -Uri "https://dl.google.com/chrome/install/latest/chrome_installer.exe" `
  -OutFile "$env:TEMP\chrome_installer.exe"



Start-Process "$env:TEMP\chrome_installer.exe" -Wait






VBoxManage modifymedium disk "F:\NEWsage\CLONE de sage 200gb\CLONE de sage 200gb.vdi" --resize 204800




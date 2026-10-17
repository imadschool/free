$ProgressPreference = 'SilentlyContinue'
Invoke-WebRequest `
  -Uri "https://dl.google.com/chrome/install/latest/chrome_installer.exe" `
  -OutFile "$env:TEMP\chrome_installer.exe"



Start-Process "$env:TEMP\chrome_installer.exe" -Wait






VBoxManage modifymedium disk "F:\NEWsage\CLONE de sage 200gb\CLONE de sage 200gb.vdi" --resize 204800




$ProgressPreference = 'SilentlyContinue'
Invoke-WebRequest `
  -Uri "https://dl.google.com/chrome/install/latest/chrome_installer.exe" `
  -OutFile "$env:TEMP\chrome_installer.exe"

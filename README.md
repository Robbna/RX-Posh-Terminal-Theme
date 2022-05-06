# :minidisc: Terminal-Icons module (_see icons in the terminal_)
```
Install-Module -Name Terminal-Icons -Repository PSGallery -Force
```
```
Import-Module Terminal-Icons
```
# :minidisc: PSReadLine module (_autocomplete system_)
```
Install-Module -Name PSReadLine -Scope CurrentUser -Force -SkipPublisherCheck
```
```
Set-PSReadLineOption -PredictionSource History
```
```
Set-PSReadLineOption -PredictionViewStyle ListView
```
# :pencil: Configure $profile
```
# ----------< SET POSH THEME >----------
oh-my-posh init pwsh --config 'https://raw.githubusercontent.com/Robbna/RX-Posh-Terminal-Theme/master/rxMainTheme.json' | Invoke-Expression

# ----------< IMPORTS AND SETTERS >----------
Import-Module Terminal-Icons
Set-PSReadLineOption -PredictionSource History

# ----------< UTILITIES >----------
function which ($command) {
  Get-Command -Name $command -ErrorAction SilentlyContinue |
   Select-Object -ExpandProperty Path -ErrorAction SilentlyContinue
}

oh-my-posh init pwsh | Invoke-Expression
cls
```

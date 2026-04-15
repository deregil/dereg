# Topgrade and PSWindowsUpdate
This directory is configured to use `topgrade` for routine system and tooling updates.

## Enable Windows Update integration in Topgrade
Topgrade uses the `PSWindowsUpdate` PowerShell module to perform the Windows Update step.

Install the module in the current user scope:

```powershell
Install-Module -Name PSWindowsUpdate -Scope CurrentUser -Force -AllowClobber -Confirm:$false
```

## Verify integration
Run Topgrade:

```powershell
topgrade
```

Look for a `Windows Update` section in the output and confirm the summary reports:

- `Windows update: OK`

If no updates are available, Topgrade may report that 0 updates were found, which still indicates successful integration.

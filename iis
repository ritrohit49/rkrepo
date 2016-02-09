$winRmUri = Get-AzureWinRMUri -ServiceName vmtwo -Name vmtwo 
Invoke-Command -ConnectionUri $winRmUri.ToString() -Credential vmtwo\dcadmin -ScriptBlock { 
    Import-Module ServerManager 
    Add-WindowsFeature -Name Web-Server -IncludeManagementTools -IncludeAllSubFeature
    } -Verbose
Wait-Job -State Completed

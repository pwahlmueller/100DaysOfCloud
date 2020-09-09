# Startup
![placeholder image](https://cdna.artstation.com/p/assets/images/images/006/860/916/medium/marc-miquet-grivet-bilbo-ext-fini-photoshope.jpg?1501782354)

# Another day - another Azure Day

## Introduction

Nicht viel heute, nur ein kleines Berechtigugnsskript

### Step 1 — Summary of Step

Owner Rechte auf alle Subscriptions, auf die der aktuell angemeldete User Berechtigungen hat.

```powershell
Connect-AzAccount

$subs=Get-AzSubscription

foreach ($sub in $subs)
{
    Select-AzSubscription $sub
    New-AzRoleAssignment -SignInName <UserName> -RoleDefinitionName <Role>
}
```

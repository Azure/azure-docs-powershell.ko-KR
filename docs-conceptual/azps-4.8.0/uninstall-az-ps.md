---
title: Azure PowerShell 제거
description: Azure PowerShell의 전체 제거를 수행하는 방법
ms.date: 09/15/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ec4ecc9902f700e12ce6b22c32b4e07b13b4d4dc
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407785"
---
# <a name="how-to-uninstall-azure-powershell-modules"></a>Azure PowerShell 모듈을 제거하는 방법

이 문서에서는 Azure PowerShell의 이전 버전을 제거하거나 시스템에서 완전히 제거하는 방법을 알려줍니다. Azure PowerShell을 완전히 제거하기로 한 경우 [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet을 통해 몇 가지 피드백을 보내주세요. 버그가 발생하면 해결을 위해 [GitHub 문제를 제출](https://github.com/azure/azure-powershell/issues)해 주시기 바랍니다.

## <a name="uninstall-the-az-module"></a>Az 모듈 제거

시스템에 Az 모듈이 설치되어 있고 이를 제거하려는 경우 두 가지 옵션이 있습니다. 수행할 방법은 Az 모듈을 설치한 방법에 따라 달라집니다. 원래의 설치 방법을 잘 모르는 경우 먼저 제거를 위해 MSI 단계를 수행합니다.

### <a name="option-1-uninstall-the-az-powershell-module-from-msi"></a>옵션 1: MSI에서 Az PowerShell 모듈 제거

MSI 패키지를 사용하여 Az PowerShell 모듈을 설치한 경우 PowerShell이 아닌 Windows 시스템을 통해 제거해야 합니다.

|         플랫폼         |                      Instructions                      |
| ------------------------ | ------------------------------------------------------ |
| 윈도우 10               | 시작 > 설정 > 앱                                |
| Windows 7 </br>Windows 8 | 시작 > 제어판 > 프로그램 > 프로그램 제거 |

이 화면을 띄우면 프로그램 목록에 **Azure PowerShell** 이 보일 것입니다. 이 앱을 제거하면 됩니다. 이 프로그램이 나열되지 않으면 PowerShellGet을 통해 설치한 후 다음 지침을 따라야 합니다.

### <a name="option-2-uninstall-the-az-powershell-module-from-powershellget"></a>옵션 2: PowerShellGet에서 Az PowerShell 모듈 제거

Az 모듈을 제거하기 위해 [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet을 사용할 수 있습니다. 그러나 `Uninstall-Module`은 모듈 중 하나만 제거합니다. Az PowerShell 모듈을 완전히 제거하려면 각 모듈을 개별적으로 제거해야 합니다. 2개 이상의 Azure PowerShell 버전을 설치한 경우 제거가 복잡할 수 있습니다.

설치한 Az PowerShell 모듈 버전을 확인하려면 다음 명령을 실행합니다.

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

다음 스크립트는 PowerShell 갤러리를 쿼리하여 종속 하위 모듈의 목록을 가져옵니다. 그런 다음 스크립트는 올바른 버전의 각 하위 모듈을 제거합니다. **프로세서** 또는 **현재 사용자** 외의 범위에서 이 스크립트를 실행하려면 관리자 권한이 필요합니다.

```powershell-interactive
function Uninstall-AzModule {
  [CmdletBinding(SupportsShouldProcess)]
  param(
    [ValidateNotNullOrEmpty()]
    [ValidateSet('Az','AzureRM','Azure')]
    [string]$Name = 'Az',

    [Parameter(Mandatory)]
    [string]$Version,

    [switch]$AllowPrerelease
  )

  $Params = @{}

  if ($PSBoundParameters.AllowPrerelease) {
    $Params.AllowPrerelease = $true
  }

  $IsAdmin = ([Security.Principal.WindowsPrincipal] [Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole] 'Administrator')

  if (-not(Get-InstalledModule -Name $Name -RequiredVersion $Version -ErrorAction SilentlyContinue -OutVariable RootModule @Params)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version not found."

  } elseif (($RootModule.InstalledLocation -notlike "*$env:USERPROFILE*") -and ($IsAdmin -eq $false)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version exists in a system path. PowerShell must be run elevated as an admin to remove it."

  } elseif ((Get-Process -Name powershell, pwsh -OutVariable Sessions -ErrorAction SilentlyContinue).Count -gt 1) {

    Write-Warning -Message "Uninstall aborted. Please close all other PowerShell sessions before continuing. There are currently $($Sessions.Count) PowerShell sessions running."

  } else {
    Write-Verbose -Message 'Creating list of dependencies...'
    $target = Find-Module -Name $Name -RequiredVersion $Version @Params

    $AllModules = @([pscustomobject]@{
      Name = $Name
      Version = $Version
    })

    $AllModules += foreach ($dependency in $target.Dependencies) {
      switch ($dependency.keys) {
        {$_ -contains 'RequiredVersion'} {$UninstallVersion = $dependency.RequiredVersion; break}
        {$_ -contains 'MinimumVersion'} {$UninstallVersion = $dependency.MinimumVersion; break}
      }

      [pscustomobject]@{
        Name = $dependency.Name
        Version = $UninstallVersion
      }
    }

    [int]$i = 100 / $AllModules.Count

    foreach ($module in $AllModules) {
      Write-Progress -Activity 'Uninstallation in Progress' -Status "$i% Complete:" -PercentComplete $i
      $i++

      if (Get-InstalledModule -Name $module.Name -RequiredVersion $module.Version -ErrorAction SilentlyContinue @Params) {
        Write-Verbose -Message "Uninstalling $($module.Name) version $($module.Version)"

        Remove-Module -FullyQualifiedName @{ModuleName=$module.Name;ModuleVersion=$module.Version} -ErrorAction SilentlyContinue

        try {
          if ($PSCmdlet.ShouldProcess("$($module.Name) version $($module.Version)")) {
            Uninstall-Module -Name $module.Name -RequiredVersion $module.Version -Force -ErrorAction Stop @Params
          }
          $State = 'Uninstalled'
        } Catch {
          $State = 'Manual uninstall required'
          Write-Verbose -Message "$($module.Name) version: $($module.Version) may require manual uninstallation."
        }

      } else {
        $State = 'Not found'
        Write-Verbose -Message "$($module.Name) version: $($module.Version) not found."
      }

      if (-not $PSBoundParameters.WhatIf) {
        [pscustomobject]@{
          ModuleName = $module.Name
          Version = $module.Version
          State = $State
        }
      }

    }
  }
}
```

이 함수를 사용하려면 코드를 복사하고 PowerShell 세션에 붙여넣습니다. 다음 예제에서는 이전 버전의 Az PowerShell 모듈 및 해당 하위 모듈을 제거하는 함수를 실행하는 방법을 보여 줍니다.

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

이 스크립트를 실행하면 제거하고 있는 각 하위 모듈의 **이름** , **버전** 및 **상태** 가 표시됩니다. 제거하지는 않되, 삭제할 것을 표시만 하도록 스크립트를 실행하려면 `-WhatIf` 매개 변수를 지정합니다.

```output
ModuleName              Version  State
----------              -------  -----
Az.Accounts             1.5.1    Not found
Az.Aks                  1.0.1    Uninstalled
Az.AnalysisServices     1.1.0    Uninstalled
Az.ApiManagement        1.0.0    Uninstalled
Az.ApplicationInsights  1.0.0    Uninstalled
...
```

> [!IMPORTANT]
> 이 스크립트가 제거할 동일한 버전의 정확한 종속성과 매치될 수 없으면 해당 종속성의 _어떠한_ 버전도 제거하지 않습니다. 이는 시스템에 이러한 종속성을 사용하는 대상 모듈의 다른 버전이 있을 수 있기 때문입니다.

제거하려는 Az PowerShell 모듈의 모든 버전에 대해 다음 예제를 실행합니다.
편의를 위해, 다음 스크립트는 최신 버전을 **제외한** 모든 Az 버전을 제거합니다.

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a>AzureRM 모듈을 제거합니다.

시스템에 Az 모듈이 설치되어 있고 AzureRM을 제거하려는 경우 두 가지 옵션이 있습니다. 수행할 방법은 AzureRM 모듈을 설치한 방법에 따라 달라집니다. 원래의 설치 방법을 잘 모르는 경우 먼저 제거를 위해 MSI 단계를 수행합니다.

### <a name="option-1-uninstall-the-azurerm-powershell-module-from-msi"></a>옵션 1: MSI에서 AzureRM PowerShell 모듈 제거

MSI 패키지를 사용하여 AzureRM PowerShell 모듈을 설치한 경우 PowerShell이 아닌 Windows 시스템을 통해 제거해야 합니다.

|         플랫폼         |                      Instructions                      |
| ------------------------ | ------------------------------------------------------ |
| 윈도우 10               | 시작 > 설정 > 앱                                |
| Windows 7 </br>Windows 8 | 시작 > 제어판 > 프로그램 > 프로그램 제거 |

이 화면의 프로그램 목록에서 **Azure PowerShell** 또는 **Microsoft Azure PowerShell - Month Year** 를 확인할 수 있습니다. 이 앱을 제거하면 됩니다. 이 프로그램이 나열되지 않으면 PowerShellGet을 통해 설치한 후 다음 지침을 따라야 합니다.

### <a name="option-2-uninstall-the-azurerm-powershell-module-from-powershellget"></a>옵션 2: PowerShellGet에서 AzureRM PowerShell 모듈 제거

AzureRM을 PowerShellGet과 함께 설치한 경우 `Az.Accounts` 모듈의 일부로 사용할 수 있는 [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet을 사용하여 모듈을 제거할 수 있습니다.

`Az.Accounts` 모듈을 사용하려면 Az 모듈이 설치되어 있어야 합니다.  AzureRM 및 Az 모듈을 동시에 설치하는 것은 지원되지 않지만 Az 모듈을 사용하여 AzureRM 모듈을 즉시 제거할 수 있습니다.  Az 모듈이 설치되어 있지 않은 경우 다음 명령을 사용하여 Az 모듈을 설치하고 AzureRM 모듈 경고를 무시할 수 있습니다.

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

Az 모듈이 설치되면 다음 명령을 사용하여 _모든_ AzureRM 모듈을 머신에서 제거할 수 있습니다. 관리자 권한이 필요합니다.

```powershell-interactive
Uninstall-AzureRm
```

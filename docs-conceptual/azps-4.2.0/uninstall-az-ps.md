---
title: Azure PowerShell 제거
description: Azure PowerShell의 전체 제거를 수행하는 방법
ms.date: 05/28/2020
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 4b40a3aebab84176a48bcdb0ef818cfa05dea269
ms.sourcegitcommit: cef87acc9f2a0d296bef74f526afd2e067e8146b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/02/2020
ms.locfileid: "84294745"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="fbd18-103">Azure PowerShell 모듈 제거</span><span class="sxs-lookup"><span data-stu-id="fbd18-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="fbd18-104">이 문서에서는 Azure PowerShell의 이전 버전을 제거하거나 시스템에서 완전히 제거하는 방법을 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="fbd18-105">Azure PowerShell을 완전히 제거하기로 한 경우 [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet을 통해 몇 가지 피드백을 보내주세요.</span><span class="sxs-lookup"><span data-stu-id="fbd18-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="fbd18-106">버그가 발생하면 해결을 위해 [GitHub 문제를 제출](https://github.com/azure/azure-powershell/issues)해 주시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-azure-powershell-from-msi"></a><span data-ttu-id="fbd18-107">MSI에서 Azure PowerShell 제거</span><span class="sxs-lookup"><span data-stu-id="fbd18-107">Uninstall Azure PowerShell from MSI</span></span>

<span data-ttu-id="fbd18-108">MSI 패키지를 사용하여 Azure PowerShell을 설치한 경우 PowerShell이 아닌 Windows 시스템을 통해 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="fbd18-109">플랫폼</span><span class="sxs-lookup"><span data-stu-id="fbd18-109">Platform</span></span>         |                      <span data-ttu-id="fbd18-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="fbd18-110">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="fbd18-111">윈도우 10</span><span class="sxs-lookup"><span data-stu-id="fbd18-111">Windows 10</span></span>               | <span data-ttu-id="fbd18-112">시작 > 설정 > 앱</span><span class="sxs-lookup"><span data-stu-id="fbd18-112">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="fbd18-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fbd18-113">Windows 7</span></span> </br><span data-ttu-id="fbd18-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fbd18-114">Windows 8</span></span> | <span data-ttu-id="fbd18-115">시작 > 제어판 > 프로그램 > 프로그램 제거</span><span class="sxs-lookup"><span data-stu-id="fbd18-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="fbd18-116">이 화면을 띄우면 프로그램 목록에 **Azure PowerShell** 이 보일 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-116">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="fbd18-117">이 앱을 제거하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-117">This is the app to uninstall.</span></span> <span data-ttu-id="fbd18-118">이 프로그램이 나열되지 않으면 PowerShellGet을 통해 설치한 후 다음 지침을 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-azure-powershell-from-powershellget"></a><span data-ttu-id="fbd18-119">PowerShellGet에서 Azure PowerShell 제거</span><span class="sxs-lookup"><span data-stu-id="fbd18-119">Uninstall Azure PowerShell from PowerShellGet</span></span>

<span data-ttu-id="fbd18-120">Az 모듈을 제거하기 위해 [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-120">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="fbd18-121">그러나 `Uninstall-Module`은 모듈 중 하나만 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="fbd18-122">Azure PowerShell을 완전히 제거하려면 각 모듈을 개별적으로 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-122">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="fbd18-123">2개 이상의 Azure PowerShell 버전을 설치한 경우 제거가 복잡할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="fbd18-124">설치한 Azure PowerShell 버전을 확인하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-124">To check which versions of Azure PowerShell you've installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<a name="uninstall-script"/>

<span data-ttu-id="fbd18-125">다음 스크립트는 PowerShell 갤러리를 쿼리하여 종속 하위 모듈의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="fbd18-126">그런 다음 스크립트는 올바른 버전의 각 하위 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="fbd18-127">**Process** 또는 **CurrentUser** 외의 범위에서 이 스크립트를 실행하려면 관리자 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-127">You need to have administrator access to run this script in a scope other than **Process** or **CurrentUser**.</span></span>

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

<span data-ttu-id="fbd18-128">이 함수를 사용하려면 코드를 복사하고 PowerShell 세션에 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="fbd18-129">다음 예제에서는 이전 버전의 Azure PowerShell을 제거하는 함수를 실행하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-129">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="fbd18-130">이 스크립트를 실행하면 제거하고 있는 각 하위 모듈의 **이름**, **버전** 및 **상태**가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-130">As the script runs, it displays the **Name**, **Version**, and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="fbd18-131">제거하지는 않되, 삭제할 것을 표시만 하도록 스크립트를 실행하려면 `-WhatIf` 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-131">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

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
> <span data-ttu-id="fbd18-132">이 스크립트가 제거할 동일한 버전의 정확한 종속성과 매치될 수 없으면 해당 종속성의 _어떠한_ 버전도 제거하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="fbd18-133">이는 시스템에 이러한 종속성을 사용하는 대상 모듈의 다른 버전이 있을 수 있기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="fbd18-134">제거하려는 Azure PowerShell의 모든 버전에 대해 다음 예제를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-134">Run the following example for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="fbd18-135">편의를 위해, 다음 스크립트는 최신 버전을 **제외한** 모든 Az 버전을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-135">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions | 
    Sort-Object -Property Version -Descending | 
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="fbd18-136">AzureRM 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-136">Uninstall the AzureRM module</span></span>

<span data-ttu-id="fbd18-137">시스템에 Az 모듈이 설치되어 있고 AzureRM을 제거하려면 위의 `Uninstall-AzModule` 스크립트를 실행하지 않아도 되는 두 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-137">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AzModule` script above.</span></span> <span data-ttu-id="fbd18-138">수행할 방법은 AzureRM 모듈을 설치한 방법에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-138">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="fbd18-139">원래의 설치 방법을 잘 모르는 경우 먼저 MSI를 제거하는 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-139">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="fbd18-140">Azure PowerShell MSI 제거</span><span class="sxs-lookup"><span data-stu-id="fbd18-140">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="fbd18-141">MSI 패키지를 사용하여 Azure PowerShell AzureRM 모듈을 설치한 경우 PowerShell이 아닌 Windows 시스템을 통해 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-141">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="fbd18-142">플랫폼</span><span class="sxs-lookup"><span data-stu-id="fbd18-142">Platform</span></span>         |                      <span data-ttu-id="fbd18-143">Instructions</span><span class="sxs-lookup"><span data-stu-id="fbd18-143">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="fbd18-144">윈도우 10</span><span class="sxs-lookup"><span data-stu-id="fbd18-144">Windows 10</span></span>               | <span data-ttu-id="fbd18-145">시작 > 설정 > 앱</span><span class="sxs-lookup"><span data-stu-id="fbd18-145">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="fbd18-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fbd18-146">Windows 7</span></span> </br><span data-ttu-id="fbd18-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fbd18-147">Windows 8</span></span> | <span data-ttu-id="fbd18-148">시작 > 제어판 > 프로그램 > 프로그램 제거</span><span class="sxs-lookup"><span data-stu-id="fbd18-148">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="fbd18-149">이 화면의 프로그램 목록에서 **Azure PowerShell** 또는 **Microsoft Azure PowerShell - Month Year**를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-149">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="fbd18-150">이 앱을 제거하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-150">This is the app to uninstall.</span></span> <span data-ttu-id="fbd18-151">이 프로그램이 나열되지 않으면 PowerShellGet을 통해 설치한 후 다음 지침을 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-151">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="fbd18-152">PowerShell에서 제거하기</span><span class="sxs-lookup"><span data-stu-id="fbd18-152">Uninstall from PowerShell</span></span>

<span data-ttu-id="fbd18-153">AzureRM을 PowerShellGet과 함께 설치한 경우 `Az.Accounts` 모듈의 일부로 사용할 수 있는 [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet을 사용하여 모듈을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-153">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="fbd18-154">다음 예제는 머신에서 _모든_ AzureRM 모듈을 제거할 수 있지만 관리자 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-154">The following example removes _all_ AzureRM modules from your machine but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="fbd18-155">`Uninstall-AzureRM` 명령을 성공적으로 실행할 수 없으면 이 문서에서 제공하는 [`Uninstall-AzModule` 스크립트](#uninstall-script)를 사용하여 다음과 같이 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd18-155">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AzModule` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name AzureRM -AllVersions
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

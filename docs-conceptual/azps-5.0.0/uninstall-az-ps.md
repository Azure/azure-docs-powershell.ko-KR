---
title: Azure PowerShell 제거
description: Azure PowerShell의 전체 제거를 수행하는 방법
ms.date: 09/15/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 7f831bdf6d6144640e036d72900958847283acf1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753582"
---
# <a name="how-to-uninstall-azure-powershell-modules"></a><span data-ttu-id="38c86-103">Azure PowerShell 모듈을 제거하는 방법</span><span class="sxs-lookup"><span data-stu-id="38c86-103">How to uninstall Azure PowerShell modules</span></span>

<span data-ttu-id="38c86-104">이 문서에서는 Azure PowerShell의 이전 버전을 제거하거나 시스템에서 완전히 제거하는 방법을 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="38c86-105">Azure PowerShell을 완전히 제거하기로 한 경우 [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet을 통해 몇 가지 피드백을 보내주세요.</span><span class="sxs-lookup"><span data-stu-id="38c86-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="38c86-106">버그가 발생하면 해결을 위해 [GitHub 문제를 제출](https://github.com/azure/azure-powershell/issues)해 주시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="38c86-107">Az 모듈 제거</span><span class="sxs-lookup"><span data-stu-id="38c86-107">Uninstall the Az module</span></span>

<span data-ttu-id="38c86-108">시스템에 Az 모듈이 설치되어 있고 이를 제거하려는 경우 두 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-108">If you have the Az module installed on your system and would like to uninstall it, there are two options.</span></span> <span data-ttu-id="38c86-109">수행할 방법은 Az 모듈을 설치한 방법에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-109">Which method you follow depends on how you installed the Az module.</span></span> <span data-ttu-id="38c86-110">원래의 설치 방법을 잘 모르는 경우 먼저 제거를 위해 MSI 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-110">If you're not sure of your original installation method, follow the MSI steps for uninstalling first.</span></span>

### <a name="option-1-uninstall-the-az-powershell-module-from-msi"></a><span data-ttu-id="38c86-111">옵션 1: MSI에서 Az PowerShell 모듈 제거</span><span class="sxs-lookup"><span data-stu-id="38c86-111">Option 1: Uninstall the Az PowerShell module from MSI</span></span>

<span data-ttu-id="38c86-112">MSI 패키지를 사용하여 Az PowerShell 모듈을 설치한 경우 PowerShell이 아닌 Windows 시스템을 통해 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-112">If you installed Az PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="38c86-113">플랫폼</span><span class="sxs-lookup"><span data-stu-id="38c86-113">Platform</span></span>         |                      <span data-ttu-id="38c86-114">Instructions</span><span class="sxs-lookup"><span data-stu-id="38c86-114">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="38c86-115">윈도우 10</span><span class="sxs-lookup"><span data-stu-id="38c86-115">Windows 10</span></span>               | <span data-ttu-id="38c86-116">시작 > 설정 > 앱</span><span class="sxs-lookup"><span data-stu-id="38c86-116">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="38c86-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="38c86-117">Windows 7</span></span> </br><span data-ttu-id="38c86-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="38c86-118">Windows 8</span></span> | <span data-ttu-id="38c86-119">시작 > 제어판 > 프로그램 > 프로그램 제거</span><span class="sxs-lookup"><span data-stu-id="38c86-119">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="38c86-120">이 화면을 띄우면 프로그램 목록에 **Azure PowerShell** 이 보일 것입니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-120">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="38c86-121">이 앱을 제거하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-121">This is the app to uninstall.</span></span> <span data-ttu-id="38c86-122">이 프로그램이 나열되지 않으면 PowerShellGet을 통해 설치한 후 다음 지침을 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-122">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="option-2-uninstall-the-az-powershell-module-from-powershellget"></a><span data-ttu-id="38c86-123">옵션 2: PowerShellGet에서 Az PowerShell 모듈 제거</span><span class="sxs-lookup"><span data-stu-id="38c86-123">Option 2: Uninstall the Az PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="38c86-124">Az 모듈을 제거하기 위해 [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-124">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="38c86-125">그러나 `Uninstall-Module`은 모듈 중 하나만 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-125">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="38c86-126">Az PowerShell 모듈을 완전히 제거하려면 각 모듈을 개별적으로 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-126">To remove the Az PowerShell module completely, you must uninstall each module individually.</span></span> <span data-ttu-id="38c86-127">2개 이상의 Azure PowerShell 버전을 설치한 경우 제거가 복잡할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-127">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="38c86-128">설치한 Az PowerShell 모듈 버전을 확인하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-128">To check which versions of the Az PowerShell module you've installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<span data-ttu-id="38c86-129">다음 스크립트는 PowerShell 갤러리를 쿼리하여 종속 하위 모듈의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-129">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="38c86-130">그런 다음 스크립트는 올바른 버전의 각 하위 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-130">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="38c86-131">**프로세서** 또는 **현재 사용자** 외의 범위에서 이 스크립트를 실행하려면 관리자 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-131">You need to have administrator access to run this script in a scope other than **Process** or **Current User** .</span></span>

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

<span data-ttu-id="38c86-132">이 함수를 사용하려면 코드를 복사하고 PowerShell 세션에 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-132">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="38c86-133">다음 예제에서는 이전 버전의 Az PowerShell 모듈 및 해당 하위 모듈을 제거하는 함수를 실행하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-133">The following example shows how to run the function to remove an older version of the Az PowerShell module and its submodules.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="38c86-134">이 스크립트를 실행하면 제거하고 있는 각 하위 모듈의 **이름** , **버전** 및 **상태** 가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-134">As the script runs, it displays the **Name** , **Version** , and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="38c86-135">제거하지는 않되, 삭제할 것을 표시만 하도록 스크립트를 실행하려면 `-WhatIf` 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-135">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

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
> <span data-ttu-id="38c86-136">이 스크립트가 제거할 동일한 버전의 정확한 종속성과 매치될 수 없으면 해당 종속성의 _어떠한_ 버전도 제거하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-136">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="38c86-137">이는 시스템에 이러한 종속성을 사용하는 대상 모듈의 다른 버전이 있을 수 있기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-137">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="38c86-138">제거하려는 Az PowerShell 모듈의 모든 버전에 대해 다음 예제를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-138">Run the following example for every version of the Az PowerShell module that you want to uninstall.</span></span>
<span data-ttu-id="38c86-139">편의를 위해, 다음 스크립트는 최신 버전을 **제외한** 모든 Az 버전을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-139">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="38c86-140">AzureRM 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-140">Uninstall the AzureRM module</span></span>

<span data-ttu-id="38c86-141">시스템에 Az 모듈이 설치되어 있고 AzureRM을 제거하려는 경우 두 가지 옵션이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-141">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options.</span></span> <span data-ttu-id="38c86-142">수행할 방법은 AzureRM 모듈을 설치한 방법에 따라 달라집니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-142">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="38c86-143">원래의 설치 방법을 잘 모르는 경우 먼저 제거를 위해 MSI 단계를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-143">If you're not sure of your original installation method, follow the MSI steps for uninstalling first.</span></span>

### <a name="option-1-uninstall-the-azurerm-powershell-module-from-msi"></a><span data-ttu-id="38c86-144">옵션 1: MSI에서 AzureRM PowerShell 모듈 제거</span><span class="sxs-lookup"><span data-stu-id="38c86-144">Option 1: Uninstall the AzureRM PowerShell module from MSI</span></span>

<span data-ttu-id="38c86-145">MSI 패키지를 사용하여 AzureRM PowerShell 모듈을 설치한 경우 PowerShell이 아닌 Windows 시스템을 통해 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-145">If you installed the AzureRM PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="38c86-146">플랫폼</span><span class="sxs-lookup"><span data-stu-id="38c86-146">Platform</span></span>         |                      <span data-ttu-id="38c86-147">Instructions</span><span class="sxs-lookup"><span data-stu-id="38c86-147">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="38c86-148">윈도우 10</span><span class="sxs-lookup"><span data-stu-id="38c86-148">Windows 10</span></span>               | <span data-ttu-id="38c86-149">시작 > 설정 > 앱</span><span class="sxs-lookup"><span data-stu-id="38c86-149">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="38c86-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="38c86-150">Windows 7</span></span> </br><span data-ttu-id="38c86-151">Windows 8</span><span class="sxs-lookup"><span data-stu-id="38c86-151">Windows 8</span></span> | <span data-ttu-id="38c86-152">시작 > 제어판 > 프로그램 > 프로그램 제거</span><span class="sxs-lookup"><span data-stu-id="38c86-152">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="38c86-153">이 화면의 프로그램 목록에서 **Azure PowerShell** 또는 **Microsoft Azure PowerShell - Month Year** 를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-153">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="38c86-154">이 앱을 제거하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-154">This is the app to uninstall.</span></span> <span data-ttu-id="38c86-155">이 프로그램이 나열되지 않으면 PowerShellGet을 통해 설치한 후 다음 지침을 따라야 합니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-155">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="option-2-uninstall-the-azurerm-powershell-module-from-powershellget"></a><span data-ttu-id="38c86-156">옵션 2: PowerShellGet에서 AzureRM PowerShell 모듈 제거</span><span class="sxs-lookup"><span data-stu-id="38c86-156">Option 2: Uninstall the AzureRM PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="38c86-157">AzureRM을 PowerShellGet과 함께 설치한 경우 `Az.Accounts` 모듈의 일부로 사용할 수 있는 [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet을 사용하여 모듈을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-157">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span>

<span data-ttu-id="38c86-158">`Az.Accounts` 모듈을 사용하려면 Az 모듈이 설치되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-158">In order to use the `Az.Accounts` module, you will need to have the Az module installed.</span></span>  <span data-ttu-id="38c86-159">AzureRM 및 Az 모듈을 동시에 설치하는 것은 지원되지 않지만 Az 모듈을 사용하여 AzureRM 모듈을 즉시 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-159">Having both the AzureRM and the Az modules installed at the same time is not supported however the Az module can be used to immediately uninstall the AzureRM module.</span></span>  <span data-ttu-id="38c86-160">Az 모듈이 설치되어 있지 않은 경우 다음 명령을 사용하여 Az 모듈을 설치하고 AzureRM 모듈 경고를 무시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-160">You can install the Az module and bypass the AzureRM module warning with the following command if you do not have the Az module installed already:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="38c86-161">Az 모듈이 설치되면 다음 명령을 사용하여 _모든_ AzureRM 모듈을 머신에서 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-161">Once the Az module is installed, the following command removes _all_ AzureRM modules from your machine.</span></span> <span data-ttu-id="38c86-162">관리자 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="38c86-162">It requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

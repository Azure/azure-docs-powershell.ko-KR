---
title: Azure PowerShell 제거
description: Azure PowerShell의 전체 제거를 수행하는 방법
ms.date: 06/10/2019
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 6fc8ff8af0355ab705007f5df81d2aba8444c266
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/14/2020
ms.locfileid: "83388009"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="e9b35-103">Azure PowerShell 모듈 제거</span><span class="sxs-lookup"><span data-stu-id="e9b35-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="e9b35-104">이 문서에서는 Azure PowerShell의 이전 버전을 제거하거나 시스템에서 완전히 제거하는 방법을 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="e9b35-105">Azure PowerShell을 완전히 제거하기로 한 경우 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet을 통해 몇 가지 피드백을 보내주세요.</span><span class="sxs-lookup"><span data-stu-id="e9b35-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="e9b35-106">버그가 발생한 경우 [GitHub 문제를 제출](https://github.com/azure/azure-powershell/issues)해주시면 감사하겠습니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi-or-web-platform-installer"></a><span data-ttu-id="e9b35-107">MSI 또는 웹 플랫폼 설치 관리자 제거</span><span class="sxs-lookup"><span data-stu-id="e9b35-107">Uninstall MSI or Web Platform Installer</span></span>

<span data-ttu-id="e9b35-108">MSI 패키지 또는 웹 플랫폼 설치 관리자를 사용 하여 Azure PowerShell을 설치한 경우 PowerShell이 아닌 Windows 시스템을 통해 제거 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-108">If you installed Azure PowerShell using the MSI package or the Web Platform Installer, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="e9b35-109">플랫폼</span><span class="sxs-lookup"><span data-stu-id="e9b35-109">Platform</span></span> | <span data-ttu-id="e9b35-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="e9b35-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="e9b35-111">윈도우 10</span><span class="sxs-lookup"><span data-stu-id="e9b35-111">Windows 10</span></span> | <span data-ttu-id="e9b35-112">시작 > 설정 > 앱</span><span class="sxs-lookup"><span data-stu-id="e9b35-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="e9b35-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e9b35-113">Windows 7</span></span> </br><span data-ttu-id="e9b35-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e9b35-114">Windows 8</span></span> | <span data-ttu-id="e9b35-115">시작 > 제어판 > 프로그램 > 프로그램 제거</span><span class="sxs-lookup"><span data-stu-id="e9b35-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="e9b35-116">이 화면의 프로그램 목록에서 "Azure PowerShell"이 보여야 여기에서 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="e9b35-117">PowerShell에서 제거하기</span><span class="sxs-lookup"><span data-stu-id="e9b35-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="e9b35-118">PowerShellGet을 사용하여 Azure PowerShell을 설치하는 경우 [Uninstall-module](/powershell/module/powershellget/uninstall-module) cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="e9b35-119">그러나 `Uninstall-Module`은 모듈 중 하나만 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="e9b35-120">Azure PowerShell을 완전히 제거하려면 각 모듈을 개별적으로 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="e9b35-121">여러 버전의 Azure PowerShell이 설치되어 있는 경우 제거가 복잡할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="e9b35-122">다음 스크립트를 사용하면 단일 버전의 Azure PowerShell을 완전히 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-122">You use the following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="e9b35-123">해당 스크립트는 PowerShell 갤러리를 쿼리하여 종속 하위 모듈의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="e9b35-124">그런 다음 스크립트는 올바른 버전의 각 하위 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-124">Then, the script uninstalls the correct version of each submodule.</span></span>

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force,

    [switch]$WhatIf
  )
  
  $AllModules = @()
  
  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    if ($_.PSObject.Properties.Name -contains 'requiredVersion') {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version -ErrorAction Ignore
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        $availableModules = Get-InstalledModule $_.name -AllVersions
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall. Available versions are: {2}" -f $_.name,$version,($availableModules.Version -join ', '))
      }
    }
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}...' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop -WhatIf:$WhatIf
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

<span data-ttu-id="e9b35-125">이 함수를 사용하려면 코드를 복사하고 PowerShell 세션에 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="e9b35-126">다음 예제에서는 이전 버전의 Azure PowerShell을 제거하는 함수를 실행하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="e9b35-127">이 스크립트를 실행하면 제거하고 있는 각 하위 모듈의 이름 및 버전이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="e9b35-128">제거하지는 안되, 삭제할 것을 표시만 하도록 스크립트를 실행하려면 `-WhatIf` 옵션을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-128">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> <span data-ttu-id="e9b35-129">이 스크립트가 제거할 동일한 버전의 정확한 종속성과 매치될 수 없으면 해당 종속성의 _어떠한_ 버전도 제거하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-129">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="e9b35-130">이는 시스템에 이러한 종속성을 사용하는 대상 모듈의 다른 버전이 있을 수 있기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-130">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="e9b35-131">이 경우 해당 종속성의 사용 가능한 버전이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-131">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="e9b35-132">그러면 `Uninstall-Module`을 사용하여 이전 버전을 수동으로 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-132">You can then remove any old versions manually with `Uninstall-Module`.</span></span>


<span data-ttu-id="e9b35-133">제거하려는 Azure PowerShell의 모든 버전에 대해 이 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-133">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="e9b35-134">편의를 위해, 다음 스크립트는 최신 버전을 __제외한__ 모든 AzureRM 버전을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e9b35-134">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```

---
title: Azure PowerShell 제거
description: Azure PowerShell의 전체 제거를 수행하는 방법
ms.date: 06/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 17197b77e26ccf0e41b5faf3cbbde34338b28167
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "67037730"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="7bf4b-103">Azure PowerShell 모듈 제거</span><span class="sxs-lookup"><span data-stu-id="7bf4b-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="7bf4b-104">이 문서에서는 Azure PowerShell의 이전 버전을 제거하거나 시스템에서 완전히 제거하는 방법을 알려줍니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="7bf4b-105">Azure PowerShell을 완전히 제거하기로 한 경우 [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet을 통해 몇 가지 피드백을 보내주세요.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="7bf4b-106">버그가 발생한 경우 [GitHub 문제를 제출](https://github.com/azure/azure-powershell/issues)해주시면 감사하겠습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>


## <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="7bf4b-107">Azure PowerShell MSI 제거</span><span class="sxs-lookup"><span data-stu-id="7bf4b-107">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="7bf4b-108">MSI 패키지를 사용하여 Azure PowerShell을 설치한 경우 PowerShell이 아닌 Windows 시스템을 통해 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="7bf4b-109">플랫폼</span><span class="sxs-lookup"><span data-stu-id="7bf4b-109">Platform</span></span> | <span data-ttu-id="7bf4b-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="7bf4b-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="7bf4b-111">윈도우 10</span><span class="sxs-lookup"><span data-stu-id="7bf4b-111">Windows 10</span></span> | <span data-ttu-id="7bf4b-112">시작 > 설정 > 앱</span><span class="sxs-lookup"><span data-stu-id="7bf4b-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="7bf4b-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7bf4b-113">Windows 7</span></span> </br><span data-ttu-id="7bf4b-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7bf4b-114">Windows 8</span></span> | <span data-ttu-id="7bf4b-115">시작 > 제어판 > 프로그램 > 프로그램 제거</span><span class="sxs-lookup"><span data-stu-id="7bf4b-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="7bf4b-116">이 화면을 띄우면 프로그램 목록에 __Azure PowerShell__ 이 보일 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-116">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="7bf4b-117">이 앱을 제거하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-117">This is the app to uninstall.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="7bf4b-118">PowerShell에서 제거하기</span><span class="sxs-lookup"><span data-stu-id="7bf4b-118">Uninstall from PowerShell</span></span>

<span data-ttu-id="7bf4b-119">PowerShellGet을 사용하여 Azure PowerShell을 설치하는 경우 [Uninstall-module](/powershell/module/powershellget/uninstall-module) cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-119">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="7bf4b-120">그러나 `Uninstall-Module`은 모듈 중 하나만 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-120">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="7bf4b-121">Azure PowerShell을 완전히 제거하려면 각 모듈을 개별적으로 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-121">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="7bf4b-122">2개 이상의 Azure PowerShell 버전을 설치한 경우 제거가 복잡할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-122">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="7bf4b-123">현재 설치한 Azure PowerShell 버전을 확인하려면 다음 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-123">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

```output
Version              Name                                Repository           Description
-------              ----                                ----------           -----------
6.11.0               AzureRM                             PSGallery            Azure Resource Manager Module
6.13.1               AzureRM                             PSGallery            Azure Resource Manager Module
```

<span data-ttu-id="7bf4b-124">다음 스크립트는 PowerShell 갤러리를 쿼리하여 종속 하위 모듈의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-124">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="7bf4b-125">그런 다음 스크립트는 올바른 버전의 각 하위 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-125">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="7bf4b-126">`Process` 또는 `CurrentUser`외의 범위에서 이 스크립트를 실행하려면 관리자 권한이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-126">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="7bf4b-127">이 함수를 사용하려면 코드를 복사하고 PowerShell 세션에 붙여넣습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-127">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="7bf4b-128">다음 예제에서는 이전 버전의 Azure PowerShell을 제거하는 함수를 실행하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-128">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="7bf4b-129">이 스크립트를 실행하면 제거하고 있는 각 하위 모듈의 이름 및 버전이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-129">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="7bf4b-130">제거하지는 안되, 삭제할 것을 표시만 하도록 스크립트를 실행하려면 `-WhatIf` 옵션을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-130">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> <span data-ttu-id="7bf4b-131">이 스크립트가 제거할 동일한 버전의 정확한 종속성과 매치될 수 없으면 해당 종속성의 _어떠한_ 버전도 제거하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-131">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="7bf4b-132">이는 시스템에 이러한 종속성을 사용하는 대상 모듈의 다른 버전이 있을 수 있기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-132">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="7bf4b-133">이 경우 해당 종속성의 사용 가능한 버전이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-133">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="7bf4b-134">그러면 `Uninstall-Module`을 사용하여 이전 버전을 수동으로 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-134">You can then remove any old versions manually with `Uninstall-Module`.</span></span>


<span data-ttu-id="7bf4b-135">제거하려는 Azure PowerShell의 모든 버전에 대해 이 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-135">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="7bf4b-136">편의를 위해, 다음 스크립트는 최신 버전을 __제외한__ 모든 AzureRM 버전을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7bf4b-136">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```

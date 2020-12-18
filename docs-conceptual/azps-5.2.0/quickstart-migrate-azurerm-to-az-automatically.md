---
title: AzureRM에서 Az PowerShell 모듈로 PowerShell 스크립트 자동 마이그레이션
description: AzureRM에서 Az PowerShell 모듈로 PowerShell 스크립트를 자동으로 마이그레이션하는 방법을 알아봅니다.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 12/10/2020
ms.openlocfilehash: 6752fa0376c2f8887511455f56add0859f8961c8
ms.sourcegitcommit: 076ff98abc48e072eb1727532817487bac7507c6
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/15/2020
ms.locfileid: "97488532"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="f0e6e-103">빠른 시작: AzureRM에서 Az PowerShell 모듈로 PowerShell 스크립트 자동 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="f0e6e-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="f0e6e-104">이 문서에서는 Az.Tools.Migration PowerShell 모듈을 사용하여 PowerShell 스크립트 및 스크립트 모듈을 AzureRM에서 Az PowerShell 모듈로 자동으로 업그레이드하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f0e6e-105">Az.Tools.Migration PowerShell 모듈은 현재 공개 미리 보기로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-105">The Az.Tools.Migration PowerShell module is currently in public preview.</span></span> <span data-ttu-id="f0e6e-106">이 미리 보기 버전은 서비스 수준 계약 없이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-106">This preview version is provided without a service level agreement.</span></span> <span data-ttu-id="f0e6e-107">프로덕션 워크로드에는 권장되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-107">It's not recommended for production workloads.</span></span> <span data-ttu-id="f0e6e-108">특정 기능이 지원되지 않거나 기능이 제한될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-108">Certain features might not be supported or might have constrained capabilities.</span></span> <span data-ttu-id="f0e6e-109">자세한 내용은 [Microsoft Azure Preview에 대한 추가 사용 약관](https://azure.microsoft.com/support/legal/preview-supplemental-terms/)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-109">For more information, see [Supplemental Terms of Use for Microsoft Azure Previews](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0e6e-110">요구 사항</span><span class="sxs-lookup"><span data-stu-id="f0e6e-110">Requirements</span></span>

* <span data-ttu-id="f0e6e-111">기존 PowerShell 스크립트를 최신 버전의 [AzureRM PowerShell 모듈(6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018)로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-111">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="f0e6e-112">Az.Tools.Migration PowerShell 모듈을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-112">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="f0e6e-113">1단계: 업그레이드 계획 생성</span><span class="sxs-lookup"><span data-stu-id="f0e6e-113">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="f0e6e-114">**`New-AzUpgradeModulePlan`** cmdlet을 사용하여 스크립트 및 모듈을 Az PowerShell 모듈로 마이그레이션하기 위한 업그레이드 계획을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-114">You use the **`New-AzUpgradeModulePlan`** cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="f0e6e-115">이 cmdlet은 기존 스크립트를 변경하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-115">This cmdlet doesn’t make any changes to your existing scripts.</span></span> <span data-ttu-id="f0e6e-116">특정 스크립트를 대상으로 하는 **`FilePath`** 매개 변수를 사용하고 특정 폴더의 모든 스크립트를 대상으로 하려면 **`DirectoryPath`** 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-116">Use the **`FilePath`** parameter for targeting a specific script or the **`DirectoryPath`** parameter for targeting all scripts in a specific folder.</span></span>

> [!NOTE]
> <span data-ttu-id="f0e6e-117">**`New-AzUpgradeModulePlan`** cmdlet은 계획을 실행하지 않고 업그레이드 단계만 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-117">The **`New-AzUpgradeModulePlan`** cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

<span data-ttu-id="f0e6e-118">다음 예에서는 _`C:\Scripts`_ 폴더에 있는 모든 스크립트에 대한 계획을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-118">The following example generates a plan for all the scripts in the _`C:\Scripts`_ folder.</span></span> <span data-ttu-id="f0e6e-119">**`OutVariable`** 매개 변수가 지정되었으므로 결과가 반환되고 **`Plan`** 이라는 변수에 동시에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-119">The **`OutVariable`** parameter is specified so the results are returned and simultaneously stored in a variable named **`Plan`**.</span></span>

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

<span data-ttu-id="f0e6e-120">다음 출력에서 볼 수 있듯이 업그레이드 계획에는 AzureRM에서 Az PowerShell cmdlet으로 이동할 때 변경이 필요한 특정 파일 및 오프셋 포인트가 자세히 설명되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-120">As shown in the following output, the upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

```Output
Order Location                                                   UpgradeType     PlanResult             Original
----- --------                                                   -----------     ----------             --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter ReadyToUpgrade         ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          ReadyToUpgrade         New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          ReadyToUpgrade         Add-AzureRmVM...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          ReadyToUpgrade         Set-AzureRmVM...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          ReadyToUpgrade         New-AzureRmVM...
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          ReadyToUpgrade         New-AzureRmNe...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          ReadyToUpgrade         New-AzureRmNe...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          ReadyToUpgrade         New-AzureRmPu...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          ReadyToUpgrade         New-AzureRmVi...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          ReadyToUpgrade         New-AzureRmVi...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          ReadyToUpgrade         New-AzureRmRe...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter ReadyToUpgrade         ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          ReadyToUpgrade         New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          ReadyToUpgrade         New-AzureRmRe...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter ReadyToUpgrade         ExtensionName
...
```

<span data-ttu-id="f0e6e-121">업그레이드를 수행하기 전에 계획 결과를 보고 문제를 해결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-121">Before performing the upgrade, you need to view the results of the plan for problems.</span></span> <span data-ttu-id="f0e6e-122">다음 예에서는 스크립트와 해당 스크립트의 항목 목록을 반환하여 스크립트가 자동으로 업그레이드되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-122">The following example returns a list of scripts and the items in those scripts that will prevent them from being upgraded automatically.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

<span data-ttu-id="f0e6e-123">다음 출력에 표시된 항목은 문제를 먼저 수동으로 수정하지 않으면 자동으로 업그레이드되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-123">The items shown in the following output will not be upgraded automatically without manually correcting the issues first.</span></span> <span data-ttu-id="f0e6e-124">자동으로 업그레이드할 수 없는 알려진 문제에는 스플래팅을 사용하는 명령이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-124">Known issues that can’t be upgraded automatically include any commands that use splatting.</span></span>

```Output
Order                  : 42
UpgradeType            : CmdletParameter
PlanResult             : ErrorParameterNotFound
PlanSeverity           : Error
PlanResultReason       : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="f0e6e-125">2단계: 업그레이드 수행</span><span class="sxs-lookup"><span data-stu-id="f0e6e-125">Step 2: Perform the upgrade</span></span>

> [!CAUTION]
> <span data-ttu-id="f0e6e-126">실행 취소 작업은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-126">There is no undo operation.</span></span> <span data-ttu-id="f0e6e-127">업그레이드하려는 PowerShell 스크립트 및 모듈의 백업 복사본이 항상 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-127">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

<span data-ttu-id="f0e6e-128">계획에 만족하면 **`Invoke-AzUpgradeModulePlan`** cmdlet으로 업그레이드가 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-128">After you’re satisfied with the plan, the upgrade is performed with the **`Invoke-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="f0e6e-129">원래 스크립트가 변경되지 않도록 하려면 **`FileEditMode`** 매개 변수 값에서 **`SaveChangesToNewFiles`** 를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-129">Specify **`SaveChangesToNewFiles`** for the **`FileEditMode`** parameter value to prevent changes from being made to your original scripts.</span></span> <span data-ttu-id="f0e6e-130">이 모드를 사용하는 경우 파일 이름에 _`_az_upgraded`_ 가 추가된 각 스크립트의 복사본을 생성하여 업그레이드를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-130">When using this mode, the upgrade is performed by creating a copy of each script targeted with _`_az_upgraded`_ appended to the filenames.</span></span>

> [!WARNING]
> <span data-ttu-id="f0e6e-131">**`-FileEditMode ModifyExistingFiles`** 옵션이 지정되면 **`Invoke-AzUpgradeModulePlan`** cmdlet은 파괴적입니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-131">The **`Invoke-AzUpgradeModulePlan`** cmdlet is destructive when the **`-FileEditMode ModifyExistingFiles`** option is specified!</span></span> <span data-ttu-id="f0e6e-132">**`New-AzUpgradeModulePlan`** cmdlet에 의해 생성된 모듈 업그레이드 계획에 따라 스크립트 및 함수를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-132">It modifies your scripts and functions in place according to the module upgrade plan generated by the **`New-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="f0e6e-133">비파괴적 옵션의 경우 **`-FileEditMode SaveChangesToNewFiles`** 를 대신 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-133">For the non-destructive option specify **`-FileEditMode SaveChangesToNewFiles`** instead.</span></span>

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles -OutVariable Results
```

```Output
Order Location                                                   UpgradeType     UpgradeResult    Original
----- --------                                                   -----------     -------------    --------
1     compute-create-dockerhost.ps1:59:24                        CmdletParameter UpgradeCompleted ExtensionName
2     compute-create-dockerhost.ps1:59:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMExtens...
3     compute-create-dockerhost.ps1:54:1                         Cmdlet          UpgradeCompleted New-AzureRmVM
4     compute-create-dockerhost.ps1:51:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMSshPub...
5     compute-create-dockerhost.ps1:47:1                         Cmdlet          UpgradeCompleted Add-AzureRmVMNetwor...
6     compute-create-dockerhost.ps1:46:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMSource...
7     compute-create-dockerhost.ps1:45:1                         Cmdlet          UpgradeCompleted Set-AzureRmVMOperat...
8     compute-create-dockerhost.ps1:44:13                        Cmdlet          UpgradeCompleted New-AzureRmVMConfig
9     compute-create-dockerhost.ps1:40:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkI...
10    compute-create-dockerhost.ps1:36:8                         Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
11    compute-create-dockerhost.ps1:31:16                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
12    compute-create-dockerhost.ps1:26:15                        Cmdlet          UpgradeCompleted New-AzureRmNetworkS...
13    compute-create-dockerhost.ps1:22:8                         Cmdlet          UpgradeCompleted New-AzureRmPublicIp...
14    compute-create-dockerhost.ps1:18:9                         Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
15    compute-create-dockerhost.ps1:15:17                        Cmdlet          UpgradeCompleted New-AzureRmVirtualN...
16    compute-create-dockerhost.ps1:12:1                         Cmdlet          UpgradeCompleted New-AzureRmResource...
17    compute-create-windowsvm-quick.ps1:18:3                    CmdletParameter UpgradeCompleted ImageName
18    compute-create-windowsvm-quick.ps1:14:1                    Cmdlet          UpgradeCompleted New-AzureRmVM
19    compute-create-windowsvm-quick.ps1:11:1                    Cmdlet          UpgradeCompleted New-AzureRmResource...
20    compute-create-wordpress-mysql.ps1:59:24                   CmdletParameter UpgradeCompleted ExtensionName
...
```

<span data-ttu-id="f0e6e-134">오류가 반환되면 다음 명령을 사용하여 오류 결과를 자세히 살펴볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-134">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

```Output
Order                  : 42
UpgradeType            : CmdletParameter
UpgradeResult          : UnableToUpgrade
UpgradeSeverity        : Error
UpgradeResultReason    : Parameter was not found in Get-AzResource or it's aliases.
SourceCommand          : CommandReference
SourceCommandParameter : CommandReferenceParameter
Location               : devtestlab-add-marketplace-image-to-lab.ps1:14:74
FullPath               : C:\Scripts\devtestlab-add-marketplace-image-to-lab.ps1
StartOffset            : 556
Original               : ResourceNameEquals
Replacement            :
```

## <a name="limitations"></a><span data-ttu-id="f0e6e-135">제한 사항</span><span class="sxs-lookup"><span data-stu-id="f0e6e-135">Limitations</span></span>

* <span data-ttu-id="f0e6e-136">스플랫(splat)된 매개 변수 집합에 대한 자동화된 매개 변수 이름 업데이트는 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-136">Automated parameter name updates to splatted parameter sets aren't supported.</span></span> <span data-ttu-id="f0e6e-137">업그레이드 계획 생성 중에 발견되면 경고가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-137">If any are found during upgrade plan generation, a warning is returned.</span></span>
* <span data-ttu-id="f0e6e-138">파일 I/O 작업은 기본 인코딩을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-138">File I/O operations use default encoding.</span></span> <span data-ttu-id="f0e6e-139">비정상적인 파일 인코딩 상황으로 인해 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-139">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="f0e6e-140">Pester 단위 테스트 모의 문에 인수로 전달된 AzureRM cmdlet은 검색되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-140">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="f0e6e-141">현재 Az PowerShell 모듈 버전 4.6.1만 대상으로 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-141">Currently, only Az PowerShell module version 4.6.1 is supported as a target.</span></span>

## <a name="how-to-report-issues"></a><span data-ttu-id="f0e6e-142">문제를 보고하는 방법</span><span class="sxs-lookup"><span data-stu-id="f0e6e-142">How to report issues</span></span>

<span data-ttu-id="f0e6e-143">`azure-powershell-migration` 리포지토리에서 [GitHub 문제](https://github.com/Azure/azure-powershell-migration/issues)를 통해 Az.Tools.Migration PowerShell 모듈에 대한 피드백 및 문제를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-143">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f0e6e-144">다음 단계</span><span class="sxs-lookup"><span data-stu-id="f0e6e-144">Next steps</span></span>

<span data-ttu-id="f0e6e-145">Azure PowerShell 모듈에 대한 자세한 내용은 [Azure PowerShell 설명서](/powershell/azure/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f0e6e-145">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](/powershell/azure/)</span></span>
---
title: AzureRM에서 Az PowerShell 모듈로 PowerShell 스크립트 자동 마이그레이션
description: AzureRM에서 Az PowerShell 모듈로 PowerShell 스크립트를 자동으로 마이그레이션하는 방법을 알아봅니다.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 12/18/2020
ms.openlocfilehash: 57218c130f172bc359334b83db16e5790fa5562c
ms.sourcegitcommit: 12bb1a6d1f89789bf2a78992f9b8ca848691a4d7
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/19/2021
ms.locfileid: "98574212"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="6adcf-103">빠른 시작: AzureRM에서 Az PowerShell 모듈로 PowerShell 스크립트 자동 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="6adcf-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="6adcf-104">이 문서에서는 Az.Tools.Migration PowerShell 모듈을 사용하여 PowerShell 스크립트 및 스크립트 모듈을 AzureRM에서 Az PowerShell 모듈로 자동으로 업그레이드하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span> <span data-ttu-id="6adcf-105">추가 마이그레이션 옵션은 [Azure PowerShell을 AzureRM에서 Az로 마이그레이션](/powershell/azure/migrate-from-azurerm-to-az)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6adcf-105">For additional migration options, see [Migrate Azure PowerShell from AzureRM to Az](/powershell/azure/migrate-from-azurerm-to-az).</span></span>

## <a name="requirements"></a><span data-ttu-id="6adcf-106">요구 사항</span><span class="sxs-lookup"><span data-stu-id="6adcf-106">Requirements</span></span>

* <span data-ttu-id="6adcf-107">기존 PowerShell 스크립트를 최신 버전의 [AzureRM PowerShell 모듈(6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018)로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-107">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="6adcf-108">Az.Tools.Migration PowerShell 모듈을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-108">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="6adcf-109">1단계: 업그레이드 계획 생성</span><span class="sxs-lookup"><span data-stu-id="6adcf-109">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="6adcf-110">**`New-AzUpgradeModulePlan`** cmdlet을 사용하여 스크립트 및 모듈을 Az PowerShell 모듈로 마이그레이션하기 위한 업그레이드 계획을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-110">You use the **`New-AzUpgradeModulePlan`** cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="6adcf-111">이 cmdlet은 기존 스크립트를 변경하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-111">This cmdlet doesn’t make any changes to your existing scripts.</span></span> <span data-ttu-id="6adcf-112">특정 스크립트를 대상으로 하는 **`FilePath`** 매개 변수를 사용하고 특정 폴더의 모든 스크립트를 대상으로 하려면 **`DirectoryPath`** 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-112">Use the **`FilePath`** parameter for targeting a specific script or the **`DirectoryPath`** parameter for targeting all scripts in a specific folder.</span></span>

> [!NOTE]
> <span data-ttu-id="6adcf-113">**`New-AzUpgradeModulePlan`** cmdlet은 계획을 실행하지 않고 업그레이드 단계만 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-113">The **`New-AzUpgradeModulePlan`** cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

<span data-ttu-id="6adcf-114">다음 예에서는 _`C:\Scripts`_ 폴더에 있는 모든 스크립트에 대한 계획을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-114">The following example generates a plan for all the scripts in the _`C:\Scripts`_ folder.</span></span> <span data-ttu-id="6adcf-115">**`OutVariable`** 매개 변수가 지정되었으므로 결과가 반환되고 **`Plan`** 이라는 변수에 동시에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-115">The **`OutVariable`** parameter is specified so the results are returned and simultaneously stored in a variable named **`Plan`**.</span></span>

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 5.2.0 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

<span data-ttu-id="6adcf-116">다음 출력에서 볼 수 있듯이 업그레이드 계획에는 AzureRM에서 Az PowerShell cmdlet으로 이동할 때 변경이 필요한 특정 파일 및 오프셋 포인트가 자세히 설명되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-116">As shown in the following output, the upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

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

<span data-ttu-id="6adcf-117">업그레이드를 수행하기 전에 계획 결과를 보고 문제를 해결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-117">Before performing the upgrade, you need to view the results of the plan for problems.</span></span> <span data-ttu-id="6adcf-118">다음 예에서는 스크립트와 해당 스크립트의 항목 목록을 반환하여 스크립트가 자동으로 업그레이드되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-118">The following example returns a list of scripts and the items in those scripts that will prevent them from being upgraded automatically.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

<span data-ttu-id="6adcf-119">다음 출력에 표시된 항목은 문제를 먼저 수동으로 수정하지 않으면 자동으로 업그레이드되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-119">The items shown in the following output will not be upgraded automatically without manually correcting the issues first.</span></span>

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

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="6adcf-120">2단계: 업그레이드 수행</span><span class="sxs-lookup"><span data-stu-id="6adcf-120">Step 2: Perform the upgrade</span></span>

> [!CAUTION]
> <span data-ttu-id="6adcf-121">실행 취소 작업은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-121">There is no undo operation.</span></span> <span data-ttu-id="6adcf-122">업그레이드하려는 PowerShell 스크립트 및 모듈의 백업 복사본이 항상 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-122">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

<span data-ttu-id="6adcf-123">계획에 만족하면 **`Invoke-AzUpgradeModulePlan`** cmdlet으로 업그레이드가 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-123">After you’re satisfied with the plan, the upgrade is performed with the **`Invoke-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="6adcf-124">원래 스크립트가 변경되지 않도록 하려면 **`FileEditMode`** 매개 변수 값에서 **`SaveChangesToNewFiles`** 를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-124">Specify **`SaveChangesToNewFiles`** for the **`FileEditMode`** parameter value to prevent changes from being made to your original scripts.</span></span> <span data-ttu-id="6adcf-125">이 모드를 사용하는 경우 파일 이름에 _`_az_upgraded`_ 가 추가된 각 스크립트의 복사본을 생성하여 업그레이드를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-125">When using this mode, the upgrade is performed by creating a copy of each script targeted with _`_az_upgraded`_ appended to the filenames.</span></span>

> [!WARNING]
> <span data-ttu-id="6adcf-126">**`-FileEditMode ModifyExistingFiles`** 옵션이 지정되면 **`Invoke-AzUpgradeModulePlan`** cmdlet은 파괴적입니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-126">The **`Invoke-AzUpgradeModulePlan`** cmdlet is destructive when the **`-FileEditMode ModifyExistingFiles`** option is specified!</span></span> <span data-ttu-id="6adcf-127">**`New-AzUpgradeModulePlan`** cmdlet에 의해 생성된 모듈 업그레이드 계획에 따라 스크립트 및 함수를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-127">It modifies your scripts and functions in place according to the module upgrade plan generated by the **`New-AzUpgradeModulePlan`** cmdlet.</span></span> <span data-ttu-id="6adcf-128">비파괴적 옵션의 경우 **`-FileEditMode SaveChangesToNewFiles`** 를 대신 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-128">For the non-destructive option specify **`-FileEditMode SaveChangesToNewFiles`** instead.</span></span>

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

<span data-ttu-id="6adcf-129">오류가 반환되면 다음 명령을 사용하여 오류 결과를 자세히 살펴볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-129">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

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

## <a name="limitations"></a><span data-ttu-id="6adcf-130">제한 사항</span><span class="sxs-lookup"><span data-stu-id="6adcf-130">Limitations</span></span>

* <span data-ttu-id="6adcf-131">파일 I/O 작업은 기본 인코딩을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-131">File I/O operations use default encoding.</span></span> <span data-ttu-id="6adcf-132">비정상적인 파일 인코딩 상황으로 인해 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-132">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="6adcf-133">Pester 단위 테스트 모의 문에 인수로 전달된 AzureRM cmdlet은 검색되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-133">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="6adcf-134">현재 Az PowerShell 모듈 버전 5.2.0만 대상으로 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-134">Currently, only Az PowerShell module version 5.2.0 is supported as a target.</span></span>

## <a name="how-to-report-issues"></a><span data-ttu-id="6adcf-135">문제를 보고하는 방법</span><span class="sxs-lookup"><span data-stu-id="6adcf-135">How to report issues</span></span>

<span data-ttu-id="6adcf-136">`azure-powershell-migration` 리포지토리에서 [GitHub 문제](https://github.com/Azure/azure-powershell-migration/issues)를 통해 Az.Tools.Migration PowerShell 모듈에 대한 피드백 및 문제를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="6adcf-136">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6adcf-137">다음 단계</span><span class="sxs-lookup"><span data-stu-id="6adcf-137">Next steps</span></span>

<span data-ttu-id="6adcf-138">Azure PowerShell 모듈에 대한 자세한 내용은 [Azure PowerShell 설명서](/powershell/azure/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6adcf-138">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](/powershell/azure/)</span></span>
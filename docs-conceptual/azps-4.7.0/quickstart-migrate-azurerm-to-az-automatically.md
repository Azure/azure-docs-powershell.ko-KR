---
title: AzureRM에서 Az PowerShell 모듈로 PowerShell 스크립트 자동 마이그레이션
description: AzureRM에서 Az PowerShell 모듈로 PowerShell 스크립트를 자동으로 마이그레이션하는 방법을 알아봅니다.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 09/11/2020
ms.openlocfilehash: d342ca65baf7664f430de3b7d294c0fc9815c0a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "92002070"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a><span data-ttu-id="c2178-103">빠른 시작: AzureRM에서 Az PowerShell 모듈로 PowerShell 스크립트 자동 마이그레이션</span><span class="sxs-lookup"><span data-stu-id="c2178-103">Quickstart: Automatically migrate PowerShell scripts from AzureRM to the Az PowerShell module</span></span>

<span data-ttu-id="c2178-104">이 문서에서는 Az.Tools.Migration PowerShell 모듈을 사용하여 PowerShell 스크립트 및 스크립트 모듈을 AzureRM에서 Az PowerShell 모듈로 자동으로 업그레이드하는 방법을 알아봅니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-104">In this article, you'll learn how to use the Az.Tools.Migration PowerShell module to automatically upgrade your PowerShell scripts and script modules from AzureRM to the Az PowerShell module.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2178-105">Az.Tools.Migration PowerShell 모듈은 현재 공개 미리 보기로 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-105">The Az.Tools.Migration PowerShell module is currently in public preview.</span></span> <span data-ttu-id="c2178-106">이 미리 보기 버전은 서비스 수준 계약 없이 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-106">This preview version is provided without a service level agreement.</span></span> <span data-ttu-id="c2178-107">프로덕션 워크로드에는 권장되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-107">It's not recommended for production workloads.</span></span> <span data-ttu-id="c2178-108">특정 기능이 지원되지 않거나 기능이 제한될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-108">Certain features might not be supported or might have constrained capabilities.</span></span> <span data-ttu-id="c2178-109">자세한 내용은 [Microsoft Azure Preview에 대한 추가 사용 약관](https://azure.microsoft.com/support/legal/preview-supplemental-terms/)을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c2178-109">For more information, see [Supplemental Terms of Use for Microsoft Azure Previews](https://azure.microsoft.com/support/legal/preview-supplemental-terms/).</span></span>

<span data-ttu-id="c2178-110">`azure-powershell-migration` 리포지토리에서 [GitHub 문제](https://github.com/Azure/azure-powershell-migration/issues)를 통해 Az.Tools.Migration PowerShell 모듈에 대한 피드백 및 문제를 보고합니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-110">Report feedback and issues about the Az.Tools.Migration PowerShell module via [a GitHub issue](https://github.com/Azure/azure-powershell-migration/issues) in the `azure-powershell-migration` repository.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2178-111">요구 사항</span><span class="sxs-lookup"><span data-stu-id="c2178-111">Requirements</span></span>

* <span data-ttu-id="c2178-112">기존 PowerShell 스크립트를 최신 버전의 [AzureRM PowerShell 모듈(6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018)로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-112">Update your existing PowerShell scripts to the latest version of the [AzureRM PowerShell module (6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018).</span></span>
* <span data-ttu-id="c2178-113">Az.Tools.Migration PowerShell 모듈을 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-113">Install the Az.Tools.Migration PowerShell module.</span></span>

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a><span data-ttu-id="c2178-114">1단계: 업그레이드 계획 생성</span><span class="sxs-lookup"><span data-stu-id="c2178-114">Step 1: Generate an upgrade plan</span></span>

<span data-ttu-id="c2178-115">`New-AzUpgradeModulePlan` cmdlet을 사용하여 스크립트 및 모듈을 Az PowerShell 모듈로 마이그레이션하기 위한 업그레이드 계획을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-115">You use the `New-AzUpgradeModulePlan` cmdlet to generate an upgrade plan for migrating your scripts and modules to the Az PowerShell module.</span></span> <span data-ttu-id="c2178-116">업그레이드 계획에는 AzureRM에서 Az PowerShell cmdlet으로 이동할 때 변경이 필요한 특정 파일 및 오프셋 포인트가 자세히 설명되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-116">The upgrade plan details the specific file and offset points that require changes when moving from AzureRM to the Az PowerShell cmdlets.</span></span>

> [!NOTE]
> <span data-ttu-id="c2178-117">`New-AzUpgradeModulePlan` cmdlet은 계획을 실행하지 않고 업그레이드 단계만 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-117">The `New-AzUpgradeModulePlan` cmdlet doesn't execute the plan, it only generates the upgrade steps.</span></span>

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

<span data-ttu-id="c2178-118">업그레이드 계획 결과를 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-118">Review the results of the upgrade plan.</span></span>

```powershell
# Show the entire upgrade plan
$Plan
```

<span data-ttu-id="c2178-119">다음 명령을 실행하여 경고나 오류가 발생한 명령에 대한 결과를 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-119">Run the following command to filter the results to commands that have warnings or errors.</span></span> <span data-ttu-id="c2178-120">업그레이드를 수행하기 전에 큰 결과 집합에서 오류를 신속하게 식별하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-120">This may be helpful on large result sets to quickly identify errors before performing the upgrade.</span></span>

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a><span data-ttu-id="c2178-121">2단계: 업그레이드 수행</span><span class="sxs-lookup"><span data-stu-id="c2178-121">Step 2: Perform the upgrade</span></span>

<span data-ttu-id="c2178-122">업그레이드 계획은 `Invoke-AzUpgradeModulePlan` cmdlet을 실행할 때 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-122">The upgrade plan is executed when you run the `Invoke-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="c2178-123">이 명령은 `New-AzUpgradeModulePlan` cmdlet에 의해 식별된 오류를 제외하고 지정된 파일 또는 폴더의 업그레이드를 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-123">This command performs an upgrade of the specified file or folders except for any errors that were identified by the `New-AzUpgradeModulePlan` cmdlet.</span></span>

<span data-ttu-id="c2178-124">이 명령을 사용하려면 파일을 수정할지 또는 새 파일을 원본 파일과 함께 저장할지를 지정해야 합니다(원본은 그대로 둠).</span><span class="sxs-lookup"><span data-stu-id="c2178-124">This command requires you to specify if the files should be modified in place or if new files should be saved alongside your original files (leaving originals unmodified).</span></span>

> [!CAUTION]
> <span data-ttu-id="c2178-125">실행 취소 작업은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-125">There is no undo operation.</span></span> <span data-ttu-id="c2178-126">업그레이드하려는 PowerShell 스크립트 및 모듈의 백업 복사본이 항상 있는지 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-126">Always ensure that you have a backup copy of your PowerShell scripts and modules that you're attempting to upgrade.</span></span>

> [!WARNING]
> <span data-ttu-id="c2178-127">`-FileEditMode ModifyExistingFiles` 옵션이 지정되면 `Invoke-AzUpgradeModulePlan` cmdlet은 파괴적입니다!</span><span class="sxs-lookup"><span data-stu-id="c2178-127">The `Invoke-AzUpgradeModulePlan` cmdlet is destructive when the `-FileEditMode ModifyExistingFiles` option is specified!</span></span> <span data-ttu-id="c2178-128">`New-AzUpgradeModulePlan` cmdlet에 의해 생성된 모듈 업그레이드 계획에 따라 스크립트 및 함수를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-128">It modifies your scripts and functions in place according to the module upgrade plan generated by the `New-AzUpgradeModulePlan` cmdlet.</span></span> <span data-ttu-id="c2178-129">비파괴적 옵션의 경우 `-FileEditMode SaveChangesToNewFiles`를 대신 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-129">For the non-destructive option specify `-FileEditMode SaveChangesToNewFiles` instead.</span></span>

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

<span data-ttu-id="c2178-130">업그레이드 작업 결과를 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-130">Review the results of the upgrade operation.</span></span>

```powershell
# Show the results for the entire upgrade operation
$Results
```

<span data-ttu-id="c2178-131">오류가 반환되면 다음 명령을 사용하여 오류 결과를 자세히 살펴볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-131">If any errors are returned, you can take a closer look at the error results with the following command:</span></span>

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a><span data-ttu-id="c2178-132">제한 사항</span><span class="sxs-lookup"><span data-stu-id="c2178-132">Limitations</span></span>

* <span data-ttu-id="c2178-133">스플랫(splat)된 매개 변수 집합에 대한 자동화된 매개 변수 이름 업데이트는 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-133">Automated parameter name updates to splatted parameter sets aren't supported.</span></span> <span data-ttu-id="c2178-134">업그레이드 계획 생성 중에 발견되면 경고가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-134">If any are found during upgrade plan generation, a warning is returned.</span></span>
* <span data-ttu-id="c2178-135">파일 I/O 작업은 기본 인코딩을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-135">File I/O operations use default encoding.</span></span> <span data-ttu-id="c2178-136">비정상적인 파일 인코딩 상황으로 인해 문제가 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-136">Unusual file encoding situations may cause problems.</span></span>
* <span data-ttu-id="c2178-137">Pester 단위 테스트 모의 문에 인수로 전달된 AzureRM cmdlet은 검색되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-137">AzureRM cmdlets passed as arguments to Pester unit test mock statements aren't detected.</span></span>
* <span data-ttu-id="c2178-138">현재 Az PowerShell 모듈 버전 4.6.1만 대상으로 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2178-138">Currently, only Az PowerShell module version 4.6.1 is supported as a target.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c2178-139">다음 단계</span><span class="sxs-lookup"><span data-stu-id="c2178-139">Next steps</span></span>

<span data-ttu-id="c2178-140">Azure PowerShell 모듈에 대한 자세한 내용은 [Azure PowerShell 설명서](https://docs.microsoft.com/powershell/azure/)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c2178-140">To learn more about the Az PowerShell module, see the [Azure PowerShell documentation](https://docs.microsoft.com/powershell/azure/)</span></span>
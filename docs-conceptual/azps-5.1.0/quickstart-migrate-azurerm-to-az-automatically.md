---
title: AzureRM에서 Az PowerShell 모듈로 PowerShell 스크립트 자동 마이그레이션
description: AzureRM에서 Az PowerShell 모듈로 PowerShell 스크립트를 자동으로 마이그레이션하는 방법을 알아봅니다.
author: mikefrobbins
ms.service: azure-powershell
ms.topic: quickstart
ms.custom: devx-track-azurepowershell
ms.author: mirobb
ms.date: 09/11/2020
ms.openlocfilehash: 5945b573d467f1ff64e327c52124ffed1e4305aa
ms.sourcegitcommit: ec731e58b7de3eb14df6d3bf308df92154125bbb
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/21/2020
ms.locfileid: "95005860"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>빠른 시작: AzureRM에서 Az PowerShell 모듈로 PowerShell 스크립트 자동 마이그레이션

이 문서에서는 Az.Tools.Migration PowerShell 모듈을 사용하여 PowerShell 스크립트 및 스크립트 모듈을 AzureRM에서 Az PowerShell 모듈로 자동으로 업그레이드하는 방법을 알아봅니다.

> [!IMPORTANT]
> Az.Tools.Migration PowerShell 모듈은 현재 공개 미리 보기로 제공됩니다. 이 미리 보기 버전은 서비스 수준 계약 없이 제공됩니다. 프로덕션 워크로드에는 권장되지 않습니다. 특정 기능이 지원되지 않거나 기능이 제한될 수 있습니다. 자세한 내용은 [Microsoft Azure Preview에 대한 추가 사용 약관](https://azure.microsoft.com/support/legal/preview-supplemental-terms/)을 참조하세요.

`azure-powershell-migration` 리포지토리에서 [GitHub 문제](https://github.com/Azure/azure-powershell-migration/issues)를 통해 Az.Tools.Migration PowerShell 모듈에 대한 피드백 및 문제를 보고합니다.

## <a name="requirements"></a>요구 사항

* 기존 PowerShell 스크립트를 최신 버전의 [AzureRM PowerShell 모듈(6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018)로 업데이트합니다.
* Az.Tools.Migration PowerShell 모듈을 설치합니다.

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>1단계: 업그레이드 계획 생성

`New-AzUpgradeModulePlan` cmdlet을 사용하여 스크립트 및 모듈을 Az PowerShell 모듈로 마이그레이션하기 위한 업그레이드 계획을 생성할 수 있습니다. 업그레이드 계획에는 AzureRM에서 Az PowerShell cmdlet으로 이동할 때 변경이 필요한 특정 파일 및 오프셋 포인트가 자세히 설명되어 있습니다.

> [!NOTE]
> `New-AzUpgradeModulePlan` cmdlet은 계획을 실행하지 않고 업그레이드 단계만 생성합니다.

```powershell
#  Generate an upgrade plan for the specified PowerShell script and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -FilePath 'C:\Scripts\my-azure-script.ps1'
```

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
$Plan = New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 4.6.1 -DirectoryPath 'C:\Scripts'
```

업그레이드 계획 결과를 검토합니다.

```powershell
# Show the entire upgrade plan
$Plan
```

다음 명령을 실행하여 경고나 오류가 발생한 명령에 대한 결과를 필터링합니다. 업그레이드를 수행하기 전에 큰 결과 집합에서 오류를 신속하게 식별하는 데 도움이 될 수 있습니다.

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

## <a name="step-2-perform-the-upgrade"></a>2단계: 업그레이드 수행

업그레이드 계획은 `Invoke-AzUpgradeModulePlan` cmdlet을 실행할 때 실행됩니다. 이 명령은 `New-AzUpgradeModulePlan` cmdlet에 의해 식별된 오류를 제외하고 지정된 파일 또는 폴더의 업그레이드를 수행합니다.

이 명령을 사용하려면 파일을 수정할지 또는 새 파일을 원본 파일과 함께 저장할지를 지정해야 합니다(원본은 그대로 둠).

> [!CAUTION]
> 실행 취소 작업은 없습니다. 업그레이드하려는 PowerShell 스크립트 및 모듈의 백업 복사본이 항상 있는지 확인합니다.

> [!WARNING]
> `-FileEditMode ModifyExistingFiles` 옵션이 지정되면 `Invoke-AzUpgradeModulePlan` cmdlet은 파괴적입니다! `New-AzUpgradeModulePlan` cmdlet에 의해 생성된 모듈 업그레이드 계획에 따라 스크립트 및 함수를 수정합니다. 비파괴적 옵션의 경우 `-FileEditMode SaveChangesToNewFiles`를 대신 지정합니다.

```powershell
# Execute the automatic upgrade plan and save the results to a variable.
$Results = Invoke-AzUpgradeModulePlan -Plan $Plan -FileEditMode SaveChangesToNewFiles
```

업그레이드 작업 결과를 검토합니다.

```powershell
# Show the results for the entire upgrade operation
$Results
```

오류가 반환되면 다음 명령을 사용하여 오류 결과를 자세히 살펴볼 수 있습니다.

```powershell
# Filter results to show only errors
$Results | Where-Object UpgradeResult -ne UpgradeCompleted | Format-List
```

## <a name="limitations"></a>제한 사항

* 스플랫(splat)된 매개 변수 집합에 대한 자동화된 매개 변수 이름 업데이트는 지원되지 않습니다. 업그레이드 계획 생성 중에 발견되면 경고가 반환됩니다.
* 파일 I/O 작업은 기본 인코딩을 사용합니다. 비정상적인 파일 인코딩 상황으로 인해 문제가 발생할 수 있습니다.
* Pester 단위 테스트 모의 문에 인수로 전달된 AzureRM cmdlet은 검색되지 않습니다.
* 현재 Az PowerShell 모듈 버전 4.6.1만 대상으로 지원됩니다.

## <a name="next-steps"></a>다음 단계

Azure PowerShell 모듈에 대한 자세한 내용은 [Azure PowerShell 설명서](/powershell/azure/)를 참조하세요.
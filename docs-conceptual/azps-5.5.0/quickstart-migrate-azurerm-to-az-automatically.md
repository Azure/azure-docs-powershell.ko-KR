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
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100012031"
---
# <a name="quickstart-automatically-migrate-powershell-scripts-from-azurerm-to-the-az-powershell-module"></a>빠른 시작: AzureRM에서 Az PowerShell 모듈로 PowerShell 스크립트 자동 마이그레이션

이 문서에서는 Az.Tools.Migration PowerShell 모듈을 사용하여 PowerShell 스크립트 및 스크립트 모듈을 AzureRM에서 Az PowerShell 모듈로 자동으로 업그레이드하는 방법을 알아봅니다. 추가 마이그레이션 옵션은 [Azure PowerShell을 AzureRM에서 Az로 마이그레이션](/powershell/azure/migrate-from-azurerm-to-az)을 참조하세요.

## <a name="requirements"></a>요구 사항

* 기존 PowerShell 스크립트를 최신 버전의 [AzureRM PowerShell 모듈(6.13.1)](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018)로 업데이트합니다.
* Az.Tools.Migration PowerShell 모듈을 설치합니다.

  ```powershell
  Install-Module -Name Az.Tools.Migration
  ```

## <a name="step-1-generate-an-upgrade-plan"></a>1단계: 업그레이드 계획 생성

**`New-AzUpgradeModulePlan`** cmdlet을 사용하여 스크립트 및 모듈을 Az PowerShell 모듈로 마이그레이션하기 위한 업그레이드 계획을 생성할 수 있습니다. 이 cmdlet은 기존 스크립트를 변경하지 않습니다. 특정 스크립트를 대상으로 하는 **`FilePath`** 매개 변수를 사용하고 특정 폴더의 모든 스크립트를 대상으로 하려면 **`DirectoryPath`** 매개 변수를 사용합니다.

> [!NOTE]
> **`New-AzUpgradeModulePlan`** cmdlet은 계획을 실행하지 않고 업그레이드 단계만 생성합니다.

다음 예에서는 _`C:\Scripts`_ 폴더에 있는 모든 스크립트에 대한 계획을 생성합니다. **`OutVariable`** 매개 변수가 지정되었으므로 결과가 반환되고 **`Plan`** 이라는 변수에 동시에 저장됩니다.

```powershell
# Generate an upgrade plan for all the scripts and module files in the specified folder and save it to a variable.
New-AzUpgradeModulePlan -FromAzureRmVersion 6.13.1 -ToAzVersion 5.2.0 -DirectoryPath 'C:\Scripts' -OutVariable Plan
```

다음 출력에서 볼 수 있듯이 업그레이드 계획에는 AzureRM에서 Az PowerShell cmdlet으로 이동할 때 변경이 필요한 특정 파일 및 오프셋 포인트가 자세히 설명되어 있습니다.

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

업그레이드를 수행하기 전에 계획 결과를 보고 문제를 해결해야 합니다. 다음 예에서는 스크립트와 해당 스크립트의 항목 목록을 반환하여 스크립트가 자동으로 업그레이드되지 않도록 합니다.

```powershell
# Filter plan results to only warnings and errors
$Plan | Where-Object PlanResult -ne ReadyToUpgrade | Format-List
```

다음 출력에 표시된 항목은 문제를 먼저 수동으로 수정하지 않으면 자동으로 업그레이드되지 않습니다.

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

## <a name="step-2-perform-the-upgrade"></a>2단계: 업그레이드 수행

> [!CAUTION]
> 실행 취소 작업은 없습니다. 업그레이드하려는 PowerShell 스크립트 및 모듈의 백업 복사본이 항상 있는지 확인합니다.

계획에 만족하면 **`Invoke-AzUpgradeModulePlan`** cmdlet으로 업그레이드가 수행됩니다. 원래 스크립트가 변경되지 않도록 하려면 **`FileEditMode`** 매개 변수 값에서 **`SaveChangesToNewFiles`** 를 지정합니다. 이 모드를 사용하는 경우 파일 이름에 _`_az_upgraded`_ 가 추가된 각 스크립트의 복사본을 생성하여 업그레이드를 수행합니다.

> [!WARNING]
> **`-FileEditMode ModifyExistingFiles`** 옵션이 지정되면 **`Invoke-AzUpgradeModulePlan`** cmdlet은 파괴적입니다. **`New-AzUpgradeModulePlan`** cmdlet에 의해 생성된 모듈 업그레이드 계획에 따라 스크립트 및 함수를 수정합니다. 비파괴적 옵션의 경우 **`-FileEditMode SaveChangesToNewFiles`** 를 대신 지정합니다.

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

오류가 반환되면 다음 명령을 사용하여 오류 결과를 자세히 살펴볼 수 있습니다.

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

## <a name="limitations"></a>제한 사항

* 파일 I/O 작업은 기본 인코딩을 사용합니다. 비정상적인 파일 인코딩 상황으로 인해 문제가 발생할 수 있습니다.
* Pester 단위 테스트 모의 문에 인수로 전달된 AzureRM cmdlet은 검색되지 않습니다.
* 현재 Az PowerShell 모듈 버전 5.2.0만 대상으로 지원됩니다.

## <a name="how-to-report-issues"></a>문제를 보고하는 방법

`azure-powershell-migration` 리포지토리에서 [GitHub 문제](https://github.com/Azure/azure-powershell-migration/issues)를 통해 Az.Tools.Migration PowerShell 모듈에 대한 피드백 및 문제를 보고합니다.

## <a name="next-steps"></a>다음 단계

Azure PowerShell 모듈에 대한 자세한 내용은 [Azure PowerShell 설명서](/powershell/azure/)를 참조하세요.

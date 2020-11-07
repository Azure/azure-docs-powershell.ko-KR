---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: fbcb93ec75dc0e136c1c18743a8686f7642ef02f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696670"
---
# Get-AzDeploymentManagerRollout

## SYNOPSIS
출시를 가져옵니다.

## 구문과

### 대화형 (기본값)
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 리소스
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzDeploymentManagerRollout** cmdlet은 롤아웃을 가져오고, 롤아웃 진행 상황에 대 한 모든 세부 정보를 사용 하 여 해당 롤아웃을 나타내는 개체를 반환 합니다.
이름 및 리소스 그룹 이름을 기준으로 출시를 지정 합니다. 또는 롤아웃 개체 또는 ResourceId를 제공할 수 있습니다.

반환 되는 출시 개체에는 서비스, 서비스 단위, 배포 된 작업 및 진행 중인 단계가 포함 됩니다. 아직 배포 되지 않은 항목이 응답에 없습니다.

## 예제의

### 예제 1 출시 준비
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

이 명령은 ContosoResourceGroup에 ContosoRollout 이라는 롤아웃을 가져옵니다. 

### 예제 2 롤아웃 세부 정보 가져오기 및 표시
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

이 명령은 ContosoResourceGroup에 ContosoRollout 이라는 롤아웃을 가져옵니다. -Verbose 스위치는 모든 롤아웃 세부 정보를 계층적으로 표시 합니다. 롤아웃에 대 한 전체적인 보기를 위해 각 단계의 서비스, ServiceUnits 및 각 단계에 대 한 컨텍스트 정보를 표시 합니다.

### 예제 3: 리소스 식별자를 사용 하 여 롤아웃 가져오기
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

이 명령은 ContosoResourceGroup에 ContosoRollout 이라는 롤아웃을 가져옵니다.

### 예제 4: 롤아웃 개체를 사용 하 여 출시를 가져옵니다.
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

이 명령은 이름 및 ResourceGroup이 $rolloutObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 롤아웃을 가져옵니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
개체를 출시 합니다.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -이름
롤아웃 이름입니다.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
리소스 식별자입니다.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetryAttempt
롤아웃을 다시 시도 합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### 시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]

### Microsoft. Azure. PSRollout. 모델. a 배포

## 출력

### Microsoft. Azure. PSRollout. 모델. a 배포

## 상속자

## 관련 링크

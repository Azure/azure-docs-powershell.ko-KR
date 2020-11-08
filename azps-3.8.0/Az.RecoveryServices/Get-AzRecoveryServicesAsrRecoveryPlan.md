---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4873c30caf0f1b59bf9be848f44c6e1358649b69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034072"
---
# Get-AzRecoveryServicesAsrRecoveryPlan

## SYNOPSIS
복구 계획 또는 복구 서비스 자격 증명 모음의 모든 복구 계획을 가져옵니다.

## 구문과

### 기본값 (기본값)
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFriendlyName
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzRecoveryServicesAsrRecoveryPlan** cmdlet은 지정 된 복구 계획 또는 복구 서비스 자격 증명 모음의 모든 복구 계획에 대 한 세부 정보를 가져옵니다.

## 예제의

### 예제 1
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

지정 된 이름의 복구 계획을 가져옵니다.

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

### -FriendlyName
가져올 복구 계획의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
가져올 복구 계획의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
이 cmdlet이 복구 계획 json 정의를 저장할 파일 경로를 지정 합니다. 복구 계획을 수정 하 고 Update-AzRecoveryServicesASRRecoveryPlan cmdlet을 통해 복구 계획을 업데이트 하는 데 사용 되는 json 정의를 편집할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### 않아야

## 출력

### SiteRecovery를 통한 Recoveryrrecoveryplan 계획

## 상속자

## 관련 링크

[새로운 AzRecoveryServicesAsrRecoveryPlan](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[제거-AzRecoveryServicesAsrRecoveryPlan](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[업데이트-AzRecoveryServicesAsrRecoveryPlan](./Update-AzRecoveryServicesAsrRecoveryPlan.md)

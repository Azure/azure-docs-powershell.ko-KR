---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034067"
---
# Get-AzRecoveryServicesAsrStorageClassificationMapping

## SYNOPSIS
ASR 저장소 분류 매핑을 가져옵니다.

## 구문과

### ByObject (기본값)
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzRecoveryServicesAsrStorageClassificationMapping** CMDLET은 ASR 저장소 분류 매핑의 세부 정보를 가져옵니다.

## 예제의

### 예제 1
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

지정 된 저장소 분류에 해당 하는 모든 저장소 분류 매핑을 나열 합니다.

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

### -이름
가져올 저장소 분류 매핑의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageClassification
ASR 저장소 분류 개체를 지정 합니다. Cmdlet은 지정 된 저장소 분류에 해당 하는 ASR 저장소 분류 매핑을 가져옵니다. 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### SiteRecovery. ASRStorageClassification에 대 한 서비스

## 출력

### SiteRecovery. ASRStorageClassificationMapping에 대 한 서비스

## 상속자

## 관련 링크

[새로운 AzRecoveryServicesAsrStorageClassificationMapping](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[제거-AzRecoveryServicesAsrStorageClassificationMapping](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)

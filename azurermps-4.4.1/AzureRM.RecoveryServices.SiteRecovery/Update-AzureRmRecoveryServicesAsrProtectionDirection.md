---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: afa5da5a34954c1e1a610ce9153172934069c2a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703646"
---
# Update-AzureRmRecoveryServicesAsrProtectionDirection

## SYNOPSIS
지정 된 복제 보호 항목 또는 복구 계획에 대 한 복제 방향을 업데이트 합니다. 복제 된 항목 또는 복구 계획을 통해 장애를 다시 방지 하거나 역 복제 하는 데 사용 됩니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByRPIObject (기본값)
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByRPObject
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByPEObject
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzureRmRecoveryServicesAsrProtectionDirection** cmdlet은 커밋 장애 조치 작업이 완료 된 후 지정 된 Azure Site Recovery 개체의 복제 방향을 업데이트 합니다.

## 예제의

### 예제 1
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

지정 된 recoveyr 계획에 대 한 방향 업데이트 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업 개체를 반환 합니다.

## 변수

### 방향
업데이트 작업에 대해 장애 조치를 게시 하는 데 사용할 방향을 지정 합니다.  
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- PrimaryToRecovery
- RecoveryToPrimary

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPlan
ASR 복구 계획 개체를 지정 합니다.

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReplicationProtectedItem
ASR 복제 보호 항목을 지정 합니다.

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### SiteRecovery를 통한 Recoveryrrecoveryplan 계획
SiteRecovery. ASRReplicationProtectedItem에 대 한 서비스

## 출력

### SiteRecovery. r i m m 작업

## 상속자

## 관련 링크


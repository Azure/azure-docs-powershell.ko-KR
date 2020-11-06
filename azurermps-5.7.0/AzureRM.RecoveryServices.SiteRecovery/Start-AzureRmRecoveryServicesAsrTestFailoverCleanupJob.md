---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailovercleanupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob.md
ms.openlocfilehash: 423ec89745b21176c714c1c2e956d4320c28b034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525004"
---
# Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob

## SYNOPSIS
테스트 장애 조치 정리 작업을 시작 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByRPIObject (기본값)
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Comment <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceId
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ResourceId <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByRPObject
```
Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -RecoveryPlan <ASRRecoveryPlan> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmRecoveryServicesAsrTestFailoverCleanupJob** cmdlet은 테스트 장애 조치를 수행한 복제 보호 항목 또는 복구 계획에서 장애 조치 (failover) 정리 작업을 시작 합니다.

## 예제의

### 예제 1
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $rpi -Comments "testing done"
```

Azure Site Recovery 복제 보호 항목의 테스트 장애 조치 정리를 추적 하는 작업입니다.

### 예제 2
```
PS C:\> Start-AzureRmRecoveryServicesAsrTestFailoverCleanupJob -ReplicationProtectedItem $recoveryPlan -Comments "testing done"
```

Azure Site Recovery recoveryPlan의 테스트 장애 조치 정리를 추적 하는 작업입니다.

## 변수

### -메모
테스트 장애 조치에 대 한 사용자 설명입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPlan
장애 조치 (failover) 정리 테스트를 수행 하는 복구 계획입니다.

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
복제 보호 항목에서 테스트 장애 조치 정리를 수행 합니다.

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

### -ResourceId
Cleanon 테스트 장애 조치를 위해 복제 보호 항목의 리소스 Id/복구 계획입니다.

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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

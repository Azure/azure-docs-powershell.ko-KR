---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: b7a9dffe443ca7603b8b5a3bdd100560d83a498e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526120"
---
# Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob

## SYNOPSIS
계획 되지 않은 장애 조치 작업을 시작 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ByRPIObject (기본값)
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByRPObject
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByRPIObjectWithRecoveryTag
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmRecoveryServicesAsrTestFailoverJob** Cmdlet은 Azure Site Recovery 복제 보호 항목 또는 복구 계획의 장애 조치 테스트를 시작 합니다.
Get-AzureRmRecoveryServicesAsrJob cmdlet을 사용 하 여 작업 성공 여부를 확인할 수 있습니다.

## 예제의

### 예제 1
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

복구 계획에 대해 지정 된 매개 변수를 사용 하 여 테스트 장애 조치 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.

## 변수

### -Data Primarycertfile
보호 된 항목의 장애 조치 (failover)에 대 한 데이터 암호화 기본 인증서 파일 경로를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Data Secondarycertfile
보호 된 항목의 장애 조치 (failover)에 대 한 데이터 암호화 보조 인증서 파일 경로를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 방향
장애 조치 방향을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- PrimaryToRecovery
- RecoveryToPrimary

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PerformSourceSideAction
계획 되지 않은 장애 조치를 시작 하기 전에 원본 측에서 작업을 수행 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPlan
ASR 복구 계획 개체를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecoveryPoint
보호 된 컴퓨터를 장애 조치 (failover) 할 사용자 지정 복구 지점을 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryTag
장애 조치 (failover) 할 복구 태그를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent, Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent, Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationProtectedItem
Azure site recovery 복제 보호 항목을 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
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
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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

[Get-AzureRmRecoveryServicesAsrJob](./Get-AzureRmRecoveryServicesAsrJob.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e5864271e96add95624f857357defdea3039c7a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327984"
---
# Start-AzRecoveryServicesAsrPlannedFailoverJob

## SYNOPSIS
계획된 장애 조치(failover) 작업을 시작합니다.

## 구문

### ByRPIObject(기본값)
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByRPObject
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet은 Azure Site Recovery 복제 보호된 항목 또는 복구 계획에 대한 계획된 장애 조치(failover)를 시작합니다.
Get-AzRecoveryServicesAsrJob cmdlet을 사용하여 작업이 성공하는지 확인할 수 있습니다.

## 예제

### 예제 1
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

지정된 ASR 복구 계획에 대해 계획된 장애 조치(failover)를 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.

## PARAMETERS

### -CreateVmIfNotFound
주 지역(대체 위치 복구에 사용)으로 장애 복구하는 동안 가상 머신을 찾을 수 없는 경우 가상 머신을 생성합니다. 이 매개 변수에 허용되는 값은

- 예
- 아니요

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataEncryptionPrimaryCertFile
기본 인증서 파일을 지정합니다.

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

### -DataEncryptionSecondaryCertFile
보조 인증서 파일을 지정합니다.

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
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.


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

### -Direction
장애 조치(failover)의 방향을 지정합니다.
이 매개 변수에 허용되는 값은

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

### -Optimize
최적화할 것을 지정합니다.
이 매개 변수는 Azure 사이트에서 상당한 데이터 동기화가 필요한 Azure 사이트로 장애 조치(failover)가 수행될 때 적용됩니다.
유효한 값은

- ForDowntime
- ForSynchronization

**ForDowntime을** 지정하면 장애 조치(failover) 전에 데이터가 동기화되어 다운타임이 최소화됩니다.
동기화는 가상 머신을 종료하지 않고 수행됩니다.
동기화가 완료되면 작업이 일시 중단됩니다.
작업을 다시 시작하여 가상 머신을 종료하는 추가 동기화 작업을 실행합니다.

**ForSynchronization을** 지정하면 데이터 동기화가 최소화되도록 장애 조치(failover) 중에만 데이터가 동기화됩니다.
이 설정을 사용하도록 설정하면 가상 머신이 즉시 종료됩니다.
장애 조치(failover) 작업을 완료하기 위해 종료 후 동기화가 시작됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPlan
복구 계획에 해당하는 ASR 복구 계획 개체를 지정합니다.

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

### -ReplicationProtectedItem
복제 보호된 항목에 해당하는 ASR 복제 보호 항목 개체를 지정합니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServicesProvider
호스트에서 실행되는 ASR 서비스 공급자에 해당하는 ASR 서비스 공급자 개체를 지정하여 대체 위치로 장애 조치하는 동안 가상 머신을 만들 호스트를 식별합니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시 cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem

## 출력

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob

## 참고 사항

## 관련 링크

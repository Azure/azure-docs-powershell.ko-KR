---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E4F6D096-E265-49CF-AA73-E9C807F8383B
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0207d4b7eddfe56a8e4e86aac6899d19c10f44e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045556"
---
# Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan

## SYNOPSIS
레거시 컨테이너에 대 한 마이그레이션 계획을 가져옵니다.

## 구문과

```
Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan [-LegacyConfigId <String>]
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** cmdlet은 레거시 컨테이너에 대 한 마이그레이션 계획을 가져옵니다.
레거시 구성 ID를 기준으로 마이그레이션 계획을 지정 합니다.
마이그레이션 계획 만들기가 아직 진행 중인 경우이 cmdlet은 마이그레이션 계획의 상태를 가져옵니다.
마이그레이션 계획이 완료 되 면이 cmdlet은 레거시 컨테이너 집합에 대 한 실제 마이그레이션 계획을 반환 합니다.
*LegacyConfigId* 매개 변수를 지정 하지 않으면이 cmdlet은 구성 id 목록을 반환 합니다.

## 예제의

### 예제 1: 계획의 상태 가져오기
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 51e413fd-c2c9-4108-88cd-a0e792eab80a_PS
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 4c6398ef-35a0-4d1c-931e-d9d45599a97a_PS
VERBOSE: 2015-04-08 13:48:17 ClientRequestId: ef7a7e35-6dff-46cd-9df3-cb5fa25d149e_PS
VERBOSE: Request Id : fd7e502f273885468f633a44567bcb3f, HttpResponse OK
VERBOSE: List of volume containers: 


LegacyConfigId                    : f16463bd-94a9-4c3c-91c2-7a3ba7120087
DeviceName                        : ARUNKM-N4
MigrationTimeEstimationCompleted  : CloudConfigurationName        : OneSDKAzureCloud
                                    EstimatedTimeForLatestBackup  : 15Minutes
                                    EstimatedTimeForAllBackups    : 15Minutes
                                    These estimates are assuming 20 MBps bandwidth. Refer to migration guide to re-calculate for lower bandwidths. 



MigrationTimeEstimationInProgress : None
MigrationTimeEstimationFailed     : None
MigrationTimeEstimationNotStarted : None
```

이 명령은 마이그레이션 계획의 상태를 가져옵니다.
상태에는 가정 된 대역폭, 예상 시간 및 관련 정보가 포함 됩니다.

### 예제 2: 기존 요금제의 Id 가져오기
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 813da56c-0cfc-4325-80db-08ef32bdde1e_PS
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 9e7cf244-1894-490a-be02-749834a99318_PS
VERBOSE: List of LegacyConfig Ids on the resource: 

LegacyConfigId                                              DeviceName
--------------                                              ----------
1e1f10a0-3dff-4249-b847-4930061cd87a                        ARUNKM-N4
26d4096d-49b6-4102-b188-0446ece73c8b                        ARUNKM-N4
```

이 명령은 마이그레이션 계획의 모든 구성 Id를 가져옵니다.

## 변수

### -LegacyConfigId
레거시 기기의 구성에 대 한 고유 ID를 지정 합니다.

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

### -LegacyContainerNames
이 cmdlet이 마이그레이션 계획을 가져오는 볼륨 컨테이너 이름의 배열을 지정 합니다.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
Azure 프로필을 지정 합니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
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

### 않아야

## 출력

### MigrationPlanMsg
이 cmdlet은 마이그레이션 계획 작업의 상태, 초당 메가 비트의 가정 된 대역폭, 예상 시간 (분)을 포함 하는 **MigrationPlanMsg** 개체를 반환 합니다.

## 상속자

## 관련 링크

[시작-AzureStorSimpleLegacyVolumeContainerMigrationPlan](./Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)



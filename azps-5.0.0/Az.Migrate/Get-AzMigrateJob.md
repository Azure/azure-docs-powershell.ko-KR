---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226791"
---
# Get-AzMigrateJob

## SYNOPSIS
Azure 마이그레이션 작업의 상태를 검색 합니다.

## 구문과

### ListByName (기본값)
```
Get-AzMigrateJob -ProjectName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetById
```
Get-AzMigrateJob -JobID <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetByInputObject
```
Get-AzMigrateJob -InputObject <IJob> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetByName
```
Get-AzMigrateJob -JobName <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### ListById
```
Get-AzMigrateJob -ProjectID <String> -ResourceGroupID <String> [-SubscriptionId <String>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## 설명은
Get-AzMigrateJob cmdlet retrives Azure 마이그레이션 작업의 상태를 보고 합니다.

## 예제의

### 예제 1: 작업 Id로 가져오기
```powershell
PS C:\> Get-AzMigrateJob -JobID "/Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b" 

ActivityId                       : 68af14b4-46ae-48d1-b3e9-cdcffb9e8a93 ActivityId: 74d1a396-1d37-4264-8a5b-b727aaef0171
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 9/16/20 11:57:33 AM
Error                            : {}
FriendlyName                     : Associate replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/997e2a92-5afe-49c7-a81a-89660aec9b7b
Location                         :
Name                             : 997e2a92-5afe-49c7-a81a-89660aec9b7b
ScenarioName                     : AssociateProtectionProfile
StartTime                        : 9/16/20 11:57:32 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 42752b89-5fad-52fd-bf93-679fbdb6fed9
TargetObjectName                 : migrateAzMigratePWSHTc8d1sitepolicy
Task                             : {CloudPairingPrerequisitesCheck, CloudPairingPrepareSite}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

Id를 기준으로 작업을 검색 합니다.

### 예제 2: 리소스 그룹 및 프로젝트별 목록
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH'

ActivityId                       :
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         :
EndTime                          : 9/21/20 4:13:40 PM
Error                            : {}
FriendlyName                     : Update the virtual machine
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/1c89e38e-34ec-4903-aa7c-115201bf2de1
Location                         :
Name                             : 1c89e38e-34ec-4903-aa7c-115201bf2de1
ScenarioName                     : UpdateVmProperties
StartTime                        : 9/21/20 4:13:34 PM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionEntity
TargetObjectId                   : 593b735d-2a34-53b2-b8ed-e33da5650703
TargetObjectName                 : rb-w2k12r2-1
Task                             : {}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

프로젝트의 모든 작업을 가져옵니다.

### 예제 3: 리소스 그룹, 프로젝트 및 작업 이름으로 가져오기
```powershell
PS C:\> Get-AzMigrateJob -ResourceGroupName 'azmigratepwshtestasr13072020' -ProjectName 'AzMigrateTestProjectPWSH' -JobName 7ae1ee7c-442c-499d-8b0e-81d52a42b71e

ActivityId                       : 6986b7e5-0f1f-49d8-8b4b-77e6f66bcb92 ActivityId: eb73c6a1-7c66-469f-a853-d896aa38cc0f
AllowedAction                    : {}
CustomDetailAffectedObjectDetail : Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.JobDetailsAffectedObjectDetails
CustomDetailInstanceType         : AsrJobDetails
EndTime                          : 8/21/20 6:41:48 AM
Error                            : {}
FriendlyName                     : Create replication policy
Id                               : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Recover
                                   yServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationJobs/7ae1ee7c-442c-499d-8b0e-81d52a42b71e
Location                         :
Name                             : 7ae1ee7c-442c-499d-8b0e-81d52a42b71e
ScenarioName                     : AddProtectionProfile
StartTime                        : 8/21/20 6:41:48 AM
State                            : Succeeded
StateDescription                 : Completed
TargetInstanceType               : ProtectionProfile
TargetObjectId                   : 18b2ccec-e39a-517b-ae5d-dd395e9f4f96
TargetObjectName                 : samplePolicy3
Task                             : {AddProtectionProfilePreflightsCheckTask, AddProtectionProfileTask}
Type                             : Microsoft.RecoveryServices/vaults/replicationJobs
```

이는 특정 작업을 가져옵니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -필터
OData 필터 옵션

```yaml
Type: System.String
Parameter Sets: ListById, ListByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
복제 서버의 작업 개체를 지정 합니다.
생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob
Parameter Sets: GetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobID
세부 정보를 검색 해야 하는 작업 id를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
작업 식별자

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProjectID
서버가 복제 되는 Azure 마이그레이션 프로젝트를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProjectName
마이그레이션 프로젝트의 이름입니다.

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupID
현재 구독에서 Azure 마이그레이션 프로젝트의 리소스 그룹을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ListById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
복구 서비스 자격 증명 모음이 있는 리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: GetByName, ListByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Azure 구독 ID입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

## 출력

### Api20180110 작업을 위한. i a PowerShell.

## 상속자

별칭과

복합 매개 변수 속성

아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다. 해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.


INPUTOBJECT <IJob> : 복제 서버의 작업 개체를 지정 합니다.
  - `[Location <String>]`: 리소스 위치
  - `[ActivityId <String>]`: 활동 id입니다.
  - `[AllowedAction <String[]>]`: 작업에 허용 되는 작업입니다.
  - `[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: 원본 서버, 원본 클라우드, 대상 서버, 대상 클라우드 등과 같은 영향을 받는 개체 속성이 워크플로 개체 세부 정보를 기반으로 합니다.
    - `[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.
  - `[EndTime <DateTime?>]`: 종료 시간입니다.
  - `[Error <IJobErrorDetails[]>]`: 오류가 발생 했습니다.
    - `[CreationTime <DateTime?>]`: 작업 오류를 생성 하는 시간입니다.
    - `[ErrorLevel <String>]`: 오류 수준 오류입니다.
    - `[ProviderErrorDetailErrorCode <Int32?>]`: 오류 코드입니다.
    - `[ProviderErrorDetailErrorId <String>]`: 공급자 오류 Id입니다.
    - `[ProviderErrorDetailErrorMessage <String>]`: 오류 메시지입니다.
    - `[ProviderErrorDetailPossibleCaus <String>]`: 오류의 원인이 될 수 있습니다.
    - `[ProviderErrorDetailRecommendedAction <String>]`: 오류를 해결 하는 데 권장 되는 작업입니다.
    - `[ServiceErrorDetailActivityId <String>]`: 활동 Id입니다.
    - `[ServiceErrorDetailCode <String>]`: 오류 코드.
    - `[ServiceErrorDetailMessage <String>]`: 오류 메시지
    - `[ServiceErrorDetailPossibleCaus <String>]`: 오류가 발생할 수 있는 원인입니다.
    - `[ServiceErrorDetailRecommendedAction <String>]`: 오류를 해결 하는 데 권장 되는 작업입니다.
    - `[TaskId <String>]`: 작업의 Id입니다.
  - `[FriendlyName <String>]`: DisplayName입니다.
  - `[ScenarioName <String>]`: ScenarioName.
  - `[StartTime <DateTime?>]`: 시작 시간입니다.
  - `[State <String>]`: 작업의 상태입니다. NotStarted, InProgress, Succeeded, Failed, 취소 됨, 일시 중단 됨 또는 기타 값 중 하나입니다.
  - `[StateDescription <String>]`: 작업의 상태에 대 한 설명입니다. 예를 들어-성공 상태의 경우 설명은 완료, PartiallySucceeded, CompletedWithInformation 또는 건너뛸 수 있습니다.
  - `[TargetInstanceType <String>]`: Microsoft.Azure.SiteRecovery.V2015_11_10 {AffectedObjectType} 클래스인 영향을 받는 개체의 형식입니다.
  - `[TargetObjectId <String>]`: 영향을 받는 개체 Id입니다.
  - `[TargetObjectName <String>]`: 영향을 받는 개체의 이름입니다.
  - `[Task <IAsrTask[]>]`: 작업입니다.
    - `[AllowedAction <String[]>]`:이 작업에 해당 하는 상태/작업입니다.
    - `[CustomDetailInstanceType <String>]`: 작업 세부 정보 유형입니다.
    - `[EndTime <DateTime?>]`: 종료 시간입니다.
    - `[Error <IJobErrorDetails[]>]`: 작업 오류 세부 정보입니다.
    - `[FriendlyName <String>]`: 이름입니다.
    - `[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: 자식 작업입니다.
    - `[GroupTaskCustomDetailInstanceType <String>]`: 작업 세부 정보 유형입니다.
    - `[Name <String>]`: 고유한 작업 이름입니다.
    - `[StartTime <DateTime?>]`: 시작 시간입니다.
    - `[State <String>]`: 상태입니다. NotStarted, InProgress, Succeeded, Failed, 취소 됨, 일시 중단 됨 또는 기타 값 중 하나입니다.
    - `[StateDescription <String>]`: 작업 상태에 대 한 설명입니다. 예를 들어 성공 상태의 경우 설명은 완료, PartiallySucceeded, CompletedWithInformation 또는 건너뛸 수 있습니다.
    - `[TaskId <String>]`: Id입니다.
    - `[TaskType <String>]`: 작업 유형입니다. CustomDetails 속성의 세부 정보는이 형식에 따라 달라 집니다.

## 관련 링크


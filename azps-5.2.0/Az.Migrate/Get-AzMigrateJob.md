---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateJob.md
ms.openlocfilehash: bb28550a0b23fa9032832873a78771d25d2a38bd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330837"
---
# Get-AzMigrateJob

## SYNOPSIS
Azure Migrate 작업의 상태를 검색합니다.

## 구문

### ListByName(기본값)
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

## 설명
Get-AzMigrateJob cmdlet은 Azure Migrate 작업의 상태를 검색합니다.

## 예제

### 예제 1: 작업 ID로 얻기
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

ID로 작업을 검색합니다.

### 예제 2: 리소스 그룹 및 프로젝트로 나열
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

그러면 프로젝트의 모든 작업이 얻게 됩니다.

### 예제 3: 리소스 그룹, 프로젝트 및 작업 이름에 따라 얻기
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

특정 작업을 얻습니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Filter
OData 필터 옵션입니다.

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
복제 서버의 작업 개체를 지정합니다.
생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

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
세부 정보를 검색해야 하는 작업 ID를 지정합니다.

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
서버가 복제되는 Azure Migrate 프로젝트를 지정합니다.

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
현재 구독에서 Azure Migrate 프로젝트의 리소스 그룹을 지정합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IJob

## 참고 사항

별칭

복합 매개 변수 속성

아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.


INPUTOBJECT: 복제 서버의 <IJob> 작업 개체를 지정합니다.
  - `[Location <String>]`: 리소스 위치
  - `[ActivityId <String>]`: 활동 ID입니다.
  - `[AllowedAction <String[]>]`: 작업이 허용되는 작업입니다.
  - `[CustomDetailAffectedObjectDetail <IJobDetailsAffectedObjectDetails>]`: 워크플로 개체 세부 정보를 기반으로 원본 서버, 원본 클라우드, 대상 서버, 대상 클라우드와 같은 영향을 받는 개체 속성입니다.
    - `[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.
  - `[EndTime <DateTime?>]`: 종료 시간입니다.
  - `[Error <IJobErrorDetails[]>]`: 오류입니다.
    - `[CreationTime <DateTime?>]`: 작업 오류의 생성 시간입니다.
    - `[ErrorLevel <String>]`: 오류 수준입니다.
    - `[ProviderErrorDetailErrorCode <Int32?>]`: 오류 코드입니다.
    - `[ProviderErrorDetailErrorId <String>]`: 공급자 오류 ID입니다.
    - `[ProviderErrorDetailErrorMessage <String>]`: 오류 메시지입니다.
    - `[ProviderErrorDetailPossibleCaus <String>]`: 오류의 가능한 원인입니다.
    - `[ProviderErrorDetailRecommendedAction <String>]`: 오류를 해결하기 위한 권장 작업입니다.
    - `[ServiceErrorDetailActivityId <String>]`: 활동 ID입니다.
    - `[ServiceErrorDetailCode <String>]`: 오류 코드입니다.
    - `[ServiceErrorDetailMessage <String>]`: 오류 메시지입니다.
    - `[ServiceErrorDetailPossibleCaus <String>]`: 오류의 가능한 원인입니다.
    - `[ServiceErrorDetailRecommendedAction <String>]`: 오류를 해결하기 위한 권장 작업입니다.
    - `[TaskId <String>]`: 작업의 ID입니다.
  - `[FriendlyName <String>]`: DisplayName입니다.
  - `[ScenarioName <String>]`: ScenarioName입니다.
  - `[StartTime <DateTime?>]`: 시작 시간입니다.
  - `[State <String>]`: 작업의 상태입니다. NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended 또는 Other 값 중 하나입니다.
  - `[StateDescription <String>]`: 작업의 상태 설명입니다. 예: 성공 상태의 경우 설명은 Completed, PartiallySucceeded, CompletedWithInformation 또는 Skipped일 수 있습니다.
  - `[TargetInstanceType <String>]`: {Microsoft.Azure.SiteRecovery.V2015_11_10.AffectedObjectType} 클래스인 영향을 받는 개체의 형식입니다.
  - `[TargetObjectId <String>]`: 영향을 받는 개체 ID입니다.
  - `[TargetObjectName <String>]`: 영향을 받는 개체의 이름입니다.
  - `[Task <IAsrTask[]>]`: 작업.
    - `[AllowedAction <String[]>]`: 이 작업에 적용할 수 있는 상태/작업입니다.
    - `[CustomDetailInstanceType <String>]`: 작업 세부 정보의 유형입니다.
    - `[EndTime <DateTime?>]`: 종료 시간입니다.
    - `[Error <IJobErrorDetails[]>]`: 작업 오류 세부 정보입니다.
    - `[FriendlyName <String>]`: 이름입니다.
    - `[GroupTaskCustomDetailChildTask <IAsrTask[]>]`: 자식 작업입니다.
    - `[GroupTaskCustomDetailInstanceType <String>]`: 작업 세부 정보의 유형입니다.
    - `[Name <String>]`: 고유한 작업 이름입니다.
    - `[StartTime <DateTime?>]`: 시작 시간입니다.
    - `[State <String>]`: 상태입니다. NotStarted, InProgress, Succeeded, Failed, Cancelled, Suspended 또는 Other 값 중 하나입니다.
    - `[StateDescription <String>]`: 작업 상태 설명입니다. 예를 들어 성공 상태의 경우 설명은 Completed, PartiallySucceeded, CompletedWithInformation 또는 Skipped일 수 있습니다.
    - `[TaskId <String>]`: ID입니다.
    - `[TaskType <String>]`: 작업의 유형입니다. CustomDetails 속성의 세부 정보는 이 형식에 따라 다릅니다.

## 관련 링크


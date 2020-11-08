---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 694b9811bf11454e232f1514b59b1b537e4720a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214674"
---
# New-AzSynapseSqlPool

## SYNOPSIS
Synapse Analytics SQL 풀을 만듭니다.

## 구문과

### CreateByNameParameterSet (기본값)
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateFromBackupIdByNameParameterSet
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateFromBackupIdByParentObjectParameterSet
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### CreateFromBackupNameByNameParameterSet
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### CreateFromBackupNameByParentObjectParameterSet
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### CreateFromBackupInputObjectByNameParameterSet
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateFromRestorePointIdByNameParameterSet
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### CreateFromRestorePointIdByParentObjectParameterSet
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### CreateFromRestorePointNameByNameParameterSet
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateFromRestorePointNameByParentObjectParameterSet
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### CreateFromRestorePointInputObjectByNameParameterSet
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateByParentObjectParameterSet
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명은
**AzSynapseSqlPool** Cmdlet은 Azure SYNAPSE Analytics SQL 풀을 만듭니다.

## 예제의

### 예제 1
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

이 명령은 Azure Synapse Analytics SQL 풀을 만듭니다.

### 예제 2
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

이 명령은이 구독에 있는 모든 SQL 풀의 최신 백업에서 복원 하 여 Azure Synapse Analytics SQL 풀을 만듭니다.

### 예제 3
```powershell
PS C:\> New-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

이 명령은이 구독의 모든 SQL 풀에서 복원 지점을 활용 하 여 이전 상태에서 복구 하거나 복사 하 여 Azure Synapse Analytics SQL 풀을 만듭니다.

### 예제 4
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

이 명령은 리소스 ID를 사용 하 여이 구독에 있는 모든 SQL 풀의 가장 최근 백업에서 복원 하 여 Azure Synapse Analytics SQL 풀을 만듭니다.

### 예제 5
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws |  New-AzSynapseSqlPool -FromRestorePoint -Name dwsql0554 -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/mandywtest/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

이 명령은 리소스 ID를 사용 하 여 이전 상태에서 복구 하거나 복사 하기 위해이 구독에 있는 모든 SQL 풀의 복원 지점을 활용 하 여 Azure Synapse Analytics SQL 풀을 만듭니다.

## 변수

### -AsJob
백그라운드에서 cmdlet 실행

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackupResourceGroupName
만들 bakcup SQL 풀 개체의 자원 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackupResourceId
복원할 백업 SQL 풀 개체의 리소스 식별자입니다.

```yaml
Type: System.String
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackupSqlPoolName
만들 bakcup SQL 풀 개체의 이름입니다.

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Backupsqlpoo...
일반적으로 파이프라인을 통해 전달 되는 SQL 풀 입력 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackupWorkspaceName
Synapse에서 만들 bakcup SQL 풀 개체의 작업 영역 이름입니다.

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -데이터 정렬
데이터 정렬은 데이터를 정렬 및 비교 하는 규칙을 정의 하 고 SQL 풀을 만든 후에는 변경할 수 없습니다.
기본 데이터 정렬은 SQL_Latin1_General_CP1_CI_AS입니다.

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromBackup
이 구독에 있는 모든 SQL 풀의 최신 백업에서 복원을 나타냅니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromRestorePoint
이 구독에서 모든 SQL 풀의 복원 지점을 활용 하 여 이전 상태에서 복구 하거나 복사 하도록 지정 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
Synapse SQL 풀의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PerformanceLevel
SQL 풀에 할당할 SQL 서비스 계층 및 성능 수준입니다.
예를 DW2000c.

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestorePoint
스냅숏 복원 시간입니다.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceResourceGroupName
만들 원본 SQL 풀 개체의 리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceResourceId
만들 원본 SQL 풀 개체의 리소스 식별자입니다.

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceSqlPoolName
만들 원본 SQL 풀 개체의 이름입니다.

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceSqlPoolObject
일반적으로 파이프라인을 통해 전달 되는 SQL 풀 입력 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceWorkspaceName
Synapse 작업 영역에서 만들 원본 SQL 풀 개체의 이름입니다.

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 태그
리소스와 연결 된 태그의 문자열 사전입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -버전
Synapse SQL 풀의 버전입니다. 예를 들면 2 또는 3입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Synapse 작업 영역의 이름입니다.

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceObject
일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateByParentObjectParameterSet
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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### Synapse. PSSynapseWorkspace/.

## 출력

### Synapse. PSSynapseSqlPool/.

## 상속자

## 관련 링크

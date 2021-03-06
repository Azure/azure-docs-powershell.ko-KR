---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserverreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerReplica.md
ms.openlocfilehash: 5b201a035dbd919223d12c5205c4a154bc16fc2c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192097"
---
# New-AzMySqlFlexibleServerReplica

## SYNOPSIS
MySQL 유연한 서버에 대한 복제본 서버 생성

## 구문

```
New-AzMySqlFlexibleServerReplica -Replica <String> -ResourceGroupName <String> -Master <IServerAutoGenerated>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## 설명
기존 데이터베이스에서 새 복제본을 만듭니다.

## 예제

### 예제 1: 새 MySql 서버 복제본 만들기
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | New-AzMySqlFlexibleServerReplica -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName       SkuTier        
----               -------- ------------------ ------- ----------------------- -------       -------        
mysql-test-replica westus2   mysql_test         5.7     10240                   Standard_B1ms Burstable
```

이 cmdlet은 새 MySql 서버 복제본을 만듭니다.

### 예제 2: 새 MySql 서버 복제본 만들기
```powershell
PS C:\> $mysql = Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
PS C:\> New-AzMySqlFlexibleServerReplica -Master $mysql -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName       SkuTier        
----               -------- ------------------ ------- ----------------------- -------       -------        
mysql-test-replica westus2   mysql_test         5.7     10240                   Standard_B1ms Burstable
```

매개 변수 master(inputobject)가 있는 이 cmdlet은 새 MySql 서버 복제본을 만듭니다.

## PARAMETERS

### -AsJob
명령을 작업으로 실행합니다.

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

### -Master
복제본을 만들 원본 서버 개체입니다.
생성을 위해 MASTER 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoWait
명령을 비동기적으로 실행합니다.

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

### -Replica
서버의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicaServerName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스가 포함된 리소스 그룹의 이름입니다. Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.

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

### -SubscriptionId
Azure 구독을 식별하는 구독 ID입니다.

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
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

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

### Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated

## 출력

### Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated

## 참고 사항

별칭

복합 매개 변수 속성

아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다. 해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.


MASTER: <IServerAutoGenerated> 복제본을 만들 원본 서버 개체입니다.
  - `Location <String>`: 리소스가 있는 지리적 위치
  - `[Tag <ITrackedResourceTags>]`: 리소스 태그입니다.
    - `[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.
  - `[AdministratorLogin <String>]`: 서버의 관리자 로그인 이름입니다. 서버를 만들 때만 지정할 수 있습니다(생성에 필요).
  - `[AdministratorLoginPassword <String>]`: 관리자 로그인의 암호(서버 생성에 필요).
  - `[AvailabilityZone <String>]`: 서버의 가용성 영역 정보입니다.
  - `[CreateMode <CreateMode?>]`: 새 MySQL 서버를 만드는 모드입니다.
  - `[DelegatedSubnetArgumentSubnetArmResourceId <String>]`: 위임된 서브넷 arm 리소스 ID입니다.
  - `[HaEnabled <HaEnabledEnum?>]`: 서버에 대해 HA를 사용하도록 설정하거나 활성화하지 않습니다.
  - `[IdentityType <ResourceIdentityType?>]`: ID 유형입니다.
  - `[InfrastructureEncryption <InfrastructureEncryptionEnum?>]`: 서버가 인프라 암호화를 사용할 수 있는지 여부를 보여주는 상태입니다.
  - `[MaintenanceWindowCustomWindow <String>]`: 사용자 지정 창을 사용하도록 설정하거나 사용하지 않도록 설정하는지 여부를 나타냅니다.
  - `[MaintenanceWindowDayOfWeek <Int32?>]`: 유지 관리 기간에 대한 주일
  - `[MaintenanceWindowStartHour <Int32?>]`: 유지 관리 기간의 시작 시간
  - `[MaintenanceWindowStartMinute <Int32?>]`: 유지 관리 기간의 시작 분
  - `[PropertiesTag <IServerPropertiesTags>]`: 키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.
    - `[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.
  - `[ReplicationRole <String>]`: 복제 역할입니다.
  - `[RestorePointInTime <DateTime?>]`: 복원 지점 생성 시간(ISO8601 형식)으로 복원할 시간을 지정합니다.
  - `[SkuName <String>]`: SKU의 이름(예: Standard_D32s_v3.
  - `[SkuTier <SkuTier?>]`: 특정 SKU의 계층입니다(예: GeneralPurpose).
  - `[SourceServerId <String>]`: 원본 MySQL 서버 ID입니다.
  - `[SslEnforcement <SslEnforcementEnum?>]`: 서버에 연결할 때 ssl 적용을 사용하도록 설정하거나 설정하지 않습니다.
  - `[StorageProfileBackupRetentionDay <Int32?>]`: 서버에 대한 백업 보존 기간입니다.
  - `[StorageProfileStorageAutogrow <StorageAutogrow?>]`: 저장소 자동 증가를 사용하도록 설정
  - `[StorageProfileStorageIop <Int32?>]`: 서버에 대한 저장소 IOPS입니다.
  - `[StorageProfileStorageMb <Int32?>]`: 서버에 허용되는 최대 저장소입니다.
  - `[Version <ServerVersion?>]`: 서버 버전입니다.

## 관련 링크


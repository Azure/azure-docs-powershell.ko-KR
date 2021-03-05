---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: be1f2fc5c0aa2abda5f036580e377f05b26c2eb2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976304"
---
# New-AzSqlDatabaseFailoverGroup

## SYNOPSIS
이 명령은 새 Azure SQL 장애 조치(Failover) 그룹을 만듭니다.

## 구문

```
New-AzSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
지정된 서버에 SQL 데이터베이스 장애 조치(Failover) 그룹을 새로 만듭니다.
Azure SQL 데이터베이스 TDS 엔드포인트는 FailoverGroupName.SqlDatabaseDnsSuffix(예: FailoverGroupName.database.windows.net) 및 FailoverGroupName.secondary.SqlDatabaseDnsSuffix에서 만들어집니다. 이러한 엔드포인트는 장애 조치(Failover) 그룹의 기본 및 보조 서버에 각각 연결하는 데 사용할 수 있습니다. 주 서버가 중단의 영향을 받는 경우 장애 조치(Failover) 그룹의 장애 조치(failover) 정책 및 유예 기간에 따라 엔드포인트 및 데이터베이스의 자동 장애 조치(failover)가 트리거됩니다.
새로 만든 장애 조치(Failover) 그룹에는 데이터베이스가 포함되지 않습니다. 장애 조치 그룹에서 데이터베이스 집합을 제어하려면 'Add-AzSqlDatabaseToFailoverGroup' 및 'Remove-AzSqlDatabaseFromFailoverGroup' cmdlet을 사용합니다.
'-GracePeriodWithDataLosHours' 매개 변수에 대해 1시간보다 크거나 같은 값만 지원됩니다.

## 예제

### 예제 1
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

이 명령은 동일한 리소스 그룹의 두 서버에 대해 장애 조치(failover) 정책 '자동'이 있는 새 장애 조치(Failover) 그룹을 만듭니다.

### 예제 2
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

이 명령은 서로 다른 리소스 그룹의 두 서버에 대해 장애 조치(failover) 정책 '수동'이 있는 새 장애 조치(Failover) 그룹을 만듭니다.

## 매개 변수

### -AllowReadOnlyFailoverToPrimary
보조 서버의 중단이 읽기 전용 엔드포인트의 자동 장애 조치(failover)를 트리거해야 하는지 여부입니다. 이 기능은 아직 지원되지 않습니다.

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -FailoverGroupName
만들 데이터베이스 장애 조치 SQL Azure의 이름입니다.

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

### -FailoverPolicy
Azure 데이터베이스 장애 조치(failover) SQL 장애 조치(failover) 정책입니다.

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### -GracePeriodWithDataLossHours
주 서버에서 정전이 발생하고 데이터 손실 없이 장애 조치(failover)를 완료할 수 없는 경우 자동 장애 조치(failover)가 시작되기 전의 간격입니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerResourceGroupName
Azure 데이터베이스 장애 조치(Failover) 그룹의 보조 SQL 이름입니다.

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

### -PartnerServerName
Azure 데이터베이스 장애 조치(Failover) 그룹의 보조 SQL 이름입니다.

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

### -ResourceGroupName
리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
장애 조치(Failover) 그룹의 기본 Azure SQL 데이터베이스 서버의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel

## 참고 사항

## 관련 링크

[Set-AzSqlDatabaseFailoverGroup](./Set-AzSqlDatabaseFailoverGroup.md)

[Get-AzSqlDatabaseFailoverGroup](./Get-AzSqlDatabaseFailoverGroup.md)

[Add-AzSqlDatabaseToFailoverGroup](./Add-AzSqlDatabaseToFailoverGroup.md)

[Remove-AzSqlDatabaseFromFailoverGroup](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[Switch-AzSqlDatabaseFailoverGroup](./Switch-AzSqlDatabaseFailoverGroup.md)

[Remove-AzSqlDatabaseFailoverGroup](./Remove-AzSqlDatabaseFailoverGroup.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)

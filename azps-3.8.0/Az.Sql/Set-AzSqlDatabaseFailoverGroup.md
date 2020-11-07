---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 825d6f367fb4fbace53fccdb8798d17a915fc2bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878874"
---
# Set-AzSqlDatabaseFailoverGroup

## SYNOPSIS
Azure SQL Database 장애 조치 (Failover) 그룹의 구성을 수정 합니다.

## 구문과

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
이 명령은 Azure SQL Database 장애 조치 (Failover) 그룹의 구성을 수정 합니다.
명령 실행을 위해 장애 조치 그룹의 주 서버를 사용 해야 합니다.
그룹의 데이터베이스 집합을 제어 하려면 ' AzSqlDatabaseToFailoverGroup ' 및 ' Remove-AzSqlDatabaseFromFailoverGroup '을 대신 사용 합니다.
장애 조치 (Failover) 그룹 기능을 미리 보는 동안에는 '-GracePeriodWithDataLossHours ' 매개 변수에 대해 1 시간 보다 크거나 같은 값만 지원 됩니다.

## 예제의

### 예제 1
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

장애 조치 그룹의 장애 조치 정책을 ' 자동 '으로 설정 합니다.

### 예제 2
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

장애 조치 (failover) 그룹의 파이프를 통해 장애 조치 그룹의 장애 조치 정책을 ' 수동 '으로 설정 합니다.

## 변수

### -AllowReadOnlyFailoverToPrimary
보조 서버의 작동 중단이 읽기 전용 끝점의 자동 장애 조치를 트리거해야 하는지 여부 이 기능은 아직 지원 되지 않습니다.

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
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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
Azure SQL Database 장애 조치 (Failover) 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FailoverPolicy
Azure SQL Database 장애 조치 (Failover) 그룹의 장애 조치 정책

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
기본 서버에서 정전이 발생 하는 경우 자동 장애 조치가 시작 되는 간격입니다. 이는 유예 기간이 만료 되기 전에 Azure SQL Database가 자동 장애 조치를 시작 하지 않음을 나타냅니다. AllowDataLoss 옵션을 사용 하는 장애 조치 작업으로 인해 비동기 동기화의 특성상 데이터가 손실 될 수 있다는 점에 유의 하세요.

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
장애 조치 (Failover) 그룹의 기본 Azure SQL 데이터베이스 서버 이름입니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

## 출력

### AzureSqlFailoverGroupModel (*. *.)

## 상속자

## 관련 링크

[새로운 AzSqlDatabaseFailoverGroup](./New-AzSqlDatabaseFailoverGroup.md)

[Get-AzSqlDatabaseFailoverGroup](./Get-AzSqlDatabaseFailoverGroup.md)

[추가-AzSqlDatabaseToFailoverGroup](./Add-AzSqlDatabaseToFailoverGroup.md)

[제거-AzSqlDatabaseFromFailoverGroup](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[스위치-AzSqlDatabaseFailoverGroup](./Switch-AzSqlDatabaseFailoverGroup.md)

[제거-AzSqlDatabaseFailoverGroup](./Remove-AzSqlDatabaseFailoverGroup.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)

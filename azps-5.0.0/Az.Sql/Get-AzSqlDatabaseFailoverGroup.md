---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a2c7192fc1ce2055b05a4f943a0c04560f1e714e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226321"
---
# Get-AzSqlDatabaseFailoverGroup

## SYNOPSIS
Azure SQL 데이터베이스 장애 조치 (Failover) 그룹을 가져오거나 나열 합니다.

## 구문과

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
특정 Azure SQL 데이터베이스 장애 조치 그룹을 가져오거나 서버의 장애 조치 (Failover) 그룹을 나열 합니다.
장애 조치 (Failover) 그룹의 서버 중 하나를 사용 하 여 명령을 실행할 수 있습니다. 반환 된 값은 장애 조치 그룹과 관련 하 여 지정 된 서버의 상태를 반영 합니다.

## 예제의

### 예제 1
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

서버의 모든 장애 조치 (Failover) 그룹을 나열 합니다.

### 예제 2
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

특정 장애 조치 그룹을 가져옵니다.

### 예제 3
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

"Fg"로 시작 하는 서버의 모든 장애 조치 (failover) 그룹을 가져옵니다.

## 변수

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
검색할 Azure SQL Database 장애 조치 (Failover) 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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
장애 조치 (Failover) 그룹을 검색할 Azure SQL 데이터베이스 서버의 이름입니다.

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

[Set-AzSqlDatabaseFailoverGroup](./Set-AzSqlDatabaseFailoverGroup.md)

[추가-AzSqlDatabaseToFailoverGroup](./Add-AzSqlDatabaseToFailoverGroup.md)

[제거-AzSqlDatabaseFromFailoverGroup](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[스위치-AzSqlDatabaseFailoverGroup](./Switch-AzSqlDatabaseFailoverGroup.md)

[제거-AzSqlDatabaseFailoverGroup](./Remove-AzSqlDatabaseFailoverGroup.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)

---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a4440601610af0b55282cbe0e78209379f570edb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524856"
---
# Get-AzureRmSqlDatabaseFailoverGroup

## SYNOPSIS
Azure SQL 데이터베이스 장애 조치 (Failover) 그룹을 가져오거나 나열 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
특정 Azure SQL 데이터베이스 장애 조치 그룹을 가져오거나 서버의 장애 조치 (Failover) 그룹을 나열 합니다.

장애 조치 (Failover) 그룹의 서버 중 하나를 사용 하 여 명령을 실행할 수 있습니다. 반환 된 값은 장애 조치 그룹과 관련 하 여 지정 된 서버의 상태를 반영 합니다.

## 예제의

### 예제 1
```
PS C:\> $failoverGroups = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

서버의 모든 장애 조치 (Failover) 그룹을 나열 합니다.

### 예제 2
```
PS C:\> $failoverGroup = Get-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

특정 장애 조치 그룹을 가져옵니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FailoverGroupName
검색할 Azure SQL Database 장애 조치 (Failover) 그룹의 이름입니다.

```yaml
Type: String
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
Type: String
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
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### System. 개체

## 상속자

## 관련 링크

[새로운 AzureRmSqlDatabaseFailoverGroup](./New-AzureRmSqlDatabaseFailoverGroup.md)

[Set-AzureRmSqlDatabaseFailoverGroup](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[추가-AzureRmSqlDatabaseToFailoverGroup](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[제거-AzureRmSqlDatabaseFromFailoverGroup](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[스위치-AzureRmSqlDatabaseFailoverGroup](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[제거-AzureRmSqlDatabaseFailoverGroup](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)

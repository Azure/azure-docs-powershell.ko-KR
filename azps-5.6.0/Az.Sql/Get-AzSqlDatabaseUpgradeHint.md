---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: 9018dab5f09bbab6a3fb1197ee8aabd09141e664
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014672"
---
# Get-AzSqlDatabaseUpgradeHint

## SYNOPSIS
데이터베이스에 대한 가격 책정 계층 힌트를 얻습니다.

## 구문

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Get-AzSqlDatabaseUpgradeHint** cmdlet은 Azure SQL 업그레이드하기 위한 가격 책정 계층 힌트를 얻습니다.
웹 및 비즈니스 가격 책정 계층에 있는 데이터베이스는 새 기본, 표준 또는 프리미엄 가격 책정 계층으로 업그레이드할 힌트를 얻습니다.
이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서 지원됩니다.

## 예제

### 예제 1: 서버의 모든 데이터베이스에 대한 권장 사항 얻습니다.
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

이 명령은 Server01이라는 서버의 모든 데이터베이스에 대한 업그레이드 힌트를 반환합니다.

### 예제 2: 특정 데이터베이스에 대한 권장 사항 얻습니다.
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

이 명령은 특정 데이터베이스에 대한 업그레이드 힌트를 반환합니다.

### 예제 3: 탄력적 데이터베이스 풀에 없는 모든 데이터베이스에 대한 권장 사항 얻습니다.
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

이 명령은 탄력적 데이터베이스 풀에 없는 모든 데이터베이스에 대한 업그레이드 힌트를 반환합니다.

### 예제 4: 필터링을 사용하여 서버의 모든 데이터베이스에 대한 권장 사항 얻습니다.
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

이 명령은 "Database"로 시작하는 Server01이라는 서버의 모든 데이터베이스에 대한 업그레이드 힌트를 반환합니다.

## 매개 변수

### -DatabaseName
이 cmdlet에서 업그레이드 힌트를 SQL 데이터베이스의 이름을 지정합니다.
데이터베이스를 지정하지 않으면 이 cmdlet은 논리 서버의 모든 데이터베이스에 대한 힌트를 얻습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -ExcludeElasticPoolCandidates
탄력적 데이터베이스 풀의 데이터베이스가 반환된 권장 사항에서 제외되는지 여부를 나타냅니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.

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
이 cmdlet에서 업그레이드 힌트를 얻을 데이터베이스를 호스트하는 서버의 이름을 지정합니다.

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

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

### System.Boolean

## 출력

### Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties

## 참고 사항

## 관련 링크

[Get-AzSqlDatabaseExpanded](./Get-AzSqlDatabaseExpanded.md)

[Get-AzSqlElasticPoolRecommendation](./Get-AzSqlElasticPoolRecommendation.md)



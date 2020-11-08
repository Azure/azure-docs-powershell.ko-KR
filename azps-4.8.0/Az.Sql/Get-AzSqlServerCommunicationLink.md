---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 355690129f8edcda2586d2dfee570254ce44d998
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213238"
---
# Get-AzSqlServerCommunicationLink

## SYNOPSIS
데이터베이스 서버 간의 탄력적 데이터베이스 거래에 대 한 통신 링크를 가져옵니다.

## 구문과

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzSqlServerCommunicationLink** Cmdlet은 Azure SQL database의 탄력적 데이터베이스 트랜잭션에 대 한 서버 간 통신 링크를 가져옵니다.
해당 링크에 대 한 속성을 보려면 서버 통신 연결의 이름을 지정 합니다.

## 예제의

### 예제 1: 서버에 대 한 모든 통신 링크 가져오기
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

이 명령은 ContosoServer17 이라는 서버에 대 한 탄력적 데이터베이스 거래에 대 한 서버 간 통신 링크를 모두 가져옵니다.

### 예제 2: 서버에 대 한 특정 통신 링크 가져오기
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

이 명령은 Link01 이라는 서버 대 서버 통신 링크를 가져옵니다.

### 예제 3: 필터링을 사용 하 여 서버에 대 한 모든 통신 링크 가져오기
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

이 명령은 "ContosoServer17"로 시작 하는 서버에 대 한 탄력적 데이터베이스 거래에 대 한 서버 간 통신 링크를 모두 가져옵니다.

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

### -LinkName
이 cmdlet이 가져오는 서버 통신 링크의 이름을 지정 합니다.

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
*ServerName* 매개 변수에 지정 된 서버가 속한 리소스 그룹의 이름을 지정 합니다.

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
서버의 이름을 지정 합니다.
이 서버에는이 cmdlet이 가져오는 통신 링크가 포함 되어 있습니다.

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
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

## 출력

### ServerCommunicationLink. AzureSqlServerCommunicationLinkModel에 대 한

## 상속자
* 키워드: azure, azurerm, arm, resource, 관리, manager, sql, 데이터베이스, mssql

## 관련 링크

[새로운 AzSqlServerCommunicationLink](./New-AzSqlServerCommunicationLink.md)

[제거-AzSqlServerCommunicationLink](./Remove-AzSqlServerCommunicationLink.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)

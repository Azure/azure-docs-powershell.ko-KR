---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 0492b81e5674ea08ad98dff1fca75335b1ec8fa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531608"
---
# New-AzureRmSqlServerCommunicationLink

## SYNOPSIS
두 SQL 데이터베이스 서버 간의 탄력적 데이터베이스 트랜잭션에 대 한 통신 링크를 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmSqlServerCommunicationLink** Cmdlet은 Azure SQL 데이터베이스에 있는 두 논리 서버 간의 탄력적 데이터베이스 트랜잭션에 대 한 통신 링크를 만듭니다.
탄력적 데이터베이스 트랜잭션은 쌍으로 연결 된 서버 중 하나에서 데이터베이스를 확장할 수 있습니다.
서버에서 두 개 이상의 링크를 만들 수 있습니다.
따라서 탄력적 데이터베이스 트랜잭션은 많은 수의 서버에서 확장 될 수 있습니다.

## 예제의

### 예제 1: 통신 링크 만들기
```
PS C:\>New-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

이 명령은 ContosoServer17와 ContosoServer02 사이의 Link01 이라는 링크를 만듭니다.

## 변수

### -AsJob
백그라운드에서 cmdlet 실행
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -LinkName
이 cmdlet이 만드는 서버 통신 링크의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -또는 서버
이 통신 링크에 참여 하는 다른 서버의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
*ServerName* 매개 변수에 지정 된 서버가 속한 리소스 그룹의 이름을 지정 합니다.

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
이 cmdlet이 통신 링크를 설정 하는 서버의 이름을 지정 합니다.

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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### AzureSqlServerCommunicationLinkModel를 통해 서의 명령

## 상속자
* 키워드: azure, azurerm, arm, resource, 관리, manager, sql, 데이터베이스, mssql

## 관련 링크

[Get-AzureRmSqlServerCommunicationLink](./Get-AzureRmSqlServerCommunicationLink.md)

[제거-AzureRmSqlServerCommunicationLink](./Remove-AzureRmSqlServerCommunicationLink.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)

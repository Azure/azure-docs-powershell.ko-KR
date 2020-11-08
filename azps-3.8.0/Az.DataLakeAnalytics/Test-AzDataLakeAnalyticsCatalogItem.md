---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: ED17430D-4DAF-4B9E-937D-0F8A843DAB96
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: 2879923b38b6813213fe6819f84fa55a593f6930
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033993"
---
# Test-AzDataLakeAnalyticsCatalogItem

## SYNOPSIS
카탈로그 항목이 있는지 확인 합니다.

## 구문과

```
Test-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [-Path] <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzDataLakeAnalyticsCatalogItem** Cmdlet은 Azure Data Lake Analytics 카탈로그 항목이 있는지 확인 합니다.

## 예제의

### 예제 1: 카탈로그 항목이 있는지 테스트
```
PS C:\>Test-AzDataLakeAnalyticsCatalogItem -Account "ContosoAdlAccount" -ItemType Schema -Path "databaseName.schemaName"
```

이 명령은 지정 된 스키마 항목이 있는지 여부를 테스트 합니다.

## 변수

### -계정
Data Lake Analytics 계정 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -ItemType
확인할 항목의 카탈로그 항목 형식을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 데이터
- 스키마
- 어셈블리가
- 테이블로
- TablePartition
- Table의 Edfunction
- TableStatistics
- ExternalDataSource
- 보려고
- 절차
- 기밀
- 자격 증명
- 형식

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases:
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
가져올 항목의 경로 또는 나열할 항목의 상위 항목에 대 한 경로를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### DataLakeAnalytics. DataLakeAnalyticsEnums + CatalogItemType.

### DataLakeAnalytics. CatalogPathInstance/.

## 출력

### 시스템 부울

## 상속자

## 관련 링크

[Get-AzDataLakeAnalyticsCatalogItem](./Get-AzDataLakeAnalyticsCatalogItem.md)



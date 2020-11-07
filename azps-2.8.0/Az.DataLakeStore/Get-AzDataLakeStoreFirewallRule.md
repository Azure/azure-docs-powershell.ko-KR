---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 39450f979a4c79e453c66845b522aba91757f672
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696848"
---
# Get-AzDataLakeStoreFirewallRule

## SYNOPSIS
지정 된 Data Lake Store의 지정 된 방화벽 규칙을 가져옵니다.
방화벽 규칙이 지정 되지 않은 경우 계정에 대 한 모든 방화벽 규칙이 나열 됩니다.

## 구문과

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
Get-AzDataLakeStoreFirewallRule cmdlet은 지정 된 Data Lake Store에서 지정 된 방화벽 규칙을 가져옵니다.
방화벽 규칙이 지정 되지 않은 경우 계정에 대 한 모든 방화벽 규칙이 나열 됩니다.

## 예제의

### 예제 1: 특정 방화벽 규칙 검색
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

"ContosoADL" 계정의 "MyFirewallRule" 방화벽 규칙을 반환 합니다.

### 예제 2: 계정의 모든 방화벽 규칙 나열
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

계정 "ContosoADL"의 모든 방화벽 규칙을 반환 합니다.

## 변수

### -계정
방화벽 규칙을 검색할 Data Lake Store 계정입니다.

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

### -이름
검색할 방화벽 규칙의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
지정 된 계정의 지정 된 방화벽 규칙을 검색 하려는 리소스 그룹의 이름입니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### DataLakeStore. DataLakeStoreFirewallRule/.

## 상속자

## 관련 링크

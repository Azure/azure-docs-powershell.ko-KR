---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c387ebb089ab7f9dfddaee818f26596f34ed91e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536008"
---
# Get-AzureRmDataLakeStoreTrustedIdProvider

## SYNOPSIS
지정한 Data Lake Store에서 지정 된 신뢰할 수 있는 id 공급자를 가져옵니다.
공급자가 지정 되지 않은 경우 계정에 대 한 모든 공급자가 나열 됩니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmDataLakeStoreTrustedIdProvider** cmdlet은 지정 된 Data Lake store에서 지정 된 신뢰할 수 있는 id 공급자를 가져옵니다.
공급자가 지정 되지 않은 경우 계정에 대 한 모든 공급자가 나열 됩니다.

## 예제의

### 예제 1: 신뢰할 수 있는 특정 id 공급자 가져오기
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

"ContosoADL" 계정의 "MyProvider" 공급자를 반환 합니다.

### 예제 2: 계정의 모든 공급자 나열
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

계정 "ContosoADL"의 모든 공급자를 나열 합니다.

## 변수

### -계정
신뢰할 수 있는 id 공급자를 검색 하기 위한 Data Lake Store 계정

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
검색할 신뢰할 수 있는 id 공급자의 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
지정 된 계정의 신뢰할 수 있는 id 공급자를 검색 하려는 리소스 그룹의 이름입니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### DataLakeStoreTrustedIdProvider
지정 된 신뢰할 수 있는 id 공급자에 대 한 세부 정보입니다.

### IList<DataLakeStoreTrustedIdProvider>
지정 된 계정의 신뢰할 수 있는 id 공급자 목록입니다.

## 상속자

## 관련 링크


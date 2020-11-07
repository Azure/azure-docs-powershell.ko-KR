---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
ms.openlocfilehash: 1d31bff44bb93db1022a88a464c2942a2a3fadbb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703933"
---
# Get-AzureStorageTable

## SYNOPSIS
저장소 테이블을 나열 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### TableName (기본값)
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TablePrefix
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzureStorageTable** Cmdlet은 Azure의 저장소 계정과 연결 된 저장소 테이블을 나열 합니다.

## 예제의

### 예제 1: 모든 Azure Storage 테이블 나열
```
PS C:\>Get-AzureStorageTable
```

이 명령은 저장소 계정에 대 한 모든 저장소 테이블을 가져옵니다.

### 예제 2: 와일드 카드 문자를 사용 하 여 Azure Storage 테이블 나열
```
PS C:\>Get-AzureStorageTable -Name table*
```

이 명령은 와일드 카드 문자를 사용 하 여 이름이 table로 시작 하는 저장소 테이블을 가져옵니다.

### 예제 3: 테이블 이름 접두사를 사용 하 여 Azure Storage 테이블 나열
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

이 명령은 *Prefix* 매개 변수를 사용 하 여 이름이 table로 시작 하는 저장소 테이블을 가져옵니다.

## 변수

### -컨텍스트
저장소 컨텍스트를 지정 합니다.
이를 만들기 위해 New-AzureStorageContext cmdlet을 사용할 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
테이블 이름을 지정 합니다.
테이블 이름이 비어 있으면 cmdlet에 모든 테이블이 나열 됩니다.
그렇지 않으면 지정 된 이름 또는 일반 이름 패턴과 일치 하는 모든 테이블이 나열 됩니다.

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -접두사
가져오려는 테이블 이름에 사용 되는 접두사를 지정 합니다.
이를 사용 하 여 같은 문자열로 시작 하는 테이블 등의 모든 테이블을 찾을 수 있습니다.

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

### Microsoft. Azure. 일반. IStorageContext

## 출력

### WindowsAzure. ResourceModel를 AzureStorageTable로 저장 합니다.

## 상속자

## 관련 링크

[새로운 AzureStorageTable](./New-AzureStorageTable.md)

[제거-AzureStorageTable](./Remove-AzureStorageTable.md)



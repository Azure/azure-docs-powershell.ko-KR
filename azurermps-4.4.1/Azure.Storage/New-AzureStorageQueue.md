---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f6a9aff40d2cff62e683439b3f28f9e782b2de05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537939"
---
# New-AzureStorageQueue

## SYNOPSIS
저장소 큐를 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## 설명은
**AzureStorageQueue** Cmdlet은 Azure에서 저장소 큐를 만듭니다.

## 예제의

### 예제 1: Azure 저장소 큐 만들기
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

이 예제에서는 queueabc 라는 저장소 큐를 만듭니다.

### 예제 2: 여러 azure storage 큐 만들기
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

이 예제에서는 여러 저장소 큐를 만듭니다.
.NET 문자열 클래스의 Split 메서드를 사용 하 고 파이프라인의 이름을 전달 합니다.

## 변수

### -컨텍스트
Azure 저장소 컨텍스트를 지정 합니다.
New-AzureStorageContext cmdlet을 사용 하 여 만들 수 있습니다.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -이름
큐의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### IStorageContext

' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.

### 이름

' Name ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.

## 출력

### WindowsAzure. ResourceModel를 AzureStorageQueue로 저장 합니다.

## 상속자

## 관련 링크

[Get-AzureStorageQueue](./Get-AzureStorageQueue.md)

[제거-AzureStorageQueue](./Remove-AzureStorageQueue.md)



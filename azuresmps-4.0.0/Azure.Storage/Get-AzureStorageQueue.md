---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 11a8ffe26a65bf2ecabab7807d8e54bc23b629fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524023"
---
# Get-AzureStorageQueue

## SYNOPSIS
저장소 큐를 나열 합니다.

## 구문과

### QueueName (기본값)
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### QueuePrefix
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## 설명은
**AzureStorageQueue** Cmdlet은 Azure 저장소 계정과 연결 된 저장소 큐를 나열 합니다.

## 예제의

### 예제 1: 모든 Azure Storage 큐 나열
```
PS C:\>Get-AzureStorageQueue
```

이 명령은 현재 저장소 계정에 대 한 모든 저장소 큐의 목록을 가져옵니다.

### 예제 2: 와일드 카드 문자를 사용 하 여 Azure Storage 큐 나열
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

이 명령은 와일드 카드 문자를 사용 하 여 이름이 대기열로 시작 하는 저장소 대기열 목록을 가져옵니다.

### 예제 3: 큐 이름 접두사를 사용 하 여 Azure Storage 큐 나열
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

이 예제에서는 *Prefix* 매개 변수를 사용 하 여 이름이 대기열로 시작 하는 저장소 대기열 목록을 가져옵니다.

## 변수

### -컨텍스트
Azure 저장소 컨텍스트를 지정 합니다.
**새로운-AzureStorageContext** cmdlet을 사용 하 여 만들 수 있습니다.

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
이름을 지정 합니다.
이름을 지정 하지 않으면 cmdlet에서 모든 큐의 목록을 가져옵니다.
전체 또는 일부 이름을 지정한 경우 cmdlet은 이름 패턴과 일치 하는 모든 큐를 가져옵니다.

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -접두사
가져오려는 큐 이름에 사용 되는 접두사를 지정 합니다.

```yaml
Type: String
Parameter Sets: QueuePrefix
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

## 출력

## 상속자

## 관련 링크

[새로운 AzureStorageQueue](./New-AzureStorageQueue.md)

[제거-AzureStorageQueue](./Remove-AzureStorageQueue.md)



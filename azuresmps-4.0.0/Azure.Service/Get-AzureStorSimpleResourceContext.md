---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046549"
---
# Get-AzureStorSimpleResourceContext

## SYNOPSIS
현재 리소스 컨텍스트를 가져옵니다.

## 구문과

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Get-AzureStorSimpleResourceContext** cmdlet은 현재 리소스 컨텍스트를 가져옵니다.

## 예제의

### 예제 1: 현재 컨텍스트 가져오기
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

첫 번째 명령은 **-Azurestorsimplerazurecmdlet** 을 사용 하 여 Contoso63-Tsqa 라는 리소스로 현재 컨텍스트를 설정 합니다.

두 번째 명령은 현재 리소스 컨텍스트를 가져옵니다.

### 예제 2: 현재 컨텍스트 가져오기 시도
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

이 명령은 현재 컨텍스트를 가져옵니다.
이 예제에서는 컨텍스트가 설정 되지 않았습니다.
이 명령은 문제를 설명 하는 메시지를 반환 합니다.

## 변수

### -프로필
Azure 프로필을 지정 합니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### StorSimpleResourceContext
이 cmdlet은 **Resourcecontext** 개체를 반환 합니다.

## 상속자

## 관련 링크

[Get-AzureStorSimpleResource](./Get-AzureStorSimpleResource.md)

[선택-AzureStorSimpleResource](./Select-AzureStorSimpleResource.md)



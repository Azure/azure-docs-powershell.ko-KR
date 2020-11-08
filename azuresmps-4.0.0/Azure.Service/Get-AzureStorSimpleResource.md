---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 482E8CD6-C38F-4BD5-8214-016D0D8C7FD0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6381b8e0fac5ebf047122f131af6087d5bb5a9fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045554"
---
# Get-AzureStorSimpleResource

## SYNOPSIS
만든 모든 리소스를 가져옵니다.

## 구문과

```
Get-AzureStorSimpleResource [-ResourceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Get-AzureStorSimpleResource** Cmdlet는 Azure 포털을 사용 하 여 만든 모든 리소스를 가져옵니다.
Cmdlet은 리소스에 연결 하는 데 사용할 수 있는 세부 정보를 가져옵니다.

## 예제의

### 예제 1: 모든 리소스 가져오기
```
PS C:\>Get-AzureStorSimpleResource
VERBOSE: ClientRequestId: 5cd61b91-ef40-43b4-986d-156e06d2ed65_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    8838459798595306468  Started
Contoso68-Tsqa                                    2859070203638134681  Started
Contoso73-Tsqa                                    7871392677286863733  Started
Contoso87-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 4 StorSimple resources.
```

이 명령은 만든 모든 리소스를 가져옵니다.
이 예제에는 세 개의 리소스가 있습니다.

### 예제 2: 이름을 사용 하 여 리소스 가져오기
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa"
VERBOSE: ClientRequestId: efc3c85c-12aa-4345-b6eb-ccc532de4825_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 1 StorSimple resource.
```

이 명령은 Contoso63 라는 리소스를 가져옵니다.

### 예제 3: 존재 하지 않는 리소스 가져오기 시도
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
VERBOSE: ClientRequestId: 5d08d40b-f9d7-4d43-956f-13f01e89625b_PS
VERBOSE: Invalid input : Could not find a resource named Contoso64-Tsqa in your subscription.
```

이 명령은 Contoso64 라는 리소스를 가져오려고 시도 합니다.
이 이름을 가진 리소스가 없습니다.
이 예제는 리소스를 반환 하지 않습니다.

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

### -Context.resourcename
이 cmdlet이 가져오는 리소스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### IEnumerable \<ResourceCredentials\> , ResourceCredentials
이 cmdlet은 다음 속성을 포함 하는 **ResourceCredentials** 개체를 반환 합니다. 

- **Context.resourcename**
- **ResouceId**
- **ResourceState**

## 상속자

## 관련 링크

[Get-AzureStorSimpleResourceContext](./Get-AzureStorSimpleResourceContext.md)

[선택-AzureStorSimpleResource](./Select-AzureStorSimpleResource.md)



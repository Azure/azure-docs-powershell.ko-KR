---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046552"
---
# Get-AzureStorSimpleAccessControlRecord

## SYNOPSIS
서비스 구성의 액세스 제어 레코드를 가져옵니다.

## 구문과

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureStorSimpleAccessControlRecord** Cmdlet은 StorSimple Manager 서비스 구성에서 액세스 제어 레코드를 가져옵니다.
이 cmdlet은 모든 레코드 또는 명명 된 레코드를 가져옵니다.

액세스 제어 레코드는 iSCSI 초기자 매개 변수의 컨테이너입니다.
이러한 매개 변수는 볼륨에 액세스할 수 있는 초기자를 지정 합니다.
ISCSI 초기자가 볼륨에 대 한 연결을 시도 하면 기기는 해당 볼륨에 할당 된 액세스 제어 레코드를 확인 합니다.
ISCSI 초기자 매개 변수가 해당 볼륨에 매핑된 액세스 제어 레코드의 항목 중 하 나와 일치 하는 경우 iSCSI 초기자가 연결할 수 있습니다.

## 예제의

### 예제 1: 모든 액세스 제어 레코드 가져오기
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

이 명령은 모든 액세스 제어 레코드를 가져옵니다.

### 예제 2: 특정 액세스 제어 레코드 가져오기
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

이 명령은 Acr11 이라는 액세스 제어 레코드를 가져옵니다.

## 변수

### -ACRName
가져올 액세스 제어 레코드의 이름을 지정 합니다.

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

### AccessControlRecord, IList\<AccessControlRecord\>
이 cmdlet은 **Accesscontrolrecord** 개체 또는 **\<AccessControlRecord\> IList** 개체를 반환 합니다.
**Accesscontrolrecord** 개체에는 다음 필드가 포함 되어 있습니다. 

- **Globalid** ( **String** ) 
- **InitiatorName** ( **String** ) 
- **InstanceId** ( **String** ) 
- **Name** ( **String** ) 
- **Operationinprogress** ( **operationinprogress** ) 
- **(** **Int** ).

## 상속자

## 관련 링크

[새로운 AzureStorSimpleAccessControlRecord](./New-AzureStorSimpleAccessControlRecord.md)

[제거-AzureStorSimpleAccessControlRecord](./Remove-AzureStorSimpleAccessControlRecord.md)

[Set-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)



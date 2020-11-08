---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046532"
---
# Get-AzureVMImage

## SYNOPSIS
하나 또는 여러 운영 체제 목록 또는 이미지 리포지토리의 가상 컴퓨터 이미지에 대 한 속성을 가져옵니다.

## 구문과

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**AzureVMImage** cmdlet은 하나 또는 여러 운영 체제 또는 이미지 리포지토리의 가상 컴퓨터 이미지 목록에 대 한 속성을 가져옵니다.
Cmdlet은 리포지토리의 모든 이미지에 대 한 정보를 반환 하거나, 해당 이미지 이름을 제공 하는 경우 특정 이미지에 대 한 정보를 반환 합니다.

## 예제의

### 예제 1: 현재 이미지 리포지토리에서 특정 이미지 개체를 가져옵니다.
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

이 명령은 현재 이미지 리포지토리에서 Image001 이라는 이미지 개체를 가져옵니다.

### 예제 2: 현재 이미지 리포지토리에서 모든 이미지 가져오기
```
PS C:\> Get-AzureVMImage
```

이 명령은 현재 이미지 리포지토리에서 모든 이미지를 검색 합니다.

### 예제 3: 구독 컨텍스트를 설정한 다음 모든 이미지 가져오기
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

이 명령은 구독 컨텍스트를 설정한 다음 이미지 리포지토리에서 모든 이미지를 검색 합니다.

## 변수

### -ImageName
이미지 리포지토리에서 운영 체제 또는 가상 컴퓨터 이미지의 이름을 지정 합니다.
이 매개 변수를 지정 하지 않으면 모든 이미지가 반환 됩니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 하기로
- 숨기기
- Inquire
- SilentlyContinue
- 중지가
- 대기

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
정보 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

## 출력

## 상속자

## 관련 링크

[추가-AzureVMImage](./Add-AzureVMImage.md)

[제거-AzureVMImage](./Remove-AzureVMImage.md)

[저장-AzureVMImage](./Save-AzureVMImage.md)

[업데이트-AzureVMImage](./Update-AzureVMImage.md)



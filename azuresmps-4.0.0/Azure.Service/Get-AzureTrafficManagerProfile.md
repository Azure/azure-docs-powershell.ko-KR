---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045536"
---
# Get-AzureTrafficManagerProfile

## SYNOPSIS
Traffic Manager 프로필의 세부 정보를 가져옵니다.

## 구문과

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureTrafficManagerProfile** Cmdlet은 Microsoft Azure 트래픽 관리자 프로필의 세부 정보를 가져옵니다.
*Name* 매개 변수를 지정 하지 않으면 cmdlet은 현재 구독의 Traffic Manager 프로필을 나열 합니다.

## 예제의

### 예제 1: 구독에서 Traffic Manager 프로필 목록 가져오기
```
PS C:\>Get-AzureTrafficManagerProfile
```

이 명령은 구독에서 Traffic Manager 프로필의 목록을 가져옵니다.

### 예제 2: Traffic Manager 프로필 가져오기
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

이 명령은 MyProfile 이라는 Traffic Manager 프로필을 가져옵니다.

### 예제 3: Traffic Manager 프로필에 끝점 추가
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

이 명령은 Traffic Manager 프로필에 끝점을 추가한 다음 프로필을 저장 합니다.

## 변수

### -이름
가져올 Traffic Manager 프로필의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다. 프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

### WindowsAzure. TrafficManager. 유틸리티. IProfileWithDefinition
이 cmdlet은 Traffic Manager 프로필 개체를 생성 합니다.

## 상속자

## 관련 링크

[추가-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[새로운 AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[제거-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)



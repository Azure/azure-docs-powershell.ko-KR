---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046375"
---
# Enable-AzureTrafficManagerProfile

## SYNOPSIS
Traffic Manager 프로필을 사용 하도록 설정 합니다.

## 구문과

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
AzureTrafficManagerProfile cmdlet을 **사용** 하면 Microsoft Azure Traffic Manager 프로필을 사용할 수 있습니다.
작업의 성공 여부를 표시 하는 *PassThru* 매개 변수를 지정 합니다.

## 예제의

### 예제 1: Traffic Manager 프로필 사용
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

이 명령은 MyProfile 이라는 Traffic Manager 프로필을 사용 하도록 설정 합니다.

### 예제 2: Traffic Manager 프로필을 사용 하도록 설정 하 고 결과 표시
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

이 명령은 MyProfile 이라는 Traffic Manager 프로필을 사용 하도록 설정 하 고 명령이 성공적으로 수행 되었는지 여부를 표시 합니다.

## 변수

### -이름
사용할 Traffic Manager 프로필의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
작업이 성공한 경우 $True를 반환 하 고, 그렇지 않으면 그렇지 않으면 $False 합니다.
기본적으로이 cmdlet은 출력을 생성 하지 않습니다.

```yaml
Type: SwitchParameter
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

### 시스템 부울
이 cmdlet은 $True 또는 $False를 생성 합니다.
작업이 성공 하 고 *PassThru* 매개 변수를 지정 하면이 cmdlet은 $True 값을 반환 합니다.

## 상속자

## 관련 링크

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[새로운 AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[제거-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)



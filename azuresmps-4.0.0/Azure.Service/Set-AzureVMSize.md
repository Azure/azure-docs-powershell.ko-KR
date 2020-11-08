---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 437889D1-F24F-4BBE-8C56-7C3E48CEA517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86dd38ce7fa55507be3362c1494b88df491a1067
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045791"
---
# Set-AzureVMSize

## SYNOPSIS
Azure 가상 컴퓨터의 크기를 설정 합니다.

## 구문과

```
Set-AzureVMSize [-InstanceSize] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**AzureVMSize** cmdlet은 가상 컴퓨터의 크기를 업데이트 합니다.
이 파일에는 가상 컴퓨터의 새 크기인 *InstanceSize* 와 **get-help** cmdlet을 사용 하 여 검색 되는 가상 머신 개체인 *VM* 이라는 두 개의 매개 변수가 있습니다.
**Set-AzureVMSize** 결과를 **업데이트-add-azurevm** cmdlet으로 파이프 하거나 나중에 사용 하기 위해 변수에 저장할 수 있습니다.
**업데이트-add-azurevm** 를 실행할 때 까지는 실제 변경 내용이 적용 되지 않습니다.

참고:이 cmdlet은 가상 컴퓨터를 다시 프로 비전 해야 하며 새 IP 주소를 받을 수 있습니다.

## 예제의

### 예제 1: 가상 컴퓨터의 크기 설정
```
PS C:\> Get-AzureVM -ServiceName "MySvc1" -Name "MyVM3" | Set-AzureVMSize "Small" | Update-AzureVM
```

이 명령은 가상 컴퓨터를 "Small" 크기로 업데이트 합니다.

## 변수

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

### -InstanceSize
가상 컴퓨터의 크기를 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

--ExtraSmall--작음--보통--큼--높음--ExtraLarge--A5--A6--A7

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -VM
이 cmdlet이 크기를 설정 하는 영구 가상 컴퓨터 개체를 지정 합니다.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[다운로드-Add-azurevm](./Get-AzureVM.md)

[업데이트-Add-azurevm](./Update-AzureVM.md)



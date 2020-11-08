---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 61CF7F95-F0BB-4282-A971-537CB73708B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d5774213054f3e9e56e9804a9319e31f095f868
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045547"
---
# Get-AzureStoreAddOn

## SYNOPSIS
사용할 수 있는 Azure Store 추가 기능을 가져옵니다.

## 구문과

### ListAvailable
```
Get-AzureStoreAddOn [-ListAvailable] [-Country <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### GetAddOn
```
Get-AzureStoreAddOn [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

Azure Store에서 구입 하는 데 사용할 수 있는 추가 기능을 모두 가져오거나 현재 구독에 대 한 기존 추가 기능 인스턴스를 가져옵니다.

## 예제의

### 예제 1
```
PS C:\> Get-AzureStoreAddOn
```

이 예제에서는 현재 구독에 대해 구매한 모든 추가 기능 인스턴스를 가져옵니다.

### 예제 2
```
PS C:\> Get-AzureStoreAddOn -ListAvailable
```

이 예제에서는 Azure Store에서 미국에서 구매할 수 있는 모든 추가 기능을 가져옵니다.

### 예제 3
```
PS C:\> Get-AzureStoreAddOn -Name MyAddOn
```

이 예제에서는 현재 구독의 구매한 추가 기능 인스턴스에서 MyAddOn 이라는 추가 기능을 가져옵니다.

## 변수

### -국가
지정 된 경우 지정 된 국가에서 사용 가능한 Azure Store 추가 기능 인스턴스만 반환 합니다.
기본값은 "US"입니다.

```yaml
Type: String
Parameter Sets: ListAvailable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ListAvailable
지정 하는 경우 Azure Store에서 구매할 수 있는 추가 기능을 가져옵니다.

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
지정 된 이름과 일치 하는 추가 기능을 반환 합니다.

```yaml
Type: String
Parameter Sets: GetAddOn
Aliases: 

Required: False
Position: Named
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[새-Azure추가 기능](./New-AzureStoreAddOn.md)

[-Azure추가 기능 제거](./Remove-AzureStoreAddOn.md)

[Set-Azure기능 추가 기능](./Set-AzureStoreAddOn.md)



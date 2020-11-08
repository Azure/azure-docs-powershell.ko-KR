---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BFB57100-93F6-4FD2-8ECA-7F54BEB0D6B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7114f39ee2b105c80429151df8347b5c17dcfea0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046506"
---
# Get-AzureWebsiteLog

## SYNOPSIS
지정 된 웹 사이트의 로그를 가져옵니다.

## 구문과

### 있음
```
Get-AzureWebsiteLog [-Path <String>] [-Message <String>] [-Tail] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ListPath
```
Get-AzureWebsiteLog [-ListPath] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

지정 된 웹 사이트의 로그를 가져옵니다.

## 예제의

### 예제 1: 스트리밍 로그 시작
```
PS C:\> Get-AzureWebsiteLog -Tail
```

이 예제에서는 모든 응용 프로그램 로그에 대 한 로깅 스트리밍을 시작 합니다.

### 예제 2: http 로그에 대 한 스트리밍 로그 시작
```
PS C:\> Get-AzureWebsiteLog -Tail -Path http
```

이 예제에서는 http 로그에 대 한 로그 스트리밍을 시작 합니다.

### 예제 3: 오류 로그에 대 한 스트리밍 로그 시작
```
PS C:\> Get-AzureWebsiteLog -Tail -Message Error
```

이 예제에서는 로그 스트리밍을 시작 하 고 오류 로그만 표시 합니다.

### 예제 4: avaiable 로그 표시
```
PS C:\> Get-AzureWebsiteLog -Name MyWebsite -ListPath
```

이 예제에서는 웹 사이트에서 사용할 수 있는 모든 로그 경로를 나열 합니다.

## 변수

### -ListPath
로그 경로를 나열할 지 여부를 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: ListPath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -메시지
로그 메시지를 필터링 하는 데 사용 되는 문자열을 지정 합니다.
이 문자열이 포함 된 로그만 검색 됩니다.

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
웹 사이트의 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
로그를 검색 하는 경로입니다.
기본적으로 루트 이며, 모든 경로가 포함 됨을 의미 합니다.

```yaml
Type: String
Parameter Sets: Tail
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

### -슬롯
슬롯 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -꼬리
로그를 스트림할 지 여부를 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: Tail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureWebsite](./Get-AzureWebsite.md)

[새로운 AzureWebsite](./New-AzureWebsite.md)

[제거-AzureWebsite](./Remove-AzureWebsite.md)

[시작-AzureWebsite](./Start-AzureWebsite.md)



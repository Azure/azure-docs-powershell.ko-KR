---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6B406310-287F-4BD3-BA38-A9C97E8EDC45
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9f68ca1667e7b028c7646bf5a569e4e467c1b03
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046273"
---
# Get-AzureWebsiteJob

## SYNOPSIS
웹 사이트와 연결 된 웹 작업을 가져옵니다.

## 구문과

```
Get-AzureWebsiteJob [-JobName <String>] [-JobType <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
웹 사이트와 연결 된 웹 작업을 가져옵니다.

## 예제의

### 예제 1: 특정 웹 작업 정보 가져오기
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

MyWebsite 프로덕션 슬롯에서 MyWebJob 이라고 하는 웹 작업을 가져옵니다.

### 예제 2: 웹 사이트에 대 한 모든 웹 작업 가져오기
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite
```

MyWebsite 프로덕션 슬롯에 연결 된 모든 웹 작업을 가져옵니다.

### 예제 3: 트리거된 모든 웹 작업 가져오기
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -Slot staging -Type Triggered
```

MyWebsite의 스테이징 슬롯에서 트리거된 모든 웹 작업을 가져옵니다.

## 변수

### -JobName
웹 작업 이름

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

### -JobType
웹 작업 유형입니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 되었을
- 연속적

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

### -이름
Azure 웹 사이트의 이름입니다.

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
Azure 웹 사이트의 슬롯 이름입니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureWebsite](./Get-AzureWebsite.md)

[새로운 AzureWebsiteJob](./New-AzureWebsiteJob.md)

[제거-AzureWebsiteJob](./Remove-AzureWebsiteJob.md)

[시작-AzureWebsiteJob](./Start-AzureWebsiteJob.md)

[중지-AzureWebsiteJob](./Stop-AzureWebsiteJob.md)



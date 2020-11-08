---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: DF12406D-894C-4732-95EE-D75524023B82
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2e6596c0de702175927f51bfd70fc5271b13bfd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045980"
---
# New-AzureSchedulerJobCollection

## SYNOPSIS
스케줄러 작업 컬렉션을 만듭니다.

## 구문과

```
New-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

**AzureSchedulerJobCollection** cmdlet은 스케줄러 작업 컬렉션을 만듭니다.
*Plan* 매개 변수에 대 한 값을 지정 하지 않으면 cmdlet이 표준 작업 컬렉션을 만듭니다.

## 예제의

### 예제 1: 기본 값이 포함 된 스케줄러 작업 컬렉션 만들기
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection01" -Location "North Central US" -Plan "Standard"
```

이 명령은 JobCollection01 이라는 표준 스케줄러 작업 컬렉션을 만듭니다.
새 컬렉션에는 표준 스케줄러 작업 모음에 대 한 기본 작업 수 및 최대 되풀이 값이 있습니다.

### 예제 2: 지정 된 값을 사용 하 여 스케줄러 작업 컬렉션 만들기
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection02" -Location "North Central US" -Frequency "Hour" -Interval 12 -MaxJobCount 30 -Plan "Standard"
```

이 명령은 JobCollection02 이라는 표준 스케줄러 작업 컬렉션을 만듭니다.
새 컬렉션의 최대 작업 수는 30이 고 최대 되풀이 시간은 시간 당 12입니다.

## 변수

### -빈도
이 스케줄러 작업 컬렉션의 모든 작업에 지정할 수 있는 최대 빈도를 지정 합니다.

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

### -Interval
*Frequency* 매개 변수를 사용 하 여 지정 된 빈도로 되풀이 간격을 지정 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobCollectionName
새 스케줄러 작업 컬렉션의 이름을 지정 합니다.

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

### -위치
클라우드 서비스를 호스트 하는 위치의 이름을 지정 합니다.
유효한 값은 다음과 같습니다. 

- 아시아 어디서 나
- 유럽 어디서 나
- 미국 어디서 나
- 동아시아
- 미국 동부
- 대한민국 미국 중부
- 동유럽
- 미국 중부 US
- 동남 아시아
- 유럽 서유럽
- 미국 서 부

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxJobCount
스케줄러 작업 컬렉션에서 만들 수 있는 최대 작업 수를 지정 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -계획
스케줄러 작업 컬렉션 계획을 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureSchedulerJobCollection](./Get-AzureSchedulerJobCollection.md)

[제거-AzureSchedulerJobCollection](./Remove-AzureSchedulerJobCollection.md)

[Set-AzureSchedulerJobCollection](./Set-AzureSchedulerJobCollection.md)



---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DBB3DD-B02D-4288-89CB-550EBECC2E79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4373e4eed8524db1dd5311778b3e297e766c74dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045443"
---
# Set-AzureSchedulerJobCollection

## SYNOPSIS
스케줄러 작업 컬렉션을 업데이트 합니다.

## 구문과

```
Set-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

**AzureSchedulerJobCollection** cmdlet은 스케줄러 작업 컬렉션을 업데이트 합니다.

## 예제의

### 예제 1: 컬렉션의 최대 작업 수 변경
```
PS C:\> Set-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -MaxJobCount 30
```

이 명령은 JobCollection01 이라는 기존 스케줄러 작업 컬렉션에서 최대 작업 수를 30으로 변경 합니다.

## 변수

### -빈도
이 스케줄러 작업 컬렉션의 모든 작업에 지정할 수 있는 최대 빈도를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 길이의
- 시간씩
- 부활절
- 이번
- 달은
- 반기

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
업데이트할 스케줄러 작업 컬렉션의 이름을 지정 합니다.

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

### -PassThru
이 cmdlet이 작동 하는 항목을 나타내는 개체를 반환 함을 나타냅니다.
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

[새로운 AzureSchedulerJobCollection](./New-AzureSchedulerJobCollection.md)

[제거-AzureSchedulerJobCollection](./Remove-AzureSchedulerJobCollection.md)



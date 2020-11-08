---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2BF5BDF8-3743-46FC-8E04-1A4EA920A2AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77b4d184ffbdb1d054f3d14aa3c51c8d2afc928b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046310"
---
# Get-AzureSchedulerJobHistory

## SYNOPSIS
스케줄러 작업에 대 한 기록을 가져옵니다.

## 구문과

```
Get-AzureSchedulerJobHistory -Location <String> -JobCollectionName <String> -JobName <String>
 [-JobStatus <String>] [-Profile <AzureSMProfile>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## 설명은
이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

**AzureSchedulerJobHistory** cmdlet은 스케줄러 작업에 대 한 기록을 가져옵니다.

## 예제의

### 예제 1: 이름을 사용 하 여 작업에 대 한 기록 가져오기
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

이 명령은 Job01 이라는 작업 기록을 가져옵니다.
해당 작업은 지정 된 위치에서 JobCollection01 이라는 작업 컬렉션에 속합니다.

### 예제 2: 이름을 사용 하 여 실패 한 작업에 대 한 기록 가져오기
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job12" -JobStatus "Failed"
```

이 명령은 상태가 실패 한 Job12 이라는 작업 기록을 가져옵니다.
해당 작업은 지정 된 위치에서 JobCollection01 이라는 작업 컬렉션에 속합니다.

## 변수

### -첫 번째
지정 된 수의 개체만 가져옵니다.
가져올 개체 수를 입력 합니다.

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeTotalCount
데이터 집합 (정수)에 있는 개체의 총 수와 선택한 개체를 보고 합니다.
Cmdlet에서 총 개수를 확인할 수 없는 경우 "알 수 없는 총 개수"가 표시 됩니다. Integer에는 총 count 값의 안정성을 나타내는 정확도 속성이 있습니다.
정확도 값의 범위는 0.0에서 0.0 1.0는 cmdlet이 개체 수를 계산할 수 없음을 의미 하 고, 1.0에서는 카운트가 정확한 지를 의미 하며, 0.0 및 1.0 간의 값이 점차 안정적인 추정치를 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobCollectionName
스케줄러 작업 컬렉션의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 컬렉션에 속한 작업의 기록을 가져옵니다.

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

### -JobName
기록을 가져올 스케줄러 작업의 이름을 지정 합니다.

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

### -JobStatus
기록을 가져올 스케줄러 작업의 상태를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 완료
- 못함

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

### -생략
지정 된 수의 개체를 무시 한 다음 나머지 개체를 가져옵니다.
건너뛸 개체 수를 입력 합니다.

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureSchedulerJob](./Get-AzureSchedulerJob.md)

[Get-AzureSchedulerJobCollection](./Get-AzureSchedulerJobCollection.md)



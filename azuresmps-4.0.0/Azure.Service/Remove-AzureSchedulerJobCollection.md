---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D4349562-1392-44B6-9353-6231F0CB5C51
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66618c0a684a8e54d41bbe4014ee1e6c893acdbf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046128"
---
# Remove-AzureSchedulerJobCollection

## SYNOPSIS
스케줄러 작업 컬렉션을 삭제 합니다.

## 구문과

```
Remove-AzureSchedulerJobCollection [-Force] [-Location <String>] -JobCollectionName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

**AzureSchedulerJobCollection** cmdlet은 스케줄러 작업 컬렉션 및 해당 컬렉션 아래의 모든 작업을 삭제 합니다.

## 예제의

### 예제 1: 위치에 대 한 작업 컬렉션 삭제
```
PS C:\> Remove-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

이 명령은 미국 중부 US 위치에서 JobCollection01 이라는 스케줄러 작업 컬렉션을 삭제 합니다.
또한이 명령은 JobCollection01에서 작업을 삭제 합니다.

### 예제 2: 작업 위치 삭제
```
PS C:\> Remove-AzureSchedulerJobCollection -JobCollectionName "JobCollection02"
```

이 명령은 JobCollection02 이라는 스케줄러 작업 컬렉션을 삭제 합니다.
또한이 명령은 JobCollection02에서 작업을 삭제 합니다.

## 변수

### -Force
이 cmdlet이 스케줄러 작업 컬렉션을 확인 메시지 없이 제거 함을 나타냅니다.

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

### -JobCollectionName
삭제할 스케줄러 작업 컬렉션의 이름을 지정 합니다.

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

[Set-AzureSchedulerJobCollection](./Set-AzureSchedulerJobCollection.md)



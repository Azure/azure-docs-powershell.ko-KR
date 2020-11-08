---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1815E7F-720E-4526-A779-106C181B840D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22b04496d9ce310b58662c62b70a195e8cfa8878
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046031"
---
# Start-AzureEmulator

## SYNOPSIS
계산 및 저장소 에뮬레이터를 시작 합니다.

## 구문과

```
Start-AzureEmulator [-Launch] [-Mode <ComputeEmulatorMode>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

**시작 AzureEmulator** cmdlet은 계산 및 저장소 에뮬레이터를 모두 시작 하 고 계산 에뮬레이터에서 현재 서비스를 호스팅합니다.

## 예제의

### 예제 1: 에뮬레이터 시작 및 브라우저 시작
```
PS C:\> Start-AzureEmulator -L
```

이 예제에서는 Azure 에뮬레이터에서 서비스를 실행 하 고 에뮬레이트된 서비스에서 새 브라우저 창을 실행 합니다.

## 변수

### -시작
에뮬레이터에서 서비스를 호스팅한 후 새 브라우저 창을 엽니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -모드
에뮬레이터 모드를 지정 합니다.
유효한 값은 Full 및 Express입니다.
기본 값은 Express입니다.

```yaml
Type: ComputeEmulatorMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

[새-AzureServiceProject](./New-AzureServiceProject.md)

[게시-AzureServiceProject](./Publish-AzureServiceProject.md)

[정지-AzureEmulator](./Stop-AzureEmulator.md)



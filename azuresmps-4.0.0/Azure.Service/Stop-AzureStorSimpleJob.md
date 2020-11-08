---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046012"
---
# Stop-AzureStorSimpleJob

## SYNOPSIS
StorSimple 작업을 중지 합니다.

## 구문과

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureStorSimpleJob** cmdlet은 지속적인 StorSimple 작업을 중지 합니다.
인스턴스 ID 또는 작업 이름을 제공 하 여 작업을 지정할 수 있습니다.

## 예제의

### 예제 1: 장치에 대 한 작업 중지
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

이 명령은 Device07 이라는 장치에 대 한 작업을 **Get-AzureStorSimpleJob** cmdlet을 사용 하 여 가져옵니다.
이 명령은 파이프라인 연산자를 사용 하 여 현재 cmdlet에 작업을 전달 합니다.
현재 cmdlet은 명령이 전달 하는 모든 작업을 중지 합니다.
명령에서 *Force* 매개 변수를 지정 하므로 작업을 중지 하기 전에 확인 메시지가 표시 되지 않습니다.

### 예제 2: 특정 작업 중지
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

이 명령은 지정 된 인스턴스 ID가 있는 작업을 중지 합니다.

## 변수

### -Force
사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.

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

### -InstanceId
중지할 장치 작업의 ID를 지정 합니다.

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
Azure 프로필을 지정 합니다.

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

### 않아야

## 출력

### DeviceJobDetails
이 cmdlet은이 cmdlet이 중지 하는 **Devicejob** 에 대 한 세부 정보를 가져옵니다.

## 상속자

## 관련 링크

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)



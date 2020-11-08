---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EE7EC812-640B-4672-B23C-673F912F0EDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 945d06ddc1be6d2b0864b0421a5a087e14d98218
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045528"
---
# New-AzureStorSimpleDeviceBackupScheduleAddConfig

## SYNOPSIS
백업 일정 구성 개체를 만듭니다.

## 구문과

```
New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] -Enabled <Boolean>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureStorSimpleDeviceBackupScheduleAddConfig** Cmdlet은 **BackupScheduleBase** 구성 개체를 만듭니다.
이 구성 개체를 사용 하 여 **새 AzureStorSimpleDeviceBackupPolicy** cmdlet을 사용 하 여 새 백업 정책을 만듭니다.

## 예제의

### 예제 1: 백업 구성 개체 만들기
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 1 -RetentionCount 100 -Enabled $True
VERBOSE: ClientRequestId: 426a79ee-fed3-4d3d-9123-e371f83222b3_PS


BackupType     : CloudSnapshot
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 100
StartTime      : 2014-12-16T00:37:19+05:30
Status         : Enabled
```

이 명령은 클라우드 스냅숏 백업에 대 한 백업 일정 기본 개체를 만듭니다.
백업은 매일 수행 되며 백업은 100 일간 유지 됩니다.
이 일정은 기본 시간 (현재 시간)에서 사용 하도록 설정 됩니다.

## 변수

### -BackupType
백업 유형을 지정 합니다.
유효한 값은 LocalSnapshot 및 CloudSnapshot입니다.

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

### -사용
백업 일정을 사용할 수 있는지 여부를 나타냅니다.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -RecurrenceType
이 백업 일정의 되풀이 유형을 지정 합니다.
유효한 값은 다음과 같습니다. 

- 걸릴
- 마다
- Daily
- 매주

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

### -RecurrenceValue
백업을 만들 빈도를 지정 합니다.
이 매개 변수는 *RecurrenceType* 매개 변수로 지정 된 단위를 사용 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -보존 횟수
백업을 유지할 일 수를 지정 합니다.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartFromDateTime
백업 하기 시작 하는 날짜를 지정 합니다.
기본값은 현재 시간입니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### BackupScheduleBase
이 cmdlet은 **BackupScheduleBase** 개체를 반환 합니다.
**BackupScheduleBase** 를 사용 하 여 새 백업 정책을 만듭니다.

## 상속자

## 관련 링크

[새로운 AzureStorSimpleDeviceBackupScheduleUpdateConfig](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)

[새로운 AzureStorSimpleDeviceBackupPolicy](./New-AzureStorSimpleDeviceBackupPolicy.md)



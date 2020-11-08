---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 22C6845E-D7BD-4BBC-B373-394A23488A94
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0695dc42d9c540e30ddf9ac55bd6fc136c84bff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045524"
---
# New-AzureStorSimpleDeviceBackupScheduleUpdateConfig

## SYNOPSIS
백업 일정 업데이트 구성 개체를 만듭니다.

## 구문과

```
New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id <String> -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] [-Enabled <Boolean>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureStorSimpleDeviceBackupScheduleUpdateConfig** Cmdlet은 **BackupScheduleUpdateRequest** 구성 개체를 만듭니다.
이 구성 개체를 사용 하 여 **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet을 사용 하 여 백업 정책을 업데이트 합니다.

## 예제의

### 예제 1: 일정 업데이트 요청 만들기
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "147f734d-a31a-4473-8501-6ba38be2cb30" -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 50 -Enabled $True
VERBOSE: ClientRequestId: ef346641-54b4-4273-8898-7f863e7c5b7e_PS


BackupType     : CloudSnapshot
Id             : 147f734d-a31a-4473-8501-6ba38be2cb30
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 50
StartTime      : 2014-12-16T00:39:32+05:30
Status         : Enabled
```

이 명령은 지정 된 ID를 갖는 일정에 대 한 백업 일정 업데이트 요청을 만듭니다.
이 요청은 1 시간 마다 되풀이 되는 클라우드 스냅샷 백업을 예약 하는 것입니다.
백업은 50 일간 유지 됩니다.
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

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
업데이트할 백업 일정의 인스턴스 ID를 지정 합니다.

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

### BackupScheduleUpdateRequest
이 cmdlet은 업데이트 된 백업 일정에 대 한 정보를 포함 하는 **BackupScheduleUpdateRequest** 개체를 반환 합니다.

## 상속자

## 관련 링크

[새로운 AzureStorSimpleDeviceBackupScheduleAddConfig](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)

[Set-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)



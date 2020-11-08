---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 2001E040-5551-40C3-81D2-9A8334DE02BF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7692d4407df8fb4af8647ee0b4490abe73b2c937
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045558"
---
# Get-AzureStorSimpleJob

## SYNOPSIS
StorSimple 작업을 가져옵니다.

## 구문과

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**Get-AzureStorSimpleJob** Cmdlet은 Azure StorSimple 작업을 가져옵니다.
인스턴스 ID를 지정 하 여 특정 작업을 가져옵니다.
다른 매개 변수를 지정 하 여이 cmdlet이 가져오는 작업을 제한 합니다.

이 cmdlet은 최대 200 작업을 반환 합니다.
200 작업이 둘 이상 있는 경우 *첫 번째* 및 *건너뛰기* 매개 변수를 사용 하 여 나머지 작업을 가져옵니다.
*Skip* 및 50에 대 한 100 값을 *먼저* 지정 하면이 cmdlet은 첫 번째 100 결과를 반환 하지 않습니다.
이 메서드는 건너뛴 100 다음의 50 결과를 반환 합니다.

## 예제의

### 예제 1: ID를 사용 하 여 작업 가져오기
```
PS C:\>Get-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d"
BackupPolicy             : 
BackupTimeStamp          : 1/1/0001 12:00:00 AM
BackupType               : CloudSnapshot
DataStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.DataStatistics
Device                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Entity                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
ErrorDetails             : {}
HideProgressDetails      : False
InstanceId               : 574f47e0-44e9-495c-b8a5-0203c57ebf6d
IsInstantRestoreComplete : False
IsJobCancellable         : True
JobDetails               : Microsoft.WindowsAzure.Management.StorSimple.Models.JobStatusInfo
Name                     : 26447caf-59bb-41c9-a028-3224d296c7dc
Progress                 : 100
SourceDevice             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceEntity             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
SourceVolume             : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
Status                   : Completed
TimeStats                : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeStatistics
Type                     : Backup
Volume                   : Microsoft.WindowsAzure.Management.StorSimple.Models.CisBaseObject
```

이 명령은 지정 된 ID를 가진 작업에 대 한 정보를 가져옵니다.

### 예제 2: 장치 이름을 사용 하 여 작업 가져오기
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

이 명령은 8600-Bravo 001 이라는 장치 작업에 대 한 정보를 가져옵니다.
명령은 장치에 대 한 처음 두 작업을 가져옵니다.

### 예제 3: 완료 된 작업 가져오기
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

이 명령은 완료 된 작업을 가져옵니다.
명령은 처음 10 개 작업을 건너뛴 후 처음 두 개의 작업만 가져옵니다.

### 예제 4: 수동 백업 작업 가져오기
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

이 명령은 수동 백업 유형의 작업을 가져옵니다.

### 예제 5: 지정 된 시간 사이에 작업 가져오기
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

처음 두 명령은 Get-Date cmdlet을 사용 하 여 **DateTime** 개체를 만듭니다.
명령은 $StartTime 및 $EndTime 변수에 새 시간을 저장 합니다.
자세한 내용은을 입력 `Get-Help Get-Date` 하세요.

마지막 명령은 $StartTime 및 $EndTime에 저장 된 시간 사이에 Device07 이라는 장치에 대 한 작업을 가져옵니다.

## 변수

### -장치 이름
StorSimple 장치의 이름을 지정 합니다.

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

### -첫 번째
지정 된 수의 개체만 가져옵니다.
가져올 개체 수를 입력 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -보낸 사람
이 cmdlet이 가져오는 작업의 시작 날짜와 시간을 지정 합니다.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
가져올 작업의 ID를 지정 합니다.

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
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -상태
상태를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 실행
- 완료
- 되었습니다
- 못함
- ...
- CompletedWithErrors

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

### -To
이 cmdlet이 가져오는 작업의 종료 날짜와 시간을 지정 합니다.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
작업 유형을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 백업할
- ManualBackup
- 복원한
- CloneWorkflow
- DeviceRestore
- Update
- SupportPackage
- VirtualApplianceProvisioning

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
이 cmdlet에는 입력을 파이프가 지정할 수 없습니다.

## 출력

### IList \<DeviceJobDetails\> , devicejobdetails
이 cmdlet은 작업 세부 정보 개체의 목록을 반환 하거나, *InstanceID* 매개 변수를 지정 하는 경우 단일 작업 정보 개체를 반환 합니다.

## 상속자

## 관련 링크

[중지-AzureStorSimpleJob](./Stop-AzureStorSimpleJob.md)



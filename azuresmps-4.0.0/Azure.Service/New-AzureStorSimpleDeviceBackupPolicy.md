---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EFAE7117-9B8B-4CB9-B4D9-3F08DCE1816E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 405b9d427c7e59dfb3628806a878d57a281a6b4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046208"
---
# New-AzureStorSimpleDeviceBackupPolicy

## SYNOPSIS
백업 정책을 만듭니다.

## 구문과

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**새 AzureStorSimpleDeviceBackupPolicy** cmdlet은 백업 정책을 만듭니다.
백업 정책에는 하나 이상의 볼륨에서 실행할 수 있는 하나 이상의 백업 일정이 포함 되어 있습니다.
백업 일정을 만들려면 **새 AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet을 사용 합니다.

## 예제의

### 예제 1: 백업 정책 만들기
```
PS C:\>$Schedule01 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType LocalSnapshot -RecurrenceType Daily -RecurrenceValue 10 -RetentionCount 5 -Enabled $True
PS C:\> $Schedule02 = New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 5 -Enabled $True
PS C:\> $ScheduleArray = @()
PS C:\> $ScheduleArray += $Schedule01
PS C:\> $ScheduleArray += $Schedule02
PS C:\> $DeviceContainer = Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm"
PS C:\> $Volume = $(Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeContainer $DeviceContainer[0])
PS C:\> $VolumeArray = @()
PS C:\> $VolumeArray += $Volume[0].InstanceId
PS C:\> New-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralPolicy07" -BackupSchedulesToAdd $ScheduleArray -VolumeIdsToAdd $VolumeArray
VERBOSE: ClientRequestId: e9d6771e-c323-47b9-b424-cb98f8ed0273_PS
VERBOSE: ClientRequestId: db0e7c86-d0d2-4a5a-b1cb-182494cba027_PS
VERBOSE: ClientRequestId: 77708dfd-a386-4999-b7ed-5d53e288ae83_PS


JobId        : d4ce5340-d5d1-4471-9cc8-013193f021b3
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your add operation has completed successfully. 
VERBOSE: ClientRequestId: bbf7e9b9-b493-40b3-8348-f15bcfc4da8a_PS
BackupSchedules          : {36d21096-bbd1-47b7-91b5-40ad1792d992, 505fc91f-deb5-4dca-bfcb-98c20b75ebcc}
Volumes                  : {volume03}
BackupPolicyCreationType : BySaaS
LastBackup               : 01-01-2010 05:30:00
NextBackup               : 16-12-2014 01:13:43
SchedulesCount           : 2
SSMHostName              : 
VolumesCount             : 1
InstanceId               : 8799c2f0-8850-4e91-aa23-ee18c67da8bd
Name                     : GeneralPolicy07
OperationInProgress      : None
```

첫 번째 명령은 **새 AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet을 사용 하 여 백업 일정 구성 개체를 만든 다음 해당 개체를 $Schedule 01 변수에 저장 합니다.

두 번째 명령은 **New-AzureStorSimpleDeviceBackupScheduleAddConfig** 를 사용 하 여 다른 백업 구성 개체를 만든 다음 해당 개체를 $Schedule 02 변수에 저장 합니다.

세 번째 명령은 $ScheduleArray 라는 빈 배열 변수를 만듭니다.
다음 두 명령은 $ScheduleArray 하기 위해 처음 두 명령에서 만든 개체를 추가 합니다.

여섯 번째 명령은 **AzureStorSimpleDeviceVolumeContainer** cmdlet을 사용 하 여 Contoso63-AppVm 이라는 장치에 대 한 볼륨 컨테이너를 가져온 다음 해당 컨테이너 개체를 $DeviceContainer 변수에 저장 합니다.

일곱 번째 명령은 **AzureStorSimpleDeviceVolume** cmdlet을 사용 하 여 $DeviceContainer의 첫 번째 구성원에 저장 된 볼륨 컨테이너에 대 한 볼륨을 가져온 다음 해당 볼륨을 $Volume 변수에 저장 합니다.

여덟 번째 명령은 $VolumeArray 라는 빈 배열 변수를 만듭니다.
다음 명령은 $VolumeArray에 볼륨 ID를 추가 합니다.
이 값은 백업 정책이 실행 되는 $Volume에 저장 된 볼륨을 식별 합니다.
$VolumeArray에 다른 볼륨 Id를 추가할 수 있습니다.

마지막 명령은 Contoso63-AppVm 이라는 장치에 대 한 GeneralPolicy07 라는 백업 정책을 만듭니다.
명령은 $ScheduleArray에 저장 된 일정 구성 개체를 지정 합니다.
이 명령은 $VolumeArray 정책을 적용할 볼륨을 지정 합니다.
**AzureStorSimpleDeviceBackupPolicy** cmdlet을 사용 하 여 백업 정책을 확인할 수 있습니다.

## 변수

### -BackupPolicyName
백업 정책의 이름을 지정 합니다.

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

### -BackupSchedulesToAdd
정책에 추가할 **BackupScheduleBase** 개체의 배열을 지정 합니다.
각 개체는 일정을 나타냅니다.
백업 정책에는 하나 이상의 일정이 포함 되어 있습니다.
**BackupScheduleBase** 개체를 얻으려면 **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet을 사용 합니다.

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -장치 이름
백업 정책을 만들 StorSimple 장치의 이름을 지정 합니다.

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

### -VolumeIdsToAdd
백업 정책에 추가할 볼륨 Id의 배열을 지정 합니다.

```yaml
Type: PSObject[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForComplete
이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### BackupPolicy
이 cmdlet은 새 일정 및 볼륨을 포함 하는 **Backuppolicy** 개체를 반환 합니다.

## 상속자

## 관련 링크

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[Get-AzureStorSimpleDeviceVolume](./Get-AzureStorSimpleDeviceVolume.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[제거-AzureStorSimpleDeviceBackupPolicy](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[Set-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[새로운 AzureStorSimpleDeviceBackupScheduleAddConfig](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)



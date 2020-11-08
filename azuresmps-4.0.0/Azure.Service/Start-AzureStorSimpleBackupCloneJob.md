---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 403AD2BF-5D03-4B48-A635-E08216FFFC0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07df96f59b2278d804312d1076965ffed43c2569
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045748"
---
# Start-AzureStorSimpleBackupCloneJob

## SYNOPSIS
장치에서 백업을 복제 하는 작업을 시작 합니다.

## 구문과

### 비어 있음 (기본값)
```
Start-AzureStorSimpleBackupCloneJob -BackupId <String> -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceName <String> -TargetDeviceName <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Start-AzureStorSimpleBackupCloneJob -SourceDeviceId <String> -TargetDeviceId <String> -BackupId <String>
 -Snapshot <Snapshot> -CloneVolumeName <String>
 [-TargetAccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureStorSimpleBackupCloneJob** Cmdlet은 StorSimple 장치에서 기존 백업을 복제 하는 작업을 시작 합니다.

## 예제의

### 예제 1: 장치 이름을 사용 하 여 다른 볼륨으로 백업 복제
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07 -TargetDeviceName "ContosoDev07" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

첫 번째 명령은 **AzureStorSimpleDeviceBackup** cmdlet을 사용 하 여 ContosoDev07 이라는 장치에 대 한 첫 번째 백업을 가져옵니다.
이 명령은 $Backup 변수에 해당 백업을 저장 합니다.

두 번째 명령은 **Get-AzureStorSimpleAccessControlRecord** cmdlet을 사용 하 여 액세스 제어 레코드를 가져옵니다.
명령이 $Acrs 변수에 결과를 저장 합니다.

마지막 명령은 장치의 볼륨에 대 한 지정 된 백업을 같은 장치의 다른 볼륨에 복제 하는 작업을 시작 합니다.
이 예제에서는 이름을 기준으로 디바이스를 지정 합니다.
이 명령은 $Backup 및 $Acrs에 저장 된 값을 사용 합니다.
명령에서 작업의 ID를 반환 합니다.

### 예제 2: 장치 Id를 사용 하 여 다른 볼륨으로 백업 복제
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev07 -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -TargetDeviceId "be7a73a7-980c-4ba2-82d4-f6a7ee0eacbb" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

첫 번째 명령은 **AzureStorSimpleDeviceBackup** cmdlet을 사용 하 여 ContosoDev07 이라는 장치에 대 한 첫 번째 백업을 가져옵니다.
이 명령은 $Backup 변수에 해당 백업을 저장 합니다.

두 번째 명령은 **Get-AzureStorSimpleAccessControlRecord** cmdlet을 사용 하 여 액세스 제어 레코드를 가져옵니다.
명령이 $Acrs 변수에 결과를 저장 합니다.

마지막 명령은 장치의 볼륨에 대 한 지정 된 백업을 같은 장치의 다른 볼륨에 복제 하는 작업을 시작 합니다.
이 예제에서는 장치 ID를 기준으로 디바이스를 지정 합니다.
이 명령은 $Backup 및 $Acrs에 저장 된 값을 사용 합니다.
명령에서 작업의 ID를 반환 합니다.

### 예제 3: 장치 이름을 사용 하 여 다른 장치의 볼륨에 백업 복제
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "ContosoDev07" -First 1
PS C:\> $Acrs = Get-AzureStorSimpleAccessControlRecord -ACRName "Acr01"
PS C:\> Start-AzureStorSimpleBackupCloneJob -SourceDeviceName "ContosoDev07" -TargetDeviceName "ContosoDev12" -BackupId $Backup.InstanceId -Snapshot $Backup.Snapshots[0] -CloneVolumeName "cloned_volume11" -TargetAccessControlRecords $Acrs
VERBOSE: ClientRequestId: 43d8b4dc-39da-4ec5-92f6-be1f499155e9_PS
VERBOSE: ClientRequestId: be7a73a7-980c-4ba2-82d4-f6a7ee0eac0a_PS
VERBOSE: ClientRequestId: ee02aaae-d366-43d2-a229-8761d6db39f1_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 9b81d9f9-3e31-49be-a8cd-1b1c6afdb744_PS
bd05baee-36d0-48f4-8b1e-8119c4133446
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId bd05baee-36d0-48f4-8b1e-8119c4133446 for tracking the job's status
```

첫 번째 명령은 **AzureStorSimpleDeviceBackup** cmdlet을 사용 하 여 ContosoDev07 이라는 장치에 대 한 첫 번째 백업을 가져옵니다.
이 명령은 $Backup 변수에 해당 백업을 저장 합니다.

두 번째 명령은 **Get-AzureStorSimpleAccessControlRecord** cmdlet을 사용 하 여 액세스 제어 레코드를 가져옵니다.
명령이 $Acrs 변수에 결과를 저장 합니다.

마지막 명령은 장치의 볼륨에 대 한 지정 된 백업을 다른 장치의 볼륨에 복제 하는 작업을 시작 합니다.
이 예제에서는 이름을 기준으로 디바이스를 지정 합니다.
이 명령은 $Backup 및 $Acrs에 저장 된 값을 사용 합니다.
명령에서 작업의 ID를 반환 합니다.

### 예제 4: 장치 이름과 파이프라인 연산자를 사용 하 여 다른 볼륨으로 백업 복제
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName ContosoDev1 -First 1
PS C:\> Get-AzureStorSimpleAccessControlRecord -ACRName acr1 | Start-AzureStorSimpleBackupCloneJob -SourceDeviceName ContosoDev1 -TargetDeviceName ContosoDev1 -BackupId $backup.InstanceId -Snapshot $backup.Snapshots[0] -CloneVolumeName "cloned_vol1" 
VERBOSE: ClientRequestId: 1183a29d-63a9-408a-9065-032c92d317ee_PS
VERBOSE: ClientRequestId: e195717c-5920-4133-bdf0-c1201ebabf6f_PS
VERBOSE: ClientRequestId: ac16644d-bfd8-4edf-b1ad-f5df4ceb4df7_PS
VERBOSE: ClientRequestId: dcdcab7f-2aaa-496d-8a18-2e7449a70227_PS
VERBOSE: ClientRequestId: 6f92e422-eda9-4087-aefb-2257a49f5beb_PS

Confirm
Are you sure you want to clone the backup with backupId fca748a0-4154-49e0-9550-07fa481cbd2d? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
VERBOSE: ClientRequestId: 646b280c-b51c-4812-b5c5-b7ca215f1c90_PS
a747d2dc-2876-474e-aea6-6546b255427e
VERBOSE: The start job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId a747d2dc-2876-474e-aea6-6546b255427e for tracking the job's status
VERBOSE: Access Control Record with given name acr11 is found!
```

첫 번째 명령은 **AzureStorSimpleDeviceBackup** cmdlet을 사용 하 여 ContosoDev07 이라는 장치에 대 한 첫 번째 백업을 가져옵니다.
이 명령은 $Backup 변수에 해당 백업을 저장 합니다.

두 번째 명령은 **Get-AzureStorSimpleAccessControlRecord** cmdlet을 사용 하 여 액세스 제어 레코드를 가져옵니다.
이 명령은 파이프라인 연산자를 사용 하 여 결과를 현재 cmdlet에 전달 합니다.
현재 cmdlet은 장치의 볼륨에 대해 지정 된 백업을 같은 장치의 다른 볼륨에 복제 하는 작업을 시작 합니다.
이 예제에서는 이름을 기준으로 디바이스를 지정 합니다.
이 명령은 $Backup에 저장 된 값을 사용 합니다.
명령은 파이프라인에서 *Targetaccesscontrolrecords* 매개 변수 값을 가져옵니다.
명령에서 작업의 ID를 반환 합니다.

## 변수

### -BackupId
복제할 백업의 인스턴스 ID를 지정 합니다.

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

### -CloneVolumeName
대상 장치에서 복제 된 새 볼륨의 이름을 지정 합니다.

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

### -스냅숏
이 cmdlet이 복제 하는 스냅숏 개체를 지정 합니다.

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDeviceId
원본 장치의 인스턴스 ID를 지정 합니다.
이 cmdlet은 원본 장치에서 다시 복제 합니다.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDeviceName 이름
원본 장치의 이름을 지정 합니다.
이 cmdlet은 원본 장치에서 다시 복제 합니다.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetAccessControlRecords
액세스 제어 레코드를 지정 합니다.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TargetDeviceId
대상 장치의 인스턴스 ID를 지정 합니다.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDeviceName 이름
이 cmdlet이 백업을 복제 하는 디바이스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 스냅샷, AccessControlRecord 목록
이 cmdlet에 대 한 **Accesscontrolrecord** 개체의 목록을 파이프 **스냅샷** 개체 또는 목록으로 만들 수 있습니다.

## 출력

## 상속자

## 관련 링크

[Get-AzureStorSimpleDeviceBackup](./Get-AzureStorSimpleDeviceBackup.md)

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)



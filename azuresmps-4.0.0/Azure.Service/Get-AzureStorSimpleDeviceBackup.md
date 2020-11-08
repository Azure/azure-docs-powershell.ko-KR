---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A40879D2-371B-4CF1-BF1F-9E5C896EB89C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5ffe0a6e5a2d6ae181f4396eae2b5732f527843
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046290"
---
# Get-AzureStorSimpleDeviceBackup

## SYNOPSIS
장치에서 백업을 가져옵니다.

## 구문과

### 비어 있음 (기본값)
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> [-From <String>] [-To <String>] [-First <Int32>]
 [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicyId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById2
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -VolumeId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-From <String>]
 [-To <String>] [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject2
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -Volume <VirtualDisk> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureStorSimpleDeviceBackup** cmdlet은 장치에서 백업을 가져옵니다.
백업 정책, 볼륨 및 생성 시간을 백업에 대해 지정할 수 있습니다.

이 cmdlet은 첫 페이지에서 최대 100 개의 백업을 반환할 수 있습니다.
100 개 이상의 백업이 있는 경우 *첫 번째* 및 *건너뛰기* 매개 변수를 사용 하 여 다음 페이지를 검색 합니다.
*Skip* 및 50에 대 한 100 값을 *먼저* 지정 하면이 cmdlet은 첫 번째 100 결과를 반환 하지 않습니다.
이 메서드는 건너뛴 100 다음의 50 결과를 반환 합니다.

## 예제의

### 예제 1: 장치에서 모든 백업 가져오기
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
InstanceId                           Name                               Type          BackupJobCreationType              CreatedOn                          SizeInBytes                       Snapshots                         SSMHostName                      
----------                           ----                               ----          ---------------------              ---------                          -----------                       ---------                         -----------                      
85074062-ef6a-408a-b6c9-2a0904bb99ca Snapshot_vg-all                    LocalSnapshot BySchedule                         4/15/2015 1:30:02 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
ebd87fa3-a9e2-49c9-a7e6-dada47071544 Cloud_Snapshot_vg-all              CloudSnapshot BySchedule                         4/15/2015 11:30:02 AM              9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
9f7a03be-8c39-474c-bf88-b2c7b54e833c Cloud_Snapshot_Vol3_clone VG       CloudSnapshot BySchedule                         4/15/2015 9:00:03 AM               1717986918400                     {Volume 3 Clone}                                                   
177b2dad-c0b2-42d6-b7bb-16926e54e9c6 VG Clones                          CloudSnapshot BySchedule                         4/15/2015 8:30:02 AM               5016521801728                     {Volume 1 Clone, Volume 3 Clone}                                   
49c470c0-eadb-40ac-9928-94018a8edcd4 Cloud_Snapshot_Vol1_clone VG       CloudSnapshot BySchedule                         4/15/2015 7:30:02 AM               3298534883328                     {Volume 1 Clone}                                                   
45dfd283-f924-4b45-93eb-b20650cadf43 vg-all                             LocalSnapshot Adhoc                              3/27/2015 9:12:15 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
2c3dd48d-824c-4298-82b5-fb44abb67a1e Test Group                         LocalSnapshot Adhoc                              3/27/2015 1:47:00 AM               5016521801728                     {Volume 1, Volume 3}
```

이 명령은 Contoso63 라는 장치에 존재 하는 모든 백업을 가져옵니다.
첫 페이지에 대해 최대 100 개의 백업이 허용 되는 경우 *첫 번째* *매개 변수를 사용* 하 여 추가 결과를 확인 합니다.

### 예제 2: 두 날짜 사이에 만든 백업 가져오기
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -From "9/7/2014" -To "10/7/2014" -First 2 -Skip 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/5/2014 11:00:04 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : ec2fdf5c-c807-4f7b-a942-d4c4a9b68c44
Name                  : ContosoTSQA_Default
BackupJobCreationType : BySchedule
CreatedOn             : 10/4/2014 11:00:06 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 5ac4f947-f4c6-4770-9000-2242e72fc6d3
Name                  : ContosoTSQA_DefaultVERBOSE: # of backups returned : 2
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 2 -Skip 3\" in
your commandlet
```

이 명령은 10/7/2014 및 10/8/2014 또는 이전에 만든 Contoso63-AppVm 라는 장치에서 백업을 가져옵니다.
이 cmdlet은 첫 번째 결과를 건너뛰고 첫 번째 결과 두 개의 결과를 반환 합니다.
*먼저* 값을 수정 하 고 *건너 뛰고* 다른 결과를 봅니다.

### 예제 3: 백업 정책 ID에 대 한 백업 가져오기
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

이 명령은 지정 된 날짜 또는 그 이전에 만들어진 Contoso63-AppVm 장치에서 백업을 가져옵니다.
명령은 지정 된 ID를 가진 백업 정책을 사용 하 여 만든 백업을 가져옵니다.
이 *명령은 첫 번째 매개 변수* 를 지정 하므로 처음 10 개의 결과만 반환 합니다.

### 예제 4: 백업 정책 개체에 대 한 백업 가져오기
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQATest_Default" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

이 명령은 **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet을 사용 하 여 **backuppolicydetails** 개체를 가져온 다음 파이프라인 연산자를 사용 하 여 현재 cmdlet에 해당 개체를 전달 합니다.
해당 cmdlet은 명령의 첫 번째 부분에서 백업 정책을 사용 하 여 생성 된 Contoso63-AppVm 장치에 대 한 백업을 가져옵니다.
이 명령은 이전 예제와 마찬가지로 지정 된 날짜 또는 그 이전에 만들어진 백업을 가져옵니다.
이 명령은 처음 10 개의 결과만 반환 합니다.

### 예제 5: 볼륨 ID에 대 한 백업 가져오기
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -VolumeId "SS-VOL-246b9df1-11bb-4071-8043-f955cc406446" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

이 명령은 지정 된 인스턴스 ID를 가진 볼륨에서 만들어진 장치에 대 한 백업을 가져옵니다.
이 *명령은 첫 번째 매개 변수* 를 지정 하므로 처음 하나의 결과만 반환 합니다.

### 예제 6: 볼륨 이름에 대 한 백업 가져오기
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "TSQATest03" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

이 명령은 **AzureStorSimpleDeviceVolume** cmdlet을 사용 하 여 **VirtualDisk** 개체를 가져온 다음 파이프라인 연산자를 사용 하 여 현재 cmdlet에 해당 개체를 전달 합니다.
해당 cmdlet은 명령의 첫 번째 부분에서 볼륨에 생성 된 Contoso63-AppVm 장치에 대 한 백업을 가져옵니다.
이 명령은 첫 번째 결과만 반환 합니다.

## 변수

### -BackupPolicy
**Backuppolicydetails** 개체를 지정 합니다.
이 cmdlet은이 개체의 **InstanceId** 를 사용 하 여 가져올 백업을 결정 합니다.
**Backuppolicydetails** 개체를 가져오려면 **AzureStorSimpleDeviceBackupPolicy** cmdlet을 사용 합니다.

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: BackupPolicyDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackupPolicyId
백업 정책의 인스턴스 ID를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 정책에 대 한 장치 백업을 가져옵니다.

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

### -장치 이름
백업을 가져올 StorSimple 장치의 이름을 지정 합니다.

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
이 cmdlet이 가져오는 백업의 시작 날짜와 시간을 지정 합니다.

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

### -To
이 cmdlet이 가져오는 백업의 종료 날짜와 시간을 지정 합니다.

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

### -볼륨
**VirtualDisk** 개체를 지정 합니다.
이 cmdlet은이 개체의 **InstanceId** 를 사용 하 여 백업이 있는 볼륨을 확인 합니다.
**VirtualDisk** 개체를 가져오려면 **Get-AzureStorSimpleDeviceVolume** 매개 변수를 사용 합니다.

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject2
Aliases: VirtualDiskInfo

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VolumeId
백업이 있는 볼륨의 인스턴스 ID를 지정 합니다.

```yaml
Type: String
Parameter Sets: IdentifyById2
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

### BackupPolicyDetails, VirtualDisk
이 cmdlet은 **Backuppolicydetails** 및 **VirtualDisk** 개체를 허용 합니다.

## 출력

### IList\<Backup\>
이 cmdlet은 **백업** 개체의 목록을 반환 합니다.

## 상속자

## 관련 링크

[제거-AzureStorSimpleDeviceBackup](./Remove-AzureStorSimpleDeviceBackup.md)

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[Get-AzureStorSimpleDeviceVolume](./Get-AzureStorSimpleDeviceVolume.md)



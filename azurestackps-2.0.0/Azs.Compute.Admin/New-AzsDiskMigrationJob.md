---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: c3fd190fb033a685bcb0d5087c544298681e47c5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877194"
---
# New-AzsDiskMigrationJob

## SYNOPSIS


## 구문과

### 볼륨 (기본값)
```
New-AzsDiskMigrationJob -Name <String> -TargetScaleUnit <String> -TargetVolumeLabel <String> -Disks <IDisk[]>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### 공유
```
New-AzsDiskMigrationJob -Name <String> -TargetShare <String> -Disks <IDisk[]> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 설명은


## 예제의

### 예제 1:
```powershell
PS C:\> $disks = Get-AzsDisk
PS C:\> New-AzsDiskMigrationJob -Name TestJob1 -TargetScaleUnit s-cluster -TargetVolumeLabel ObjStore_2 -Disks $disks

CreationTime : 2/26/2020 10:56:32 AM
EndTime      : 
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestJob1
Location     : redmond
MigrationId  : TestJob1
Name         : redmond/TestJob1
StartTime    : 
Status       : Pending
Subtask      : {53ee3665-00e4-4c69-a067-524058905ead, d551734f-0370-4851-9704-c7cec80b34c5}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_2
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

디스크 마이그레이션 작업을 만들어 디스크를 대상 크기 조정 단위 및 볼륨으로 마이그레이션합니다.

### 예제 2: 
```powershell
PS C:\> PS C:\> $disks = Get-AzsDisk
PS C:\> New-AzsDiskMigrationJob -Name TestJob2 -TargetShare \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_3 -Disks $disks
WARNING: TargetShare parameter will be deprecated in a future release, please use Volume instead.

CreationTime : 2/26/2020 11:02:48 AM
EndTime      : 
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob2
Location     : redmond
MigrationId  : TestJob2
Name         : redmond/TestJob2
StartTime    : 
Status       : Pending
Subtask      : {0cfd8d29-1ca4-42db-a490-9198814abc50, 89c9b15e-47c6-4321-a390-611fc190cfad}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_3
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs-AzsDiskMigrationJob -Name TestJob1 -TargetScaleUnit s-cluster -TargetVolumeLabel ObjStore_2 -Disks $disks

```

디스크 마이그레이션 작업을 만들어 디스크를 대상 공유로 마이그레이션합니다.

## 변수

### -DefaultProfile


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -디스크
생성 하려면 디스크 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -위치


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -이름


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### -TargetScaleUnit


```yaml
Type: System.String
Parameter Sets: Volume
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -TargetShare


```yaml
Type: System.String
Parameter Sets: Share
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -TargetVolumeLabel


```yaml
Type: System.String
Parameter Sets: Volume
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### Api20180730Preview. t a t t a t a t a t a t 디스크 []

## 출력

### Api20180730Preview. IDiskMigrationJob에 대 한. t t t



### Start-AzsDiskMigrationJob

## 상속자

복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다. 해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.

디스크 <IDisk [] >: 
  - `[Location <String>]`: 리소스의 위치입니다.
  - `[DiskId <String>]`: 디스크 id입니다.
  - `[SharePath <String>]`: 디스크 공유 경로입니다.
  - `[Status <DiskState?>]`: 디스크 상태입니다.

## 관련 링크


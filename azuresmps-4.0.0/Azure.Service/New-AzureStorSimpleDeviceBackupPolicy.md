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
# <span data-ttu-id="5d4b0-101">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="5d4b0-101">New-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="5d4b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d4b0-102">SYNOPSIS</span></span>
<span data-ttu-id="5d4b0-103">백업 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-103">Creates a backup policy.</span></span>

## <span data-ttu-id="5d4b0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5d4b0-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyName <String>
 -BackupSchedulesToAdd <PSObject[]> -VolumeIdsToAdd <PSObject[]> [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d4b0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5d4b0-105">DESCRIPTION</span></span>
<span data-ttu-id="5d4b0-106">**새 AzureStorSimpleDeviceBackupPolicy** cmdlet은 백업 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-106">The **New-AzureStorSimpleDeviceBackupPolicy** cmdlet creates a backup policy.</span></span>
<span data-ttu-id="5d4b0-107">백업 정책에는 하나 이상의 볼륨에서 실행할 수 있는 하나 이상의 백업 일정이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-107">A backup policy contains one or more backup schedules that can run on one or more volumes.</span></span>
<span data-ttu-id="5d4b0-108">백업 일정을 만들려면 **새 AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-108">To create a backup schedule, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

## <span data-ttu-id="5d4b0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5d4b0-109">EXAMPLES</span></span>

### <span data-ttu-id="5d4b0-110">예제 1: 백업 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="5d4b0-110">Example 1: Create a backup policy</span></span>
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

<span data-ttu-id="5d4b0-111">첫 번째 명령은 **새 AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet을 사용 하 여 백업 일정 구성 개체를 만든 다음 해당 개체를 $Schedule 01 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-111">The first command creates a backup schedule configuration object by using the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet, and then stores that object in the $Schedule01 variable.</span></span>

<span data-ttu-id="5d4b0-112">두 번째 명령은 **New-AzureStorSimpleDeviceBackupScheduleAddConfig** 를 사용 하 여 다른 백업 구성 개체를 만든 다음 해당 개체를 $Schedule 02 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-112">The second command creates another backup configuration object by using **New-AzureStorSimpleDeviceBackupScheduleAddConfig** , and then stores that object in the $Schedule02 variable.</span></span>

<span data-ttu-id="5d4b0-113">세 번째 명령은 $ScheduleArray 라는 빈 배열 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-113">The third command creates an empty array variable, named $ScheduleArray.</span></span>
<span data-ttu-id="5d4b0-114">다음 두 명령은 $ScheduleArray 하기 위해 처음 두 명령에서 만든 개체를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-114">The next two commands add the objects created in the first two commands to $ScheduleArray.</span></span>

<span data-ttu-id="5d4b0-115">여섯 번째 명령은 **AzureStorSimpleDeviceVolumeContainer** cmdlet을 사용 하 여 Contoso63-AppVm 이라는 장치에 대 한 볼륨 컨테이너를 가져온 다음 해당 컨테이너 개체를 $DeviceContainer 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-115">The sixth command gets a volume container for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet, and then stores that container object in the $DeviceContainer variable.</span></span>

<span data-ttu-id="5d4b0-116">일곱 번째 명령은 **AzureStorSimpleDeviceVolume** cmdlet을 사용 하 여 $DeviceContainer의 첫 번째 구성원에 저장 된 볼륨 컨테이너에 대 한 볼륨을 가져온 다음 해당 볼륨을 $Volume 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-116">The seventh command gets a volume for the volume container stored in the first member of $DeviceContainer by using the **Get-AzureStorSimpleDeviceVolume** cmdlet, and then stores that volume in the $Volume variable.</span></span>

<span data-ttu-id="5d4b0-117">여덟 번째 명령은 $VolumeArray 라는 빈 배열 변수를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-117">The eighth command creates an empty array variable, named $VolumeArray.</span></span>
<span data-ttu-id="5d4b0-118">다음 명령은 $VolumeArray에 볼륨 ID를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-118">The next command adds a volume ID to $VolumeArray.</span></span>
<span data-ttu-id="5d4b0-119">이 값은 백업 정책이 실행 되는 $Volume에 저장 된 볼륨을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-119">This value identifies the volume, stored in $Volume, on which the backup policy runs.</span></span>
<span data-ttu-id="5d4b0-120">$VolumeArray에 다른 볼륨 Id를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-120">You can add additional volume IDs to $VolumeArray.</span></span>

<span data-ttu-id="5d4b0-121">마지막 명령은 Contoso63-AppVm 이라는 장치에 대 한 GeneralPolicy07 라는 백업 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-121">The final command creates the backup policy named GeneralPolicy07 for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="5d4b0-122">명령은 $ScheduleArray에 저장 된 일정 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-122">The command specifies the schedule configuration objects stored in $ScheduleArray.</span></span>
<span data-ttu-id="5d4b0-123">이 명령은 $VolumeArray 정책을 적용할 볼륨을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-123">The command specifies the volume or volumes to which to apply the policy in $VolumeArray.</span></span>
<span data-ttu-id="5d4b0-124">**AzureStorSimpleDeviceBackupPolicy** cmdlet을 사용 하 여 백업 정책을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-124">You can verify the backup policy by using the **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="5d4b0-125">변수</span><span class="sxs-lookup"><span data-stu-id="5d4b0-125">PARAMETERS</span></span>

### <span data-ttu-id="5d4b0-126">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="5d4b0-126">-BackupPolicyName</span></span>
<span data-ttu-id="5d4b0-127">백업 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-127">Specifies the name of the backup policy.</span></span>

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

### <span data-ttu-id="5d4b0-128">-BackupSchedulesToAdd</span><span class="sxs-lookup"><span data-stu-id="5d4b0-128">-BackupSchedulesToAdd</span></span>
<span data-ttu-id="5d4b0-129">정책에 추가할 **BackupScheduleBase** 개체의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-129">Specifies an array of **BackupScheduleBase** objects to add to the policy.</span></span>
<span data-ttu-id="5d4b0-130">각 개체는 일정을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-130">Each object represents a schedule.</span></span>
<span data-ttu-id="5d4b0-131">백업 정책에는 하나 이상의 일정이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-131">A backup policy contains one or more schedules.</span></span>
<span data-ttu-id="5d4b0-132">**BackupScheduleBase** 개체를 얻으려면 **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-132">To obtain a **BackupScheduleBase** object, use the **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet.</span></span>

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

### <span data-ttu-id="5d4b0-133">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="5d4b0-133">-DeviceName</span></span>
<span data-ttu-id="5d4b0-134">백업 정책을 만들 StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-134">Specifies the name of the StorSimple device on which to create the backup policy.</span></span>

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

### <span data-ttu-id="5d4b0-135">-프로필</span><span class="sxs-lookup"><span data-stu-id="5d4b0-135">-Profile</span></span>
<span data-ttu-id="5d4b0-136">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="5d4b0-137">-VolumeIdsToAdd</span><span class="sxs-lookup"><span data-stu-id="5d4b0-137">-VolumeIdsToAdd</span></span>
<span data-ttu-id="5d4b0-138">백업 정책에 추가할 볼륨 Id의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-138">Specifies an array of the IDs of volumes to add to the backup policy.</span></span>

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

### <span data-ttu-id="5d4b0-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="5d4b0-139">-WaitForComplete</span></span>
<span data-ttu-id="5d4b0-140">이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-140">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="5d4b0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d4b0-141">CommonParameters</span></span>
<span data-ttu-id="5d4b0-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d4b0-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d4b0-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d4b0-144">입력</span><span class="sxs-lookup"><span data-stu-id="5d4b0-144">INPUTS</span></span>

### <span data-ttu-id="5d4b0-145">않아야</span><span class="sxs-lookup"><span data-stu-id="5d4b0-145">None</span></span>

## <span data-ttu-id="5d4b0-146">출력</span><span class="sxs-lookup"><span data-stu-id="5d4b0-146">OUTPUTS</span></span>

### <span data-ttu-id="5d4b0-147">BackupPolicy</span><span class="sxs-lookup"><span data-stu-id="5d4b0-147">BackupPolicy</span></span>
<span data-ttu-id="5d4b0-148">이 cmdlet은 새 일정 및 볼륨을 포함 하는 **Backuppolicy** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d4b0-148">This cmdlet returns a **BackupPolicy** object that contains the new schedules and volumes.</span></span>

## <span data-ttu-id="5d4b0-149">상속자</span><span class="sxs-lookup"><span data-stu-id="5d4b0-149">NOTES</span></span>

## <span data-ttu-id="5d4b0-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d4b0-150">RELATED LINKS</span></span>

[<span data-ttu-id="5d4b0-151">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="5d4b0-151">Get-AzureStorSimpleDeviceBackupPolicy</span></span>](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="5d4b0-152">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="5d4b0-152">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="5d4b0-153">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="5d4b0-153">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="5d4b0-154">제거-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="5d4b0-154">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="5d4b0-155">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="5d4b0-155">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="5d4b0-156">새로운 AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="5d4b0-156">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)



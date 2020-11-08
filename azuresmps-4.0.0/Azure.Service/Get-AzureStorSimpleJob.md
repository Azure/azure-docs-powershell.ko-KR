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
# <span data-ttu-id="964a0-101">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="964a0-101">Get-AzureStorSimpleJob</span></span>

## <span data-ttu-id="964a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="964a0-102">SYNOPSIS</span></span>
<span data-ttu-id="964a0-103">StorSimple 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-103">Gets StorSimple jobs.</span></span>

## <span data-ttu-id="964a0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="964a0-104">SYNTAX</span></span>

```
Get-AzureStorSimpleJob [-DeviceName <String>] [-InstanceId <String>] [-Status <String>] [-Type <String>]
 [-From <DateTime>] [-To <DateTime>] [-Skip <Int32>] [-First <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="964a0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="964a0-105">DESCRIPTION</span></span>
<span data-ttu-id="964a0-106">**Get-AzureStorSimpleJob** Cmdlet은 Azure StorSimple 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-106">The **Get-AzureStorSimpleJob** cmdlet gets Azure StorSimple jobs.</span></span>
<span data-ttu-id="964a0-107">인스턴스 ID를 지정 하 여 특정 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-107">Specify an instance ID to get a specific job.</span></span>
<span data-ttu-id="964a0-108">다른 매개 변수를 지정 하 여이 cmdlet이 가져오는 작업을 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-108">Specify other parameters to limit the jobs that this cmdlet gets.</span></span>

<span data-ttu-id="964a0-109">이 cmdlet은 최대 200 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-109">This cmdlet returns a maximum of 200 jobs.</span></span>
<span data-ttu-id="964a0-110">200 작업이 둘 이상 있는 경우 *첫 번째* 및 *건너뛰기* 매개 변수를 사용 하 여 나머지 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-110">If more than 200 jobs exist, get the remaining jobs by using the *First* and *Skip* parameters.</span></span>
<span data-ttu-id="964a0-111">*Skip* 및 50에 대 한 100 값을 *먼저* 지정 하면이 cmdlet은 첫 번째 100 결과를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-111">If you specify a value of 100 for *Skip* and 50 for *First* , this cmdlet does not return the first 100 results.</span></span>
<span data-ttu-id="964a0-112">이 메서드는 건너뛴 100 다음의 50 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-112">It returns the next 50 results after the 100 that it skips.</span></span>

## <span data-ttu-id="964a0-113">예제의</span><span class="sxs-lookup"><span data-stu-id="964a0-113">EXAMPLES</span></span>

### <span data-ttu-id="964a0-114">예제 1: ID를 사용 하 여 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="964a0-114">Example 1: Get a job by using an ID</span></span>
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

<span data-ttu-id="964a0-115">이 명령은 지정 된 ID를 가진 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-115">This command gets information for the job that has the specified ID.</span></span>

### <span data-ttu-id="964a0-116">예제 2: 장치 이름을 사용 하 여 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="964a0-116">Example 2: Get jobs by using a device name</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "8600-Bravo 001" -First 2
InstanceId                           Type                         Status                                          DeviceName                                      StartTime                                       Progress                                       
----------                           ----                         ------                                          ----------                                      ---------                                       --------                                       
1997c33f-bfcc-4d08-9aba-28068340a1f9 Backup                       Running                                         8600-Bravo 001                                  4/15/2015 1:30:02 PM                            92                                             
85074062-ef6a-408a-b6c9-2a0904bb99ca Backup                       Completed                                       8600-Bravo 001                                  4/15/2015 1:30:02 PM                            100
```

<span data-ttu-id="964a0-117">이 명령은 8600-Bravo 001 이라는 장치 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-117">This command gets information for the jobs for the device named 8600-Bravo 001.</span></span>
<span data-ttu-id="964a0-118">명령은 장치에 대 한 처음 두 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-118">The command gets the first two jobs for the device.</span></span>

### <span data-ttu-id="964a0-119">예제 3: 완료 된 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="964a0-119">Example 3: Get completed jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Status "Completed" -Skip 10 -First 2
```

<span data-ttu-id="964a0-120">이 명령은 완료 된 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-120">This command gets completed jobs.</span></span>
<span data-ttu-id="964a0-121">명령은 처음 10 개 작업을 건너뛴 후 처음 두 개의 작업만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-121">The command gets only the first two jobs after it skips the first ten jobs.</span></span>

### <span data-ttu-id="964a0-122">예제 4: 수동 백업 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="964a0-122">Example 4: Get manual backup jobs</span></span>
```
PS C:\>Get-AzureStorSimpleJob -Type "ManualBackup"
```

<span data-ttu-id="964a0-123">이 명령은 수동 백업 유형의 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-123">This command gets jobs of the manual backup type.</span></span>

### <span data-ttu-id="964a0-124">예제 5: 지정 된 시간 사이에 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="964a0-124">Example 5: Get jobs between specified times</span></span>
```
PS C:\>$StartTime = Get-Date -Year 2015 -Month 3 -Day 10
PS C:\> $EndTime = Get-Date -Year 2015 -Month 3 -Day 11 -Hour 12 -Minute 15
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" -From $StartTime -To $EndTime
```

<span data-ttu-id="964a0-125">처음 두 명령은 Get-Date cmdlet을 사용 하 여 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-125">The first two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="964a0-126">명령은 $StartTime 및 $EndTime 변수에 새 시간을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-126">The commands store the new times in the $StartTime and $EndTime variables.</span></span>
<span data-ttu-id="964a0-127">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="964a0-127">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="964a0-128">마지막 명령은 $StartTime 및 $EndTime에 저장 된 시간 사이에 Device07 이라는 장치에 대 한 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-128">The final command gets jobs for the device named Device07 between the times stored in $StartTime and $EndTime.</span></span>

## <span data-ttu-id="964a0-129">변수</span><span class="sxs-lookup"><span data-stu-id="964a0-129">PARAMETERS</span></span>

### <span data-ttu-id="964a0-130">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="964a0-130">-DeviceName</span></span>
<span data-ttu-id="964a0-131">StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-131">Specifies the name of a StorSimple device.</span></span>

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

### <span data-ttu-id="964a0-132">-첫 번째</span><span class="sxs-lookup"><span data-stu-id="964a0-132">-First</span></span>
<span data-ttu-id="964a0-133">지정 된 수의 개체만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-133">Gets only the specified number of objects.</span></span>
<span data-ttu-id="964a0-134">가져올 개체 수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-134">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="964a0-135">-보낸 사람</span><span class="sxs-lookup"><span data-stu-id="964a0-135">-From</span></span>
<span data-ttu-id="964a0-136">이 cmdlet이 가져오는 작업의 시작 날짜와 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-136">Specifies the start date and time for the jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="964a0-137">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="964a0-137">-InstanceId</span></span>
<span data-ttu-id="964a0-138">가져올 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-138">Specifies the ID of the job to get.</span></span>

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

### <span data-ttu-id="964a0-139">-프로필</span><span class="sxs-lookup"><span data-stu-id="964a0-139">-Profile</span></span>
<span data-ttu-id="964a0-140">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="964a0-141">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="964a0-142">-생략</span><span class="sxs-lookup"><span data-stu-id="964a0-142">-Skip</span></span>
<span data-ttu-id="964a0-143">지정 된 수의 개체를 무시 한 다음 나머지 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-143">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="964a0-144">건너뛸 개체 수를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-144">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="964a0-145">-상태</span><span class="sxs-lookup"><span data-stu-id="964a0-145">-Status</span></span>
<span data-ttu-id="964a0-146">상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-146">Specifies the status.</span></span>
<span data-ttu-id="964a0-147">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="964a0-148">실행</span><span class="sxs-lookup"><span data-stu-id="964a0-148">Running</span></span>
- <span data-ttu-id="964a0-149">완료</span><span class="sxs-lookup"><span data-stu-id="964a0-149">Completed</span></span>
- <span data-ttu-id="964a0-150">되었습니다</span><span class="sxs-lookup"><span data-stu-id="964a0-150">Cancelled</span></span>
- <span data-ttu-id="964a0-151">못함</span><span class="sxs-lookup"><span data-stu-id="964a0-151">Failed</span></span>
- <span data-ttu-id="964a0-152">...</span><span class="sxs-lookup"><span data-stu-id="964a0-152">Canceling</span></span>
- <span data-ttu-id="964a0-153">CompletedWithErrors</span><span class="sxs-lookup"><span data-stu-id="964a0-153">CompletedWithErrors</span></span>

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

### <span data-ttu-id="964a0-154">-To</span><span class="sxs-lookup"><span data-stu-id="964a0-154">-To</span></span>
<span data-ttu-id="964a0-155">이 cmdlet이 가져오는 작업의 종료 날짜와 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-155">Specifies the end date and time for the jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="964a0-156">-Type</span><span class="sxs-lookup"><span data-stu-id="964a0-156">-Type</span></span>
<span data-ttu-id="964a0-157">작업 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-157">Specifies the job type.</span></span>
<span data-ttu-id="964a0-158">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-158">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="964a0-159">백업할</span><span class="sxs-lookup"><span data-stu-id="964a0-159">Backup</span></span>
- <span data-ttu-id="964a0-160">ManualBackup</span><span class="sxs-lookup"><span data-stu-id="964a0-160">ManualBackup</span></span>
- <span data-ttu-id="964a0-161">복원한</span><span class="sxs-lookup"><span data-stu-id="964a0-161">Restore</span></span>
- <span data-ttu-id="964a0-162">CloneWorkflow</span><span class="sxs-lookup"><span data-stu-id="964a0-162">CloneWorkflow</span></span>
- <span data-ttu-id="964a0-163">DeviceRestore</span><span class="sxs-lookup"><span data-stu-id="964a0-163">DeviceRestore</span></span>
- <span data-ttu-id="964a0-164">Update</span><span class="sxs-lookup"><span data-stu-id="964a0-164">Update</span></span>
- <span data-ttu-id="964a0-165">SupportPackage</span><span class="sxs-lookup"><span data-stu-id="964a0-165">SupportPackage</span></span>
- <span data-ttu-id="964a0-166">VirtualApplianceProvisioning</span><span class="sxs-lookup"><span data-stu-id="964a0-166">VirtualApplianceProvisioning</span></span>

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

### <span data-ttu-id="964a0-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="964a0-167">CommonParameters</span></span>
<span data-ttu-id="964a0-168">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="964a0-169">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="964a0-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="964a0-170">입력</span><span class="sxs-lookup"><span data-stu-id="964a0-170">INPUTS</span></span>

### <span data-ttu-id="964a0-171">않아야</span><span class="sxs-lookup"><span data-stu-id="964a0-171">None</span></span>
<span data-ttu-id="964a0-172">이 cmdlet에는 입력을 파이프가 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-172">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="964a0-173">출력</span><span class="sxs-lookup"><span data-stu-id="964a0-173">OUTPUTS</span></span>

### <span data-ttu-id="964a0-174">IList \<DeviceJobDetails\> , devicejobdetails</span><span class="sxs-lookup"><span data-stu-id="964a0-174">IList\<DeviceJobDetails\>, DeviceJobDetails</span></span>
<span data-ttu-id="964a0-175">이 cmdlet은 작업 세부 정보 개체의 목록을 반환 하거나, *InstanceID* 매개 변수를 지정 하는 경우 단일 작업 정보 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="964a0-175">This cmdlet returns a list of job details objects, or, if you specify the *InstanceID* parameter, it returns a single job detail object.</span></span>

## <span data-ttu-id="964a0-176">상속자</span><span class="sxs-lookup"><span data-stu-id="964a0-176">NOTES</span></span>

## <span data-ttu-id="964a0-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="964a0-177">RELATED LINKS</span></span>

[<span data-ttu-id="964a0-178">중지-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="964a0-178">Stop-AzureStorSimpleJob</span></span>](./Stop-AzureStorSimpleJob.md)



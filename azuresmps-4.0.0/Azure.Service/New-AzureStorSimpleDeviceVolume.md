---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 049201C9-590F-47EB-9030-25F80CD8DFA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f3337556a9d7bd52e5800af5cdbd65b71ab9818
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045523"
---
# <span data-ttu-id="44d24-101">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="44d24-101">New-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="44d24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44d24-102">SYNOPSIS</span></span>
<span data-ttu-id="44d24-103">지정 된 볼륨 컨테이너에 볼륨을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-103">Creates a volume in a specified volume container.</span></span>

## <span data-ttu-id="44d24-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44d24-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer> -VolumeName <String>
 -VolumeSizeInBytes <Int64>
 -AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>
 -VolumeAppType <AppType> -Online <Boolean> -EnableDefaultBackup <Boolean> -EnableMonitoring <Boolean>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="44d24-105">설명은</span><span class="sxs-lookup"><span data-stu-id="44d24-105">DESCRIPTION</span></span>
<span data-ttu-id="44d24-106">**AzureStorSimpleDeviceVolume** cmdlet은 지정 된 볼륨 컨테이너에 볼륨을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-106">The **New-AzureStorSimpleDeviceVolume** cmdlet creates a volume in a specified volume container.</span></span>
<span data-ttu-id="44d24-107">이 cmdlet은 각 볼륨을 하나 이상의 액세스 제어 레코드와 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-107">This cmdlet associates each volume with one or more access control records.</span></span>
<span data-ttu-id="44d24-108">**Accesscontrolrecord** 개체를 가져오려면 **Get-AzureStorSimpleAccessControlRecord** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-108">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="44d24-109">볼륨에 대 한 이름, 크기 및 AppType를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-109">Specify a name, size, and AppType for the volume.</span></span>
<span data-ttu-id="44d24-110">또한 볼륨을 온라인으로 만들지 여부, 기본 백업을 사용할지 여부, 모니터링을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-110">Also, specify whether to create the volume online, whether to enable default backup, and whether to enable monitoring.</span></span>

## <span data-ttu-id="44d24-111">예제의</span><span class="sxs-lookup"><span data-stu-id="44d24-111">EXAMPLES</span></span>

### <span data-ttu-id="44d24-112">예제 1: 볼륨 만들기</span><span class="sxs-lookup"><span data-stu-id="44d24-112">Example 1: Create a volume</span></span>
```
PS C:\>$AcrList = Get-AzureStorSimpleAccessControlRecord
PS C:\> Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer07" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Size 2000000000 -AccessControlRecords $AcrList -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False

VERBOSE: ClientRequestId: a29d1a84-1f81-4f20-9130-7adfe45e41fb_PS
VERBOSE: ClientRequestId: 8fa63df1-3f81-4029-a536-b536a70068ad_PS
VERBOSE: ClientRequestId: 964c5744-8bb1-4f70-beda-95ca4c7f3eb6_PS
VERBOSE: ClientRequestId: f09fff3a-54fa-4a0e-93db-b079260ed2dd_PS
VERBOSE: ClientRequestId: 59aa29e3-8044-411a-adae-b64a2681ffed_PS
VERBOSE: ClientRequestId: 0ffd0297-19be-40fe-a64e-6a2947d831b4_PS
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90 for tracking the task's status
VERBOSE: Volume container with name: VolumeContainer07 is found.
```

<span data-ttu-id="44d24-113">첫 번째 명령은 **AzureStorSimpleAccessControlRecord** cmdlet을 사용 하 여 StorSimple Manager 서비스 구성에서 액세스 제어 레코드를 가져온 다음 $AcrList 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-113">The first command gets the access control records in the StorSimple Manager service configuration by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet, and then stores them in the $AcrList variable.</span></span>

<span data-ttu-id="44d24-114">두 번째 명령은 **AzureStorSimpleDeviceVolumeContainer** cmdlet을 사용 하 여 Contoso63-AppVm 이라는 장치에 대 한 VolumeContainer07 이라는 볼륨 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-114">The second command gets the volume container named VolumeContainer07 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="44d24-115">이 명령은 파이프라인 연산자를 사용 하 여 해당 컨테이너를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-115">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="44d24-116">이 cmdlet은 볼륨을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-116">This cmdlet creates the volume.</span></span>
<span data-ttu-id="44d24-117">명령은 볼륨 이름, 크기 및 $AcrList에 저장 된 액세스 제어 레코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-117">The command specifies the name for the volume, the size, and the access control records stored in $AcrList.</span></span>
<span data-ttu-id="44d24-118">이 명령은 작업을 시작한 다음 **Taskresponse** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-118">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="44d24-119">작업 상태를 확인 하려면 **Get-AzureStorSimpleTask** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-119">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="44d24-120">예제 2: 액세스 제어 권한이 없는 볼륨 만들기 recordsaccess 컨트롤</span><span class="sxs-lookup"><span data-stu-id="44d24-120">Example 2: Create a volume without Access Controlaccess control recordsaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer01" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume22" -Size 2000000000 -AccessControlRecords @() -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False -WaitForComplete
VERBOSE: ClientRequestId: 3f359790-7e1f-48e7-acf8-ecabba850966_PS
VERBOSE: ClientRequestId: 2723ebcf-cd72-47bb-99b5-0c099d45641b_PS
VERBOSE: ClientRequestId: e605091f-dd63-42a7-bda2-24753cbc1f9a_PS
VERBOSE: ClientRequestId: b3fd08c3-67c5-4309-9591-15d92c360469_PS
VERBOSE: ClientRequestId: 15a024a3-b0c9-4f83-9c34-0ed8b95d024b_PS
VERBOSE: ClientRequestId: c13f92f9-aea1-40dd-af80-3affe273adbe_PS


TaskId       : ceef657e-390e-4f7a-aab7-669a29c29e7f
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 1d79febf-f752-4255-af2d-230d40773bc6_PS
AccessType             : NoAccess
AcrIdList              : {}
AcrList                : {}
AppType                : PrimaryVolume
DataContainer          : Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainer
DataContainerId        : 68b63d15-6aa5-4e69-9f9d-4a0bc607d6e9
InstanceId             : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd
InternalInstanceId     : 
IsBackupEnabled        : False
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
Name                   : Volume22
Online                 : True
OperationInProgress    : None
SizeInBytes            : 2000000000
VSN                    : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd

VERBOSE: Volume container with name: VolumeContainer01 is found.
```

<span data-ttu-id="44d24-121">이 명령은 **AzureStorSimpleDeviceVolumeContainer** cmdlet을 사용 하 여 Contoso63-AppVm 이라는 장치에 대 한 VolumeContainer01 이라는 볼륨 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-121">This command gets the volume container named VolumeContainer01 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="44d24-122">이 명령은 파이프라인 연산자를 사용 하 여 해당 컨테이너를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-122">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="44d24-123">이 cmdlet은 볼륨을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-123">This cmdlet creates the volume.</span></span>
<span data-ttu-id="44d24-124">명령에서는 볼륨 이름, 크기 및 액세스 제어 레코드의 빈 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-124">The command specifies the name for the volume, the size, and an empty value for access control records.</span></span>
<span data-ttu-id="44d24-125">이 명령은 *Waitforcomplete* 매개 변수를 지정 하므로 볼륨을 만든 후 **TaskStatusInfo** 를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-125">This command specifies the *WaitForComplete* parameter, so it returns a **TaskStatusInfo** after it creates the volume.</span></span>

<span data-ttu-id="44d24-126">명령에 액세스 제어 레코드가 지정 되어 있지 않으므로이 볼륨에 액세스할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-126">Because the command specifies no access control records, this volume cannot be accessed.</span></span>
<span data-ttu-id="44d24-127">나중에 **Set-AzureStorSimpleDeviceVolume** cmdlet을 사용 하 여 액세스를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-127">You can add access, later, by using **Set-AzureStorSimpleDeviceVolume** cmdlet.</span></span>

## <span data-ttu-id="44d24-128">변수</span><span class="sxs-lookup"><span data-stu-id="44d24-128">PARAMETERS</span></span>

### <span data-ttu-id="44d24-129">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="44d24-129">-AccessControlRecords</span></span>
<span data-ttu-id="44d24-130">볼륨과 연결할 액세스 제어 레코드 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-130">Specifies a list of access control records to associate with the volume.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44d24-131">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="44d24-131">-DeviceName</span></span>
<span data-ttu-id="44d24-132">볼륨을 만들 StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-132">Specifies the name of the StorSimple device on which to create the volume.</span></span>

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

### <span data-ttu-id="44d24-133">-EnableDefaultBackup</span><span class="sxs-lookup"><span data-stu-id="44d24-133">-EnableDefaultBackup</span></span>
<span data-ttu-id="44d24-134">볼륨에 대 한 기본 백업을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-134">Specifies whether to enable default backup for the volume.</span></span>

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

### <span data-ttu-id="44d24-135">-EnableMonitoring</span><span class="sxs-lookup"><span data-stu-id="44d24-135">-EnableMonitoring</span></span>
<span data-ttu-id="44d24-136">볼륨에 대 한 모니터링을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-136">Specifies whether to enable monitoring for the volume.</span></span>

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

### <span data-ttu-id="44d24-137">-온라인</span><span class="sxs-lookup"><span data-stu-id="44d24-137">-Online</span></span>
<span data-ttu-id="44d24-138">온라인으로 볼륨을 만들지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-138">Specifies whether to create the volume online.</span></span>

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

### <span data-ttu-id="44d24-139">-프로필</span><span class="sxs-lookup"><span data-stu-id="44d24-139">-Profile</span></span>
<span data-ttu-id="44d24-140">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-140">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="44d24-141">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="44d24-141">-VolumeAppType</span></span>
<span data-ttu-id="44d24-142">주 볼륨을 만들지 보관할 지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-142">Specifies whether to create a primary or archive volume.</span></span>
<span data-ttu-id="44d24-143">유효한 값은 PrimaryVolume 및 ArchiveVolume입니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-143">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44d24-144">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="44d24-144">-VolumeContainer</span></span>
<span data-ttu-id="44d24-145">볼륨을 만들 컨테이너를 **DataContainer** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-145">Specifies the container, as a **DataContainer** object, in which to create the volume.</span></span>
<span data-ttu-id="44d24-146">**VirtualDisk** 개체를 얻으려면 **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-146">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44d24-147">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="44d24-147">-VolumeName</span></span>
<span data-ttu-id="44d24-148">새 볼륨의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-148">Specifies a name for the new volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44d24-149">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="44d24-149">-VolumeSizeInBytes</span></span>
<span data-ttu-id="44d24-150">볼륨 크기를 바이트로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-150">Specifies the volume size in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44d24-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="44d24-151">-WaitForComplete</span></span>
<span data-ttu-id="44d24-152">이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-152">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="44d24-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44d24-153">CommonParameters</span></span>
<span data-ttu-id="44d24-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44d24-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44d24-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44d24-156">입력</span><span class="sxs-lookup"><span data-stu-id="44d24-156">INPUTS</span></span>

### <span data-ttu-id="44d24-157">DataContainer, List\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="44d24-157">DataContainer, List\<AccessControlRecord\></span></span>
<span data-ttu-id="44d24-158">이 cmdlet은 **DataContainer** 개체와 새 볼륨에 대 한 **accesscontrolrecord** 개체 목록을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-158">This cmdlet accepts a **DataContainer** object and a list of **AccessControlRecord** objects for the new volume.</span></span>

## <span data-ttu-id="44d24-159">출력</span><span class="sxs-lookup"><span data-stu-id="44d24-159">OUTPUTS</span></span>

### <span data-ttu-id="44d24-160">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="44d24-160">TaskStatusInfo</span></span>
<span data-ttu-id="44d24-161">*Waitforcomplete* 매개 변수를 지정 하는 경우이 Cmdlet은 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="44d24-161">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="44d24-162">상속자</span><span class="sxs-lookup"><span data-stu-id="44d24-162">NOTES</span></span>

## <span data-ttu-id="44d24-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44d24-163">RELATED LINKS</span></span>

[<span data-ttu-id="44d24-164">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="44d24-164">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="44d24-165">제거-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="44d24-165">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="44d24-166">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="44d24-166">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="44d24-167">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="44d24-167">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="44d24-168">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="44d24-168">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="44d24-169">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="44d24-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)



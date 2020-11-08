---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 39E9BB88-6AD8-4B05-9498-35393E22BA30
online version: ''
schema: 2.0.0
ms.openlocfilehash: 234b1f7fa2719cc1b34e6bcd0b8e8fd340acc4af
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046418"
---
# <span data-ttu-id="43748-101">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="43748-101">Set-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="43748-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43748-102">SYNOPSIS</span></span>
<span data-ttu-id="43748-103">기존 볼륨의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-103">Updates the properties of an existing volume.</span></span>

## <span data-ttu-id="43748-104">구문과</span><span class="sxs-lookup"><span data-stu-id="43748-104">SYNTAX</span></span>

### <span data-ttu-id="43748-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="43748-105">IdentifyByName</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="43748-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="43748-106">IdentifyByObject</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="43748-107">설명은</span><span class="sxs-lookup"><span data-stu-id="43748-107">DESCRIPTION</span></span>
<span data-ttu-id="43748-108">**Set-AzureStorSimpleDeviceVolume** cmdlet은 기존 볼륨의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-108">The **Set-AzureStorSimpleDeviceVolume** cmdlet updates the properties of an existing volume.</span></span>
<span data-ttu-id="43748-109">이 cmdlet은 볼륨을 하나 이상의 액세스 제어 레코드와 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-109">This cmdlet associates a volume with one or more access control records.</span></span>
<span data-ttu-id="43748-110">**Accesscontrolrecord** 개체를 가져오려면 **Get-AzureStorSimpleAccessControlRecord** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-110">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="43748-111">볼륨의 크기 또는 유형을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-111">Update the size or type for the volume.</span></span>
<span data-ttu-id="43748-112">또한 볼륨을 온라인으로 만들지 여부를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-112">Also, update whether to create the volume online.</span></span>

## <span data-ttu-id="43748-113">예제의</span><span class="sxs-lookup"><span data-stu-id="43748-113">EXAMPLES</span></span>

### <span data-ttu-id="43748-114">예제 1: 볼륨의 온라인 값 업데이트</span><span class="sxs-lookup"><span data-stu-id="43748-114">Example 1: Update online value for a volume</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $False
VERBOSE: ClientRequestId: f2869570-ea47-4be7-801e-9c0f22f2600d_PS
VERBOSE: ClientRequestId: c70bb86a-51d3-4390-be17-4d0847641dc3_PS
VERBOSE: ClientRequestId: d20cb5b2-6b3c-4e06-af99-cada28c5e50a_PS
VERBOSE: ClientRequestId: ab6d533e-b55b-4cfb-9c58-9153295e0547_PS
de7000f1-29c7-4102-a375-b52432f9e67e
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
de7000f1-29c7-4102-a375-b52432f9e67e for tracking the task's status
```

<span data-ttu-id="43748-115">이 명령은 Volume18 이라는 볼륨을 업데이트 하 여 $False의 온라인 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-115">This command updates the volume named Volume18 to have an online value of $False.</span></span>
<span data-ttu-id="43748-116">이 명령은 작업을 시작한 다음 **Taskresponse** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-116">This command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="43748-117">작업의 상태를 보려면 **Get-AzureStorSimpleTask** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-117">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="43748-118">예제 2: 온라인 값 수정 및 입력</span><span class="sxs-lookup"><span data-stu-id="43748-118">Example 2: Modify online value and type</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $True -VolumeAppType ArchiveVolume 
VERBOSE: ClientRequestId: af42b02a-645e-4801-a2d7-4197511c68cf_PS
VERBOSE: ClientRequestId: 7cb4f3b4-548e-42dc-a38c-0df0911c5206_PS
VERBOSE: ClientRequestId: 7cc706ad-a58f-4939-8e78-cabae8379a51_PS
VERBOSE: ClientRequestId: 6bed21d5-12fc-4a12-a89c-120bdb5636b1_PS
aa977225-af78-4c93-b754-72704afc928f
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
aa977225-af78-4c93-b754-72704afc928f for tracking the task's status
```

<span data-ttu-id="43748-119">이 명령은 Volume18 이라는 볼륨을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-119">This command updates the volume named Volume18.</span></span>
<span data-ttu-id="43748-120">이 메서드는 형식을 수정 하 고 *Online* 매개 변수 값을 $True 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-120">It modifies the type and changes the value of the *Online* parameter to $True.</span></span>

## <span data-ttu-id="43748-121">변수</span><span class="sxs-lookup"><span data-stu-id="43748-121">PARAMETERS</span></span>

### <span data-ttu-id="43748-122">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="43748-122">-AccessControlRecords</span></span>
<span data-ttu-id="43748-123">볼륨과 연결할 액세스 제어 레코드 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-123">Specifies a list of access control records to associate with the volume.</span></span>

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

### <span data-ttu-id="43748-124">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="43748-124">-DeviceName</span></span>
<span data-ttu-id="43748-125">볼륨을 업데이트할 StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-125">Specifies the name of the StorSimple device on which to update the volume exists.</span></span>

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

### <span data-ttu-id="43748-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="43748-126">-InformationAction</span></span>
<span data-ttu-id="43748-127">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="43748-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="43748-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43748-129">하기로</span><span class="sxs-lookup"><span data-stu-id="43748-129">Continue</span></span>
- <span data-ttu-id="43748-130">숨기기</span><span class="sxs-lookup"><span data-stu-id="43748-130">Ignore</span></span>
- <span data-ttu-id="43748-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="43748-131">Inquire</span></span>
- <span data-ttu-id="43748-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="43748-132">SilentlyContinue</span></span>
- <span data-ttu-id="43748-133">중지가</span><span class="sxs-lookup"><span data-stu-id="43748-133">Stop</span></span>
- <span data-ttu-id="43748-134">대기</span><span class="sxs-lookup"><span data-stu-id="43748-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43748-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="43748-135">-InformationVariable</span></span>
<span data-ttu-id="43748-136">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43748-137">-NewName</span><span class="sxs-lookup"><span data-stu-id="43748-137">-NewName</span></span>
<span data-ttu-id="43748-138">StorSimple 장치에 대 한 새 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-138">Specifies a new name for the StorSimple device.</span></span>

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

### <span data-ttu-id="43748-139">-온라인</span><span class="sxs-lookup"><span data-stu-id="43748-139">-Online</span></span>
<span data-ttu-id="43748-140">볼륨이 온라인 상태 인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-140">Specifies whether the volume is online.</span></span>

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

### <span data-ttu-id="43748-141">-프로필</span><span class="sxs-lookup"><span data-stu-id="43748-141">-Profile</span></span>
<span data-ttu-id="43748-142">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-142">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="43748-143">-볼륨</span><span class="sxs-lookup"><span data-stu-id="43748-143">-Volume</span></span>
<span data-ttu-id="43748-144">업데이트할 볼륨의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-144">Specifies the name of the volume to update.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43748-145">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="43748-145">-VolumeAppType</span></span>
<span data-ttu-id="43748-146">볼륨을 기본 또는 보관 볼륨으로 업데이트할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-146">Specifies whether to update the volume to be a primary or archive volume.</span></span>
<span data-ttu-id="43748-147">유효한 값은 PrimaryVolume 및 ArchiveVolume입니다.</span><span class="sxs-lookup"><span data-stu-id="43748-147">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43748-148">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="43748-148">-VolumeName</span></span>
<span data-ttu-id="43748-149">업데이트할 볼륨의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-149">Specifies the name of the volume to update.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43748-150">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="43748-150">-VolumeSizeInBytes</span></span>
<span data-ttu-id="43748-151">볼륨의 업데이트 된 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-151">Specifies the updated size, in bytes, for the volume.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43748-152">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="43748-152">-WaitForComplete</span></span>
<span data-ttu-id="43748-153">이 cmdlet이 작업을 완료 한 후에 Windows PowerShell 콘솔에 제어를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="43748-153">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="43748-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43748-154">CommonParameters</span></span>
<span data-ttu-id="43748-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43748-156">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43748-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43748-157">입력</span><span class="sxs-lookup"><span data-stu-id="43748-157">INPUTS</span></span>

### <span data-ttu-id="43748-158">목록\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="43748-158">List\<AccessControlRecord\></span></span>
<span data-ttu-id="43748-159">이 cmdlet은 볼륨에 연결 하는 **Accesscontrolrecord** 개체 목록을 수락 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-159">This cmdlet accepts a list of **AccessControlRecord** objects to associate to a volume.</span></span>

## <span data-ttu-id="43748-160">출력</span><span class="sxs-lookup"><span data-stu-id="43748-160">OUTPUTS</span></span>

### <span data-ttu-id="43748-161">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="43748-161">TaskStatusInfo</span></span>
<span data-ttu-id="43748-162">*Waitforcomplete* 매개 변수를 지정 하는 경우이 Cmdlet은 **TaskStatusInfo** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="43748-162">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="43748-163">상속자</span><span class="sxs-lookup"><span data-stu-id="43748-163">NOTES</span></span>

## <span data-ttu-id="43748-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43748-164">RELATED LINKS</span></span>

[<span data-ttu-id="43748-165">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="43748-165">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="43748-166">새로운 AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="43748-166">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="43748-167">제거-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="43748-167">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="43748-168">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="43748-168">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="43748-169">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="43748-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)



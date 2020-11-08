---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 79EE846E-D5BE-4808-BC6F-E3B16A308AB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9d0cd7ef0eacc7ff3e38c4619b60a0bd61f24f1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045566"
---
# <span data-ttu-id="a57ff-101">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="a57ff-101">Get-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="a57ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a57ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a57ff-103">장치에서 볼륨을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a57ff-103">Gets volumes on a device.</span></span>

## <span data-ttu-id="a57ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a57ff-104">SYNTAX</span></span>

### <span data-ttu-id="a57ff-105">IdentifyByParentObject</span><span class="sxs-lookup"><span data-stu-id="a57ff-105">IdentifyByParentObject</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a57ff-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="a57ff-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a57ff-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a57ff-107">DESCRIPTION</span></span>
<span data-ttu-id="a57ff-108">**AzureStorSimpleDeviceVolume** cmdlet은 지정 된 이름의 볼륨 컨테이너 또는 볼륨에 대 한 볼륨 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a57ff-108">The **Get-AzureStorSimpleDeviceVolume** cmdlet gets a list of volumes for a specified volume container, or volume that has the specified name.</span></span>
<span data-ttu-id="a57ff-109">반환 된 개체에는 다음 속성이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a57ff-109">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="a57ff-110">**AccessType**</span><span class="sxs-lookup"><span data-stu-id="a57ff-110">**AccessType**</span></span>
- <span data-ttu-id="a57ff-111">**AcrList**</span><span class="sxs-lookup"><span data-stu-id="a57ff-111">**AcrList**</span></span>
- <span data-ttu-id="a57ff-112">**AppType**</span><span class="sxs-lookup"><span data-stu-id="a57ff-112">**AppType**</span></span>
- <span data-ttu-id="a57ff-113">**DataContainer**</span><span class="sxs-lookup"><span data-stu-id="a57ff-113">**DataContainer**</span></span>
- <span data-ttu-id="a57ff-114">**DataContainerId**</span><span class="sxs-lookup"><span data-stu-id="a57ff-114">**DataContainerId**</span></span>
- <span data-ttu-id="a57ff-115">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="a57ff-115">**InstanceId**</span></span>
- <span data-ttu-id="a57ff-116">**IsBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="a57ff-116">**IsBackupEnabled**</span></span>
- <span data-ttu-id="a57ff-117">**IsDefaultBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="a57ff-117">**IsDefaultBackupEnabled**</span></span>
- <span data-ttu-id="a57ff-118">**IsMonitoringEnabled**</span><span class="sxs-lookup"><span data-stu-id="a57ff-118">**IsMonitoringEnabled**</span></span>
- <span data-ttu-id="a57ff-119">**성을**</span><span class="sxs-lookup"><span data-stu-id="a57ff-119">**Name**</span></span>
- <span data-ttu-id="a57ff-120">**온라인**</span><span class="sxs-lookup"><span data-stu-id="a57ff-120">**Online**</span></span>
- <span data-ttu-id="a57ff-121">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="a57ff-121">**OperationInProgress**</span></span>
- <span data-ttu-id="a57ff-122">**SizeInBytes**</span><span class="sxs-lookup"><span data-stu-id="a57ff-122">**SizeInBytes**</span></span>
- <span data-ttu-id="a57ff-123">**VSN**</span><span class="sxs-lookup"><span data-stu-id="a57ff-123">**VSN**</span></span>

## <span data-ttu-id="a57ff-124">예제의</span><span class="sxs-lookup"><span data-stu-id="a57ff-124">EXAMPLES</span></span>

### <span data-ttu-id="a57ff-125">예제 1: 지정 된 컨테이너에 볼륨 가져오기</span><span class="sxs-lookup"><span data-stu-id="a57ff-125">Example 1: Get volumes in a specified container</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container03" | Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
InstanceId             : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c
Name                   : Volume 1 Clone
Online                 : True
SizeInBytes            : 3298534883328
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c

InstanceId             : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe
Name                   : Volume 3 Clone
Online                 : True
SizeInBytes            : 1717986918400
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe

InstanceId             : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
Name                   : Volume 4
Online                 : True
SizeInBytes            : 1610612736000
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
```

<span data-ttu-id="a57ff-126">이 명령은 **AzureStorSimpleDeviceVolumeContainer** cmdlet을 사용 하 여 Contoso63-AppVm 이라는 장치에서 Container03 이라는 볼륨 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a57ff-126">This command gets the volume container named Container03 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="a57ff-127">이 명령은 파이프라인 연산자를 사용 하 여 해당 컨테이너를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57ff-127">The command uses the pipeline operator to pass that container to the current cmdlet.</span></span>
<span data-ttu-id="a57ff-128">해당 cmdlet은 Contoso63 이라는 장치에 대 한 해당 컨테이너의 모든 볼륨을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a57ff-128">That cmdlet gets all the volumes in that container for the device named Contoso63-AppVm.</span></span>

### <span data-ttu-id="a57ff-129">예제 2: 이름을 사용 하 여 볼륨 가져오기</span><span class="sxs-lookup"><span data-stu-id="a57ff-129">Example 2: Get a volume by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18"
InstanceId             : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
Name                   : Volume18
Online                 : True
SizeInBytes            : 2748779069440
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
```

<span data-ttu-id="a57ff-130">이 명령은 Contoso63-AppVm 이라는 장치에서 Volume18 이라는 볼륨을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a57ff-130">This command gets the volume named Volume18 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="a57ff-131">변수</span><span class="sxs-lookup"><span data-stu-id="a57ff-131">PARAMETERS</span></span>

### <span data-ttu-id="a57ff-132">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="a57ff-132">-DeviceName</span></span>
<span data-ttu-id="a57ff-133">볼륨을 가져올 StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57ff-133">Specifies the name of the StorSimple device from which to get volumes.</span></span>

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

### <span data-ttu-id="a57ff-134">-프로필</span><span class="sxs-lookup"><span data-stu-id="a57ff-134">-Profile</span></span>
<span data-ttu-id="a57ff-135">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57ff-135">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="a57ff-136">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="a57ff-136">-VolumeContainer</span></span>
<span data-ttu-id="a57ff-137">가져올 볼륨을 포함 하는 **DataContainer** 개체로 볼륨 컨테이너를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57ff-137">Specifies the volume container, as a **DataContainer** object, that includes the volumes to get.</span></span>
<span data-ttu-id="a57ff-138">**DataContainer** 을 얻으려면 **AzureStorSimpleDeviceVolumeContainer** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57ff-138">To obtain a **DataContainer** , use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: IdentifyByParentObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a57ff-139">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="a57ff-139">-VolumeName</span></span>
<span data-ttu-id="a57ff-140">가져올 볼륨의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57ff-140">Specifies the name of the volume to get.</span></span>

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

### <span data-ttu-id="a57ff-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a57ff-141">CommonParameters</span></span>
<span data-ttu-id="a57ff-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57ff-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a57ff-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a57ff-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a57ff-144">입력</span><span class="sxs-lookup"><span data-stu-id="a57ff-144">INPUTS</span></span>

### <span data-ttu-id="a57ff-145">DataContainer</span><span class="sxs-lookup"><span data-stu-id="a57ff-145">DataContainer</span></span>
<span data-ttu-id="a57ff-146">이 cmdlet은 가져올 볼륨이 포함 된 **DataContainer** 개체를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57ff-146">This cmdlet accepts a **DataContainer** object that contains the volume to get.</span></span>

## <span data-ttu-id="a57ff-147">출력</span><span class="sxs-lookup"><span data-stu-id="a57ff-147">OUTPUTS</span></span>

### <span data-ttu-id="a57ff-148">VirtualDisk, IList\<VirtualDisk\></span><span class="sxs-lookup"><span data-stu-id="a57ff-148">VirtualDisk, IList\<VirtualDisk\></span></span>
<span data-ttu-id="a57ff-149">*VolumeName* 매개 변수를 지정 하면이 Cmdlet은 **VirtualDisk** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57ff-149">This cmdlet returns a **VirtualDisk** object if you specify the *VolumeName* parameter.</span></span>
<span data-ttu-id="a57ff-150">*VolumeContainer* 를 지정 하는 경우이 Cmdlet은 **IList \<VirtualDisk\>** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a57ff-150">If you specify the *VolumeContainer* , this cmdlet returns an **IList\<VirtualDisk\>** object.</span></span>

## <span data-ttu-id="a57ff-151">상속자</span><span class="sxs-lookup"><span data-stu-id="a57ff-151">NOTES</span></span>

## <span data-ttu-id="a57ff-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a57ff-152">RELATED LINKS</span></span>

[<span data-ttu-id="a57ff-153">새로운 AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="a57ff-153">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="a57ff-154">제거-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="a57ff-154">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="a57ff-155">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="a57ff-155">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="a57ff-156">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="a57ff-156">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)



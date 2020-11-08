---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045776"
---
# <span data-ttu-id="89420-101">Start-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="89420-101">Start-AzureStorSimpleDeviceFailoverJob</span></span>

## <span data-ttu-id="89420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89420-102">SYNOPSIS</span></span>
<span data-ttu-id="89420-103">볼륨 컨테이너 그룹의 장애 조치 (failover) 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-103">Initiates a failover operation of volume container groups.</span></span>

## <span data-ttu-id="89420-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89420-104">SYNTAX</span></span>

### <span data-ttu-id="89420-105">비어 있음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="89420-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="89420-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="89420-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="89420-107">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="89420-107">IdentifyByName</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="89420-108">설명은</span><span class="sxs-lookup"><span data-stu-id="89420-108">DESCRIPTION</span></span>
<span data-ttu-id="89420-109">**AzureStorSimpleDeviceFailoverJob** cmdlet은 한 장치에서 다른 장치로 하나 이상의 볼륨 컨테이너 그룹의 장애 조치 (failover) 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-109">The **Start-AzureStorSimpleDeviceFailoverJob** cmdlet initiates a failover operation of one or more volume container groups from one device to another.</span></span>

## <span data-ttu-id="89420-110">예제의</span><span class="sxs-lookup"><span data-stu-id="89420-110">EXAMPLES</span></span>

### <span data-ttu-id="89420-111">예제 1: 명명 된 장치 및 명명 된 대상 장치에 대 한 장애 조치 작업 시작</span><span class="sxs-lookup"><span data-stu-id="89420-111">Example 1: Start a failover job for a named device and named target device</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="89420-112">이 명령은 **AzureStorSimpleFailoverVolumeContainers** cmdlet을 사용 하 여 ChewD_App7 라는 장치에 대 한 장애 조치 볼륨 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89420-112">This command gets the failover volume containers for the device named ChewD_App7 by using the **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet.</span></span>
<span data-ttu-id="89420-113">명령이 **IsDCGroupEligibleForDR** 속성에 대 한 $True 이외의 값을 갖는 컨테이너가 **있는 Where 개체** cmdlet에 결과를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-113">The command passes the results to the **Where-Object** cmdlet, which drops those containers that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="89420-114">자세한 내용은을 입력 `Get-Help Where-Object` 하세요.</span><span class="sxs-lookup"><span data-stu-id="89420-114">For more information, type `Get-Help Where-Object`.</span></span>
<span data-ttu-id="89420-115">현재 cmdlet은 나머지 장애 조치 볼륨 컨테이너에 대 한 장애 조치 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-115">The current cmdlet starts failover jobs for the remaining failover volume containers.</span></span>
<span data-ttu-id="89420-116">명령은 장치 이름 및 대상 디바이스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-116">The command specifies the device name and target device name.</span></span>
<span data-ttu-id="89420-117">명령은 cmdlet이 시작 되는 작업의 인스턴스 ID를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-117">The command returns the instance ID of the job that the cmdlet starts.</span></span>

### <span data-ttu-id="89420-118">예제 2: 장치 및 ID로 지정 된 대상 장치에 대 한 장애 조치 작업 시작</span><span class="sxs-lookup"><span data-stu-id="89420-118">Example 2: Start a failover job for a device and target device specified by ID</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="89420-119">이 명령은 **AzureStorSimpleFailoverVolumeContainers** 를 사용 하 여 ChewD_App7 라는 장치에 대 한 장애 조치 볼륨 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89420-119">This command gets the failover volume containers for the device named ChewD_App7 by using **Get-AzureStorSimpleFailoverVolumeContainers**.</span></span>
<span data-ttu-id="89420-120">명령이 **IsDCGroupEligibleForDR** 속성에 대 한 $True 이외의 값이 있는 containters를 삭제 하는 해당 결과를 **Where 개체** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-120">The command passes the results to **Where-Object** , which drops those containters that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="89420-121">Cmdlet은 해당 결과를 **개체 선택** cmdlet에 전달 하 여 현재 cmdlet에 전달할 첫 번째 개체를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-121">The cmdlet passes the results to the **Select-Object** cmdlet, which selects the first object to pass to the current cmdlet.</span></span>
<span data-ttu-id="89420-122">자세한 내용은을 입력 `Get-Help Select-Object` 하세요.</span><span class="sxs-lookup"><span data-stu-id="89420-122">For more information, type `Get-Help Select-Object`.</span></span>
<span data-ttu-id="89420-123">현재 cmdlet은 선택한 장애 조치 볼륨 컨테이너에 대 한 장애 조치 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-123">The current cmdlet starts failover jobs for the selected failover volume container.</span></span>
<span data-ttu-id="89420-124">명령은 장치 ID와 대상 디바이스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-124">The command specifies the device ID and target device ID.</span></span>
<span data-ttu-id="89420-125">명령은 cmdlet이 시작 되는 작업의 인스턴스 ID를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-125">The command returns the instance ID of the job that the cmdlet starts.</span></span>

## <span data-ttu-id="89420-126">변수</span><span class="sxs-lookup"><span data-stu-id="89420-126">PARAMETERS</span></span>

### <span data-ttu-id="89420-127">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="89420-127">-DeviceId</span></span>
<span data-ttu-id="89420-128">볼륨 컨테이너 그룹이 있는 StorSimple 장치의 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-128">Specifies the instance ID of the StorSimple device on which the volume container groups exist.</span></span>

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

### <span data-ttu-id="89420-129">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="89420-129">-DeviceName</span></span>
<span data-ttu-id="89420-130">볼륨 컨테이너 그룹이 있는 StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-130">Specifies the name of the StorSimple device on which the volume container groups exist.</span></span>

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

### <span data-ttu-id="89420-131">-Force</span><span class="sxs-lookup"><span data-stu-id="89420-131">-Force</span></span>
<span data-ttu-id="89420-132">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89420-133">-프로필</span><span class="sxs-lookup"><span data-stu-id="89420-133">-Profile</span></span>
<span data-ttu-id="89420-134">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-134">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="89420-135">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="89420-135">-TargetDeviceId</span></span>
<span data-ttu-id="89420-136">이 cmdlet이 볼륨 컨테이너 그룹에 대해 장애 조치 하는 StorSimple 장치의 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-136">Specifies the instance ID of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

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

### <span data-ttu-id="89420-137">-TargetDeviceName 이름</span><span class="sxs-lookup"><span data-stu-id="89420-137">-TargetDeviceName</span></span>
<span data-ttu-id="89420-138">이 cmdlet이 볼륨 컨테이너 그룹에 대해 장애 조치 하는 StorSimple 장치의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-138">Specifies the name of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

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

### <span data-ttu-id="89420-139">-VolumecontainerGroups</span><span class="sxs-lookup"><span data-stu-id="89420-139">-VolumecontainerGroups</span></span>
<span data-ttu-id="89420-140">이 cmdlet이 다른 디바이스에 대해 장애 조치 하는 볼륨 컨테이너 그룹의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-140">Specifies the list of volume container groups that this cmdlet fails over to another device.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89420-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89420-141">CommonParameters</span></span>
<span data-ttu-id="89420-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89420-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89420-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89420-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89420-144">입력</span><span class="sxs-lookup"><span data-stu-id="89420-144">INPUTS</span></span>

### <span data-ttu-id="89420-145">목록\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="89420-145">List\<DataContainerGroup\></span></span>
<span data-ttu-id="89420-146">이 cmdlet에 볼륨 컨테이너 그룹의 목록을 파이프 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89420-146">You can pipe a list of volume container groups to this cmdlet.</span></span>

## <span data-ttu-id="89420-147">출력</span><span class="sxs-lookup"><span data-stu-id="89420-147">OUTPUTS</span></span>

### <span data-ttu-id="89420-148">이름</span><span class="sxs-lookup"><span data-stu-id="89420-148">String</span></span>

## <span data-ttu-id="89420-149">상속자</span><span class="sxs-lookup"><span data-stu-id="89420-149">NOTES</span></span>

## <span data-ttu-id="89420-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89420-150">RELATED LINKS</span></span>

[<span data-ttu-id="89420-151">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="89420-151">Get-AzureStorSimpleFailoverVolumeContainers</span></span>](./Get-AzureStorSimpleFailoverVolumeContainers.md)



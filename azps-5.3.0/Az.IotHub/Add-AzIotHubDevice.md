---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: e13cd1ba814bc5bea66a6a3d06506b9822dd38bd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495476"
---
# <span data-ttu-id="94f60-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="94f60-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="94f60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94f60-102">SYNOPSIS</span></span>
<span data-ttu-id="94f60-103">IoT Hub에서 디바이스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="94f60-104">구문</span><span class="sxs-lookup"><span data-stu-id="94f60-104">SYNTAX</span></span>

### <span data-ttu-id="94f60-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="94f60-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f60-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="94f60-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94f60-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="94f60-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94f60-108">설명</span><span class="sxs-lookup"><span data-stu-id="94f60-108">DESCRIPTION</span></span>
<span data-ttu-id="94f60-109">IoT Hub에서 다른 권한 부여 유형이 있는 디바이스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="94f60-110">예제</span><span class="sxs-lookup"><span data-stu-id="94f60-110">EXAMPLES</span></span>

### <span data-ttu-id="94f60-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="94f60-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="94f60-112">기본 권한 부여(공유 개인 키)를 사용하여 에지 사용 IoT 디바이스를 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="94f60-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="94f60-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="94f60-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="94f60-114">비활성화된 상태 및 이유가 있는 루트 CA 권한 부여를 사용하여 IoT 디바이스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="94f60-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="94f60-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="94f60-116">에지 사용 IoT 디바이스를 만들고 자식 디바이스를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="94f60-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="94f60-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="94f60-118">IoT 디바이스를 만들고 부모 디바이스를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="94f60-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94f60-119">PARAMETERS</span></span>

### <span data-ttu-id="94f60-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="94f60-120">-AuthMethod</span></span>
<span data-ttu-id="94f60-121">엔터티를 만들 권한 부여 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-121">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f60-122">-Children</span><span class="sxs-lookup"><span data-stu-id="94f60-122">-Children</span></span>
<span data-ttu-id="94f60-123">자식 디바이스 목록 추가(콤마로 구분)에는 에지가 아닌 디바이스만 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f60-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f60-124">-DefaultProfile</span></span>
<span data-ttu-id="94f60-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f60-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="94f60-126">-DeviceId</span></span>
<span data-ttu-id="94f60-127">대상 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-127">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f60-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="94f60-128">-EdgeEnabled</span></span>
<span data-ttu-id="94f60-129">에지 사용률을 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-129">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f60-130">-Force</span><span class="sxs-lookup"><span data-stu-id="94f60-130">-Force</span></span>
<span data-ttu-id="94f60-131">비에지 디바이스의 부모 디바이스를 덮어 덮어 습니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-131">Overwrites the non-edge device's parent device.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f60-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94f60-132">-InputObject</span></span>
<span data-ttu-id="94f60-133">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="94f60-133">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94f60-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="94f60-134">-IotHubName</span></span>
<span data-ttu-id="94f60-135">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="94f60-135">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f60-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="94f60-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="94f60-137">기본 키에 사용할 명시적 자체 서명된 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f60-138">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="94f60-138">-ParentDeviceId</span></span>
<span data-ttu-id="94f60-139">에지 디바이스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-139">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f60-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f60-140">-ResourceGroupName</span></span>
<span data-ttu-id="94f60-141">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="94f60-141">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f60-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94f60-142">-ResourceId</span></span>
<span data-ttu-id="94f60-143">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="94f60-143">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f60-144">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="94f60-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="94f60-145">보조 키에 사용할 명시적 자체 서명된 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f60-146">-Status</span><span class="sxs-lookup"><span data-stu-id="94f60-146">-Status</span></span>
<span data-ttu-id="94f60-147">생성 시 디바이스 상태를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-147">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f60-148">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="94f60-148">-StatusReason</span></span>
<span data-ttu-id="94f60-149">디바이스 상태에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-149">Description for device status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f60-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94f60-150">-Confirm</span></span>
<span data-ttu-id="94f60-151">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94f60-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f60-152">-WhatIf</span></span>
<span data-ttu-id="94f60-153">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="94f60-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94f60-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94f60-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f60-155">CommonParameters</span></span>
<span data-ttu-id="94f60-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="94f60-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f60-157">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="94f60-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f60-158">입력</span><span class="sxs-lookup"><span data-stu-id="94f60-158">INPUTS</span></span>

### <span data-ttu-id="94f60-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="94f60-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="94f60-160">System.String</span><span class="sxs-lookup"><span data-stu-id="94f60-160">System.String</span></span>

## <span data-ttu-id="94f60-161">출력</span><span class="sxs-lookup"><span data-stu-id="94f60-161">OUTPUTS</span></span>

### <span data-ttu-id="94f60-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSD</span><span class="sxs-lookup"><span data-stu-id="94f60-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="94f60-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="94f60-163">NOTES</span></span>

## <span data-ttu-id="94f60-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94f60-164">RELATED LINKS</span></span>

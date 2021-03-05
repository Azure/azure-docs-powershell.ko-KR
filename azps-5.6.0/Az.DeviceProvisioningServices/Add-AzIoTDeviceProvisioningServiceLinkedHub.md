---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 8b5a42110c99a4572b411d082879f4f2853bac0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983552"
---
# <span data-ttu-id="1eaef-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="1eaef-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="1eaef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1eaef-102">SYNOPSIS</span></span>
<span data-ttu-id="1eaef-103">IoT Hub를 Azure IoT Hub 디바이스 프로비전 서비스에 연결했습니다.</span><span class="sxs-lookup"><span data-stu-id="1eaef-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="1eaef-104">구문</span><span class="sxs-lookup"><span data-stu-id="1eaef-104">SYNTAX</span></span>

### <span data-ttu-id="1eaef-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1eaef-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eaef-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1eaef-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eaef-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1eaef-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1eaef-108">설명</span><span class="sxs-lookup"><span data-stu-id="1eaef-108">DESCRIPTION</span></span>
<span data-ttu-id="1eaef-109">Azure IoT Hub 디바이스 프로비전 서비스에 대한 소개는 https://docs.microsoft.com/azure/iot-dps/about-iot-dps 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1eaef-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="1eaef-110">예제</span><span class="sxs-lookup"><span data-stu-id="1eaef-110">EXAMPLES</span></span>

### <span data-ttu-id="1eaef-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1eaef-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="1eaef-112">IoT Hub를 Azure IoT Hub 디바이스 프로비전 서비스에 연결했습니다.</span><span class="sxs-lookup"><span data-stu-id="1eaef-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="1eaef-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="1eaef-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="1eaef-114">AllocationWeight 및 ApplyAllocationPolicy를 사용하여 Azure IoT Hub 디바이스 프로비전 서비스에 연결된 IoT Hub입니다.</span><span class="sxs-lookup"><span data-stu-id="1eaef-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="1eaef-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1eaef-115">PARAMETERS</span></span>

### <span data-ttu-id="1eaef-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="1eaef-116">-AllocationWeight</span></span>
<span data-ttu-id="1eaef-117">IoT Hub의 할당 가중치</span><span class="sxs-lookup"><span data-stu-id="1eaef-117">Allocation weight of the IoT Hub</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eaef-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="1eaef-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="1eaef-119">IoT Hub에 할당 정책을 적용할지 여부를 나타내는 부울</span><span class="sxs-lookup"><span data-stu-id="1eaef-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="1eaef-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eaef-120">-DefaultProfile</span></span>
<span data-ttu-id="1eaef-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1eaef-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1eaef-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="1eaef-122">-DpsObject</span></span>
<span data-ttu-id="1eaef-123">IoT 디바이스 프로비전 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="1eaef-123">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1eaef-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="1eaef-124">-IotHubConnectionString</span></span>
<span data-ttu-id="1eaef-125">Iot Hub 리소스의 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="1eaef-125">Connection String of the Iot Hub resource.</span></span>

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

### <span data-ttu-id="1eaef-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="1eaef-126">-IotHubLocation</span></span>
<span data-ttu-id="1eaef-127">Iot Hub의 위치</span><span class="sxs-lookup"><span data-stu-id="1eaef-127">Location of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eaef-128">-Name</span><span class="sxs-lookup"><span data-stu-id="1eaef-128">-Name</span></span>
<span data-ttu-id="1eaef-129">IoT 디바이스 프로비전 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="1eaef-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="1eaef-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eaef-130">-ResourceGroupName</span></span>
<span data-ttu-id="1eaef-131">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="1eaef-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1eaef-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1eaef-132">-ResourceId</span></span>
<span data-ttu-id="1eaef-133">IoT 디바이스 프로비전 서비스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="1eaef-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="1eaef-134">-확인</span><span class="sxs-lookup"><span data-stu-id="1eaef-134">-Confirm</span></span>
<span data-ttu-id="1eaef-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1eaef-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1eaef-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eaef-136">-WhatIf</span></span>
<span data-ttu-id="1eaef-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1eaef-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1eaef-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1eaef-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1eaef-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eaef-139">CommonParameters</span></span>
<span data-ttu-id="1eaef-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1eaef-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eaef-141">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1eaef-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eaef-142">입력</span><span class="sxs-lookup"><span data-stu-id="1eaef-142">INPUTS</span></span>

### <span data-ttu-id="1eaef-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="1eaef-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="1eaef-144">System.String</span><span class="sxs-lookup"><span data-stu-id="1eaef-144">System.String</span></span>

## <span data-ttu-id="1eaef-145">출력</span><span class="sxs-lookup"><span data-stu-id="1eaef-145">OUTPUTS</span></span>

### <span data-ttu-id="1eaef-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="1eaef-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="1eaef-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="1eaef-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="1eaef-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1eaef-148">NOTES</span></span>

## <span data-ttu-id="1eaef-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1eaef-149">RELATED LINKS</span></span>

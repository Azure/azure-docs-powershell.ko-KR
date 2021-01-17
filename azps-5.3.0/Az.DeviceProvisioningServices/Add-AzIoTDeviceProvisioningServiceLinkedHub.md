---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 30bcf61f309a400270e9cca378fce6d1149cf66a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387052"
---
# <span data-ttu-id="12dd3-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="12dd3-101">Add-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="12dd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12dd3-102">SYNOPSIS</span></span>
<span data-ttu-id="12dd3-103">Azure IoT Hub 디바이스 프로비전 서비스에 연결된 IoT Hub</span><span class="sxs-lookup"><span data-stu-id="12dd3-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="12dd3-104">구문</span><span class="sxs-lookup"><span data-stu-id="12dd3-104">SYNTAX</span></span>

### <span data-ttu-id="12dd3-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="12dd3-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12dd3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="12dd3-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12dd3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="12dd3-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12dd3-108">설명</span><span class="sxs-lookup"><span data-stu-id="12dd3-108">DESCRIPTION</span></span>
<span data-ttu-id="12dd3-109">Azure IoT Hub Device Provisioning Service에 대한 소개는 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="12dd3-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="12dd3-110">예제</span><span class="sxs-lookup"><span data-stu-id="12dd3-110">EXAMPLES</span></span>

### <span data-ttu-id="12dd3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="12dd3-111">Example 1</span></span>
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

<span data-ttu-id="12dd3-112">Azure IoT Hub 디바이스 프로비전 서비스에 연결된 IoT Hub</span><span class="sxs-lookup"><span data-stu-id="12dd3-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="12dd3-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="12dd3-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="12dd3-114">AllocationWeight 및 ApplyAllocationPolicy를 사용하여 Azure IoT Hub 디바이스 프로비전 서비스에 연결된 IoT Hub</span><span class="sxs-lookup"><span data-stu-id="12dd3-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="12dd3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12dd3-115">PARAMETERS</span></span>

### <span data-ttu-id="12dd3-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="12dd3-116">-AllocationWeight</span></span>
<span data-ttu-id="12dd3-117">IoT Hub의 할당 가중치</span><span class="sxs-lookup"><span data-stu-id="12dd3-117">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="12dd3-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="12dd3-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="12dd3-119">IoT Hub에 할당 정책을 적용할지 여부를 나타내는 부울</span><span class="sxs-lookup"><span data-stu-id="12dd3-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="12dd3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12dd3-120">-DefaultProfile</span></span>
<span data-ttu-id="12dd3-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="12dd3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12dd3-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="12dd3-122">-DpsObject</span></span>
<span data-ttu-id="12dd3-123">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="12dd3-123">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="12dd3-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="12dd3-124">-IotHubConnectionString</span></span>
<span data-ttu-id="12dd3-125">Iot Hub 리소스의 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="12dd3-125">Connection String of the Iot Hub resource.</span></span>

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

### <span data-ttu-id="12dd3-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="12dd3-126">-IotHubLocation</span></span>
<span data-ttu-id="12dd3-127">Iot Hub의 위치</span><span class="sxs-lookup"><span data-stu-id="12dd3-127">Location of the Iot Hub</span></span>

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

### <span data-ttu-id="12dd3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="12dd3-128">-Name</span></span>
<span data-ttu-id="12dd3-129">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="12dd3-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="12dd3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12dd3-130">-ResourceGroupName</span></span>
<span data-ttu-id="12dd3-131">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="12dd3-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="12dd3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12dd3-132">-ResourceId</span></span>
<span data-ttu-id="12dd3-133">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="12dd3-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="12dd3-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12dd3-134">-Confirm</span></span>
<span data-ttu-id="12dd3-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="12dd3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12dd3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12dd3-136">-WhatIf</span></span>
<span data-ttu-id="12dd3-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="12dd3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12dd3-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="12dd3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12dd3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12dd3-139">CommonParameters</span></span>
<span data-ttu-id="12dd3-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="12dd3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12dd3-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="12dd3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12dd3-142">입력</span><span class="sxs-lookup"><span data-stu-id="12dd3-142">INPUTS</span></span>

### <span data-ttu-id="12dd3-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="12dd3-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="12dd3-144">System.String</span><span class="sxs-lookup"><span data-stu-id="12dd3-144">System.String</span></span>

## <span data-ttu-id="12dd3-145">출력</span><span class="sxs-lookup"><span data-stu-id="12dd3-145">OUTPUTS</span></span>

### <span data-ttu-id="12dd3-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="12dd3-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="12dd3-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="12dd3-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="12dd3-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="12dd3-148">NOTES</span></span>

## <span data-ttu-id="12dd3-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12dd3-149">RELATED LINKS</span></span>

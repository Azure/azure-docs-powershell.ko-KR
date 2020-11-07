---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: ca32f2d0436ea16d8897f279239ce4de079d1550
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702949"
---
# <span data-ttu-id="a222c-101">Add-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="a222c-101">Add-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="a222c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a222c-102">SYNOPSIS</span></span>
<span data-ttu-id="a222c-103">Azure IoT Hub device 프로비저닝 서비스에 연결 된 IoT hub.</span><span class="sxs-lookup"><span data-stu-id="a222c-103">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a222c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a222c-104">SYNTAX</span></span>

### <span data-ttu-id="a222c-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a222c-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a222c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a222c-106">InputObjectSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-IotHubConnectionString] <String> [-IotHubLocation] <String> [-AllocationWeight <Int32>]
 [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a222c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a222c-107">ResourceIdSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-IotHubConnectionString] <String>
 [-IotHubLocation] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a222c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a222c-108">DESCRIPTION</span></span>
<span data-ttu-id="a222c-109">Azure IoT Hub Device 프로비저닝 서비스에 대 한 소개는를 참조 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 하세요.</span><span class="sxs-lookup"><span data-stu-id="a222c-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="a222c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a222c-110">EXAMPLES</span></span>

### <span data-ttu-id="a222c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a222c-111">Example 1</span></span>
```
PS C:\> Add-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 
ApplyAllocationPolicy : 
Location              : eastus
```

<span data-ttu-id="a222c-112">Azure IoT Hub device 프로비저닝 서비스에 연결 된 IoT hub.</span><span class="sxs-lookup"><span data-stu-id="a222c-112">Linked IoT hub to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="a222c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="a222c-113">Example 2</span></span>
```
PS C:\> Add-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -IotHubConnectionString $hubConnectionString -IotHubLocation "eastus" -AllocationWeight 10 -ApplyAllocationPolicy $false

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2                   true
myiothub2.azure-devices.net     westus2     10                  false
```

<span data-ttu-id="a222c-114">AllocationWeight 및 ApplyAllocationPolicy를 사용 하 여 Azure IoT Hub 디바이스 프로비저닝 서비스에 연결 된 IoT hub</span><span class="sxs-lookup"><span data-stu-id="a222c-114">Linked IoT hub to an Azure IoT Hub device provisioning service with AllocationWeight and ApplyAllocationPolicy.</span></span>

## <span data-ttu-id="a222c-115">변수</span><span class="sxs-lookup"><span data-stu-id="a222c-115">PARAMETERS</span></span>

### <span data-ttu-id="a222c-116">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="a222c-116">-AllocationWeight</span></span>
<span data-ttu-id="a222c-117">IoT Hub의 할당 중량</span><span class="sxs-lookup"><span data-stu-id="a222c-117">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="a222c-118">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="a222c-118">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="a222c-119">IoT Hub에 할당 정책을 적용할지 여부를 나타내는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="a222c-119">A boolean indicating whether to apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="a222c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a222c-120">-DefaultProfile</span></span>
<span data-ttu-id="a222c-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a222c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a222c-122">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="a222c-122">-DpsObject</span></span>
<span data-ttu-id="a222c-123">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="a222c-123">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="a222c-124">-IotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="a222c-124">-IotHubConnectionString</span></span>
<span data-ttu-id="a222c-125">Iot Hub 리소스의 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="a222c-125">Connection String of the Iot Hub resource.</span></span>

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

### <span data-ttu-id="a222c-126">-IotHubLocation</span><span class="sxs-lookup"><span data-stu-id="a222c-126">-IotHubLocation</span></span>
<span data-ttu-id="a222c-127">Iot Hub의 위치</span><span class="sxs-lookup"><span data-stu-id="a222c-127">Location of the Iot Hub</span></span>

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

### <span data-ttu-id="a222c-128">-이름</span><span class="sxs-lookup"><span data-stu-id="a222c-128">-Name</span></span>
<span data-ttu-id="a222c-129">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="a222c-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a222c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a222c-130">-ResourceGroupName</span></span>
<span data-ttu-id="a222c-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a222c-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a222c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a222c-132">-ResourceId</span></span>
<span data-ttu-id="a222c-133">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="a222c-133">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="a222c-134">-확인</span><span class="sxs-lookup"><span data-stu-id="a222c-134">-Confirm</span></span>
<span data-ttu-id="a222c-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a222c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a222c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a222c-136">-WhatIf</span></span>
<span data-ttu-id="a222c-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a222c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a222c-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a222c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a222c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a222c-139">CommonParameters</span></span>
<span data-ttu-id="a222c-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a222c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a222c-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a222c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a222c-142">입력</span><span class="sxs-lookup"><span data-stu-id="a222c-142">INPUTS</span></span>

### <span data-ttu-id="a222c-143">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="a222c-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="a222c-144">매개 변수: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a222c-144">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="a222c-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a222c-145">System.String</span></span>

## <span data-ttu-id="a222c-146">출력</span><span class="sxs-lookup"><span data-stu-id="a222c-146">OUTPUTS</span></span>

### <span data-ttu-id="a222c-147">DeviceProvisioningServices. PSIotHubDefinitionDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="a222c-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="a222c-148">DeviceProvisioningServices. PSIotHubDefinitions/. \*</span><span class="sxs-lookup"><span data-stu-id="a222c-148">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="a222c-149">상속자</span><span class="sxs-lookup"><span data-stu-id="a222c-149">NOTES</span></span>

## <span data-ttu-id="a222c-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a222c-150">RELATED LINKS</span></span>

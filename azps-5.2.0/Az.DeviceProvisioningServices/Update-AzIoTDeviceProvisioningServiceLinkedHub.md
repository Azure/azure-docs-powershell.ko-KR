---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: cc8d2ec0602213bdbfd50ac89e5199952cea424c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347049"
---
# <span data-ttu-id="bd25f-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="bd25f-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="bd25f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd25f-102">SYNOPSIS</span></span>
<span data-ttu-id="bd25f-103">Azure IoT Hub 디바이스 프로비전 서비스에서 연결된 IoT Hub를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bd25f-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="bd25f-104">구문</span><span class="sxs-lookup"><span data-stu-id="bd25f-104">SYNTAX</span></span>

### <span data-ttu-id="bd25f-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bd25f-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd25f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bd25f-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd25f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bd25f-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd25f-108">설명</span><span class="sxs-lookup"><span data-stu-id="bd25f-108">DESCRIPTION</span></span>
<span data-ttu-id="bd25f-109">Azure IoT Hub Device Provisioning Service에 대한 소개는 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bd25f-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="bd25f-110">예제</span><span class="sxs-lookup"><span data-stu-id="bd25f-110">EXAMPLES</span></span>

### <span data-ttu-id="bd25f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="bd25f-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -AllocationWeight 10 -ApplyAllocationPolicy $true

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 10
ApplyAllocationPolicy : True
Location              : eastus
```

<span data-ttu-id="bd25f-112">Azure IoT Hub 디바이스 myiothub.azure-devices.net 서비스에서 연결된 IoT Hub "myiothub.azure-devices.net"를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bd25f-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="bd25f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd25f-113">PARAMETERS</span></span>

### <span data-ttu-id="bd25f-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="bd25f-114">-AllocationWeight</span></span>
<span data-ttu-id="bd25f-115">IoT Hub의 할당 가중치</span><span class="sxs-lookup"><span data-stu-id="bd25f-115">Allocation weight of the IoT Hub</span></span>

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

### <span data-ttu-id="bd25f-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="bd25f-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="bd25f-117">IoT Hub에 할당 정책 적용</span><span class="sxs-lookup"><span data-stu-id="bd25f-117">Apply allocation policy to the IoT Hub</span></span>

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

### <span data-ttu-id="bd25f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd25f-118">-DefaultProfile</span></span>
<span data-ttu-id="bd25f-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd25f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd25f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd25f-120">-InputObject</span></span>
<span data-ttu-id="bd25f-121">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="bd25f-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd25f-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="bd25f-122">-LinkedHubName</span></span>
<span data-ttu-id="bd25f-123">연결된 IoT Hub의 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="bd25f-123">Host name of linked IoT Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd25f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="bd25f-124">-Name</span></span>
<span data-ttu-id="bd25f-125">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="bd25f-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="bd25f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd25f-126">-ResourceGroupName</span></span>
<span data-ttu-id="bd25f-127">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="bd25f-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bd25f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd25f-128">-ResourceId</span></span>
<span data-ttu-id="bd25f-129">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="bd25f-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="bd25f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd25f-130">-Confirm</span></span>
<span data-ttu-id="bd25f-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd25f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd25f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd25f-132">-WhatIf</span></span>
<span data-ttu-id="bd25f-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bd25f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd25f-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd25f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd25f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd25f-135">CommonParameters</span></span>
<span data-ttu-id="bd25f-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bd25f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd25f-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bd25f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd25f-138">입력</span><span class="sxs-lookup"><span data-stu-id="bd25f-138">INPUTS</span></span>

### <span data-ttu-id="bd25f-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="bd25f-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="bd25f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="bd25f-140">System.String</span></span>

## <span data-ttu-id="bd25f-141">출력</span><span class="sxs-lookup"><span data-stu-id="bd25f-141">OUTPUTS</span></span>

### <span data-ttu-id="bd25f-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="bd25f-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="bd25f-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bd25f-143">NOTES</span></span>

## <span data-ttu-id="bd25f-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd25f-144">RELATED LINKS</span></span>

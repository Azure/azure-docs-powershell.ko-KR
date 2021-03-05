---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 7e1181ba837f0d2447a46f051765b0430399b123
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985068"
---
# <span data-ttu-id="0a89d-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="0a89d-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="0a89d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a89d-102">SYNOPSIS</span></span>
<span data-ttu-id="0a89d-103">Azure IoT Hub 디바이스 프로비전 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0a89d-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="0a89d-104">구문</span><span class="sxs-lookup"><span data-stu-id="0a89d-104">SYNTAX</span></span>

### <span data-ttu-id="0a89d-105">ResourceUpdateSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0a89d-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a89d-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0a89d-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a89d-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0a89d-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a89d-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0a89d-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a89d-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0a89d-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a89d-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="0a89d-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a89d-111">설명</span><span class="sxs-lookup"><span data-stu-id="0a89d-111">DESCRIPTION</span></span>
<span data-ttu-id="0a89d-112">Azure IoT Hub 디바이스 프로비전 서비스에 대한 소개는 https://docs.microsoft.com/azure/iot-dps/about-iot-dps 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0a89d-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="0a89d-113">예제</span><span class="sxs-lookup"><span data-stu-id="0a89d-113">EXAMPLES</span></span>

### <span data-ttu-id="0a89d-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="0a89d-114">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -AllocationPolicy "GeoLatency"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : GeoLatency
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="0a89d-115">Azure IoT Hub 디바이스 프로비전 서비스 "myiotdps"의 "GeoLatency"로 할당 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0a89d-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="0a89d-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="0a89d-116">Example 2</span></span>
```
PS C:\> $tag = @{}
PS C:\> $tag.Add("key1","Value1")
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag $tag

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="0a89d-117">Azure IoT Hub 디바이스 프로비전 서비스 "myiotdps"에 태그를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0a89d-117">Add tags to an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="0a89d-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="0a89d-118">Example 3</span></span>
```
PS C:\> $tag = @{}
PS C:\> $tag.Add("key1","Value1")
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzIoTDps -Tag $tag -Reset

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAS1dY=
```

<span data-ttu-id="0a89d-119">태그를 삭제하고 파이프라인을 사용하여 Azure IoT Hub 디바이스 프로비전 서비스 "myiotdps"에 새 태그를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="0a89d-119">Delete Tag and add new tags to an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="0a89d-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0a89d-120">PARAMETERS</span></span>

### <span data-ttu-id="0a89d-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="0a89d-121">-AllocationPolicy</span></span>
<span data-ttu-id="0a89d-122">IoT 디바이스 프로비전 서비스 할당 정책</span><span class="sxs-lookup"><span data-stu-id="0a89d-122">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectCreateUpdateSet, ResourceIdCreateUpdateSet, ResourceCreateUpdateSet
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a89d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a89d-123">-DefaultProfile</span></span>
<span data-ttu-id="0a89d-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a89d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a89d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a89d-125">-InputObject</span></span>
<span data-ttu-id="0a89d-126">IoT 디바이스 프로비전 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="0a89d-126">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectUpdateSet, InputObjectCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a89d-127">-Name</span><span class="sxs-lookup"><span data-stu-id="0a89d-127">-Name</span></span>
<span data-ttu-id="0a89d-128">IoT 디바이스 프로비전 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="0a89d-128">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a89d-129">-Reset</span><span class="sxs-lookup"><span data-stu-id="0a89d-129">-Reset</span></span>
<span data-ttu-id="0a89d-130">IoT 디바이스 프로비전 서비스 태그 재설정</span><span class="sxs-lookup"><span data-stu-id="0a89d-130">Reset IoT Device Provisioning Service Tags</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a89d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a89d-131">-ResourceGroupName</span></span>
<span data-ttu-id="0a89d-132">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="0a89d-132">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a89d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a89d-133">-ResourceId</span></span>
<span data-ttu-id="0a89d-134">IoT 디바이스 프로비전 서비스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="0a89d-134">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdUpdateSet, ResourceIdCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a89d-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a89d-135">-Tag</span></span>
<span data-ttu-id="0a89d-136">IoT Device Provisioning Service Tag 컬렉션</span><span class="sxs-lookup"><span data-stu-id="0a89d-136">IoT Device Provisioning Service Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a89d-137">-확인</span><span class="sxs-lookup"><span data-stu-id="0a89d-137">-Confirm</span></span>
<span data-ttu-id="0a89d-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a89d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a89d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a89d-139">-WhatIf</span></span>
<span data-ttu-id="0a89d-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0a89d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a89d-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a89d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a89d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a89d-142">CommonParameters</span></span>
<span data-ttu-id="0a89d-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0a89d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a89d-144">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0a89d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a89d-145">입력</span><span class="sxs-lookup"><span data-stu-id="0a89d-145">INPUTS</span></span>

### <span data-ttu-id="0a89d-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="0a89d-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="0a89d-147">System.String</span><span class="sxs-lookup"><span data-stu-id="0a89d-147">System.String</span></span>

## <span data-ttu-id="0a89d-148">출력</span><span class="sxs-lookup"><span data-stu-id="0a89d-148">OUTPUTS</span></span>

### <span data-ttu-id="0a89d-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="0a89d-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="0a89d-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0a89d-150">NOTES</span></span>

## <span data-ttu-id="0a89d-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a89d-151">RELATED LINKS</span></span>

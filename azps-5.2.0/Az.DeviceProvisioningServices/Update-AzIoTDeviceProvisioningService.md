---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: f533bd07d0c7b123f1d109e7abd933736093cd79
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347121"
---
# <span data-ttu-id="9e46e-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="9e46e-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="9e46e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e46e-102">SYNOPSIS</span></span>
<span data-ttu-id="9e46e-103">Azure IoT Hub 디바이스 프로비전 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9e46e-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="9e46e-104">구문</span><span class="sxs-lookup"><span data-stu-id="9e46e-104">SYNTAX</span></span>

### <span data-ttu-id="9e46e-105">ResourceUpdateSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9e46e-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e46e-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="9e46e-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e46e-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="9e46e-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e46e-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="9e46e-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e46e-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="9e46e-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e46e-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="9e46e-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e46e-111">설명</span><span class="sxs-lookup"><span data-stu-id="9e46e-111">DESCRIPTION</span></span>
<span data-ttu-id="9e46e-112">Azure IoT Hub Device Provisioning Service에 대한 소개는 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9e46e-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="9e46e-113">예제</span><span class="sxs-lookup"><span data-stu-id="9e46e-113">EXAMPLES</span></span>

### <span data-ttu-id="9e46e-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="9e46e-114">Example 1</span></span>
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

<span data-ttu-id="9e46e-115">Azure IoT Hub 디바이스 프로비전 서비스 "myiotdps"의 "GeoLatency"로 할당 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9e46e-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="9e46e-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="9e46e-116">Example 2</span></span>
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

<span data-ttu-id="9e46e-117">Azure IoT Hub 디바이스 프로비전 서비스 "myiotdps"에 태그를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9e46e-117">Add tags to an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="9e46e-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="9e46e-118">Example 3</span></span>
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

<span data-ttu-id="9e46e-119">파이프라인을 사용하여 태그를 삭제하고 Azure IoT Hub 디바이스 프로비전 서비스 "myiotdps"에 새 태그를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9e46e-119">Delete Tag and add new tags to an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="9e46e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e46e-120">PARAMETERS</span></span>

### <span data-ttu-id="9e46e-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="9e46e-121">-AllocationPolicy</span></span>
<span data-ttu-id="9e46e-122">IoT Device Provisioning Service 할당 정책</span><span class="sxs-lookup"><span data-stu-id="9e46e-122">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="9e46e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e46e-123">-DefaultProfile</span></span>
<span data-ttu-id="9e46e-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e46e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e46e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e46e-125">-InputObject</span></span>
<span data-ttu-id="9e46e-126">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="9e46e-126">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="9e46e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="9e46e-127">-Name</span></span>
<span data-ttu-id="9e46e-128">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="9e46e-128">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9e46e-129">-Reset</span><span class="sxs-lookup"><span data-stu-id="9e46e-129">-Reset</span></span>
<span data-ttu-id="9e46e-130">IoT Device Provisioning Service 태그 다시 설정</span><span class="sxs-lookup"><span data-stu-id="9e46e-130">Reset IoT Device Provisioning Service Tags</span></span>

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

### <span data-ttu-id="9e46e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e46e-131">-ResourceGroupName</span></span>
<span data-ttu-id="9e46e-132">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="9e46e-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9e46e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e46e-133">-ResourceId</span></span>
<span data-ttu-id="9e46e-134">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9e46e-134">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="9e46e-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e46e-135">-Tag</span></span>
<span data-ttu-id="9e46e-136">IoT Device Provisioning Service 태그 컬렉션</span><span class="sxs-lookup"><span data-stu-id="9e46e-136">IoT Device Provisioning Service Tag collection</span></span>

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

### <span data-ttu-id="9e46e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e46e-137">-Confirm</span></span>
<span data-ttu-id="9e46e-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e46e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e46e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e46e-139">-WhatIf</span></span>
<span data-ttu-id="9e46e-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9e46e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e46e-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e46e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e46e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e46e-142">CommonParameters</span></span>
<span data-ttu-id="9e46e-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9e46e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e46e-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9e46e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e46e-145">입력</span><span class="sxs-lookup"><span data-stu-id="9e46e-145">INPUTS</span></span>

### <span data-ttu-id="9e46e-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="9e46e-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="9e46e-147">System.String</span><span class="sxs-lookup"><span data-stu-id="9e46e-147">System.String</span></span>

## <span data-ttu-id="9e46e-148">출력</span><span class="sxs-lookup"><span data-stu-id="9e46e-148">OUTPUTS</span></span>

### <span data-ttu-id="9e46e-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="9e46e-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="9e46e-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9e46e-150">NOTES</span></span>

## <span data-ttu-id="9e46e-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e46e-151">RELATED LINKS</span></span>

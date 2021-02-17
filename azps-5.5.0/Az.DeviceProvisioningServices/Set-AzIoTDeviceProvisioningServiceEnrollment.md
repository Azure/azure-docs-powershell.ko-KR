---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 47c5c5119e41f3feeaccda66871d902e631c9ac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194489"
---
# <span data-ttu-id="5b54e-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="5b54e-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="5b54e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b54e-102">SYNOPSIS</span></span>
<span data-ttu-id="5b54e-103">디바이스 등록 레코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="5b54e-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b54e-104">SYNTAX</span></span>

### <span data-ttu-id="5b54e-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5b54e-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b54e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5b54e-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b54e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5b54e-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b54e-108">설명</span><span class="sxs-lookup"><span data-stu-id="5b54e-108">DESCRIPTION</span></span>
<span data-ttu-id="5b54e-109">Azure IoT Hub Device Provisioning Service에서 디바이스 등록을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="5b54e-110">예제</span><span class="sxs-lookup"><span data-stu-id="5b54e-110">EXAMPLES</span></span>

### <span data-ttu-id="5b54e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5b54e-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="5b54e-112">등록 레코드에 대한 할당 정책 및 허브를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="5b54e-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="5b54e-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="5b54e-114">등록의 초기 쌍 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-114">Update an enrollment's initial twin state.</span></span>

## <span data-ttu-id="5b54e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b54e-115">PARAMETERS</span></span>

### <span data-ttu-id="5b54e-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="5b54e-116">-AllocationPolicy</span></span>
<span data-ttu-id="5b54e-117">허브에 할당된 디바이스에 대한 할당 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-117">Type of allocation for device assigned to the Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAllocationPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b54e-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5b54e-118">-ApiVersion</span></span>
<span data-ttu-id="5b54e-119">사용자 지정 할당 요청의 프로비전 서비스의 API 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="5b54e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b54e-120">-DefaultProfile</span></span>
<span data-ttu-id="5b54e-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b54e-122">-Desired</span><span class="sxs-lookup"><span data-stu-id="5b54e-122">-Desired</span></span>
<span data-ttu-id="5b54e-123">초기 쌍 desired 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-123">Initial twin desired properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b54e-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="5b54e-124">-DeviceId</span></span>
<span data-ttu-id="5b54e-125">IoT Hub 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-125">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="5b54e-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="5b54e-126">-DpsName</span></span>
<span data-ttu-id="5b54e-127">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="5b54e-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5b54e-128">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="5b54e-128">-DpsObject</span></span>
<span data-ttu-id="5b54e-129">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="5b54e-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5b54e-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="5b54e-130">-EdgeEnabled</span></span>
<span data-ttu-id="5b54e-131">에지 사용률을 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-131">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b54e-132">-IotHub</span><span class="sxs-lookup"><span data-stu-id="5b54e-132">-IotHub</span></span>
<span data-ttu-id="5b54e-133">대상 IoT Hub의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="5b54e-134">여러 IoT Hub에 공백으로 구분된 목록을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="5b54e-134">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="5b54e-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="5b54e-135">-IotHubHostName</span></span>
<span data-ttu-id="5b54e-136">대상 IoT Hub의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="5b54e-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="5b54e-137">-ProvisioningStatus</span></span>
<span data-ttu-id="5b54e-138">등록 항목을 설정하거나 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-138">Enable or disable enrollment entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b54e-139">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="5b54e-139">-RegistrationId</span></span>
<span data-ttu-id="5b54e-140">개별 등록 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-140">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="5b54e-141">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="5b54e-141">-ReprovisionPolicy</span></span>
<span data-ttu-id="5b54e-142">다른 Iot Hub에 다시 프로비전할 때 처리할 디바이스 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-142">Device data to be handled on re-provision to different Iot Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSReprovisionType
Parameter Sets: (All)
Aliases:
Accepted values: reprovisionandmigratedata, reprovisionandresetdata, never

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b54e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b54e-143">-ResourceGroupName</span></span>
<span data-ttu-id="5b54e-144">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="5b54e-144">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5b54e-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b54e-145">-ResourceId</span></span>
<span data-ttu-id="5b54e-146">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="5b54e-146">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5b54e-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="5b54e-147">-Tag</span></span>
<span data-ttu-id="5b54e-148">초기 쌍 태그.</span><span class="sxs-lookup"><span data-stu-id="5b54e-148">Initial twin tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b54e-149">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="5b54e-149">-WebhookUrl</span></span>
<span data-ttu-id="5b54e-150">사용자 지정 할당 요청에 사용되는 웹후크 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-150">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="5b54e-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b54e-151">-Confirm</span></span>
<span data-ttu-id="5b54e-152">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b54e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b54e-153">-WhatIf</span></span>
<span data-ttu-id="5b54e-154">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5b54e-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b54e-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b54e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b54e-156">CommonParameters</span></span>
<span data-ttu-id="5b54e-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b54e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b54e-158">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5b54e-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b54e-159">입력</span><span class="sxs-lookup"><span data-stu-id="5b54e-159">INPUTS</span></span>

### <span data-ttu-id="5b54e-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="5b54e-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="5b54e-161">System.String</span><span class="sxs-lookup"><span data-stu-id="5b54e-161">System.String</span></span>

## <span data-ttu-id="5b54e-162">출력</span><span class="sxs-lookup"><span data-stu-id="5b54e-162">OUTPUTS</span></span>

### <span data-ttu-id="5b54e-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="5b54e-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="5b54e-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b54e-164">NOTES</span></span>

## <span data-ttu-id="5b54e-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b54e-165">RELATED LINKS</span></span>

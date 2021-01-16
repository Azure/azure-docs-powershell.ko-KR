---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 3982279b8698a84f23bc83aeccd25083d98363f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347114"
---
# <span data-ttu-id="4100b-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="4100b-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="4100b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4100b-102">SYNOPSIS</span></span>
<span data-ttu-id="4100b-103">디바이스 등록 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="4100b-104">구문</span><span class="sxs-lookup"><span data-stu-id="4100b-104">SYNTAX</span></span>

### <span data-ttu-id="4100b-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4100b-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4100b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4100b-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4100b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4100b-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4100b-108">설명</span><span class="sxs-lookup"><span data-stu-id="4100b-108">DESCRIPTION</span></span>
<span data-ttu-id="4100b-109">Azure IoT Hub Device Provisioning Service에서 등록 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="4100b-110">예제</span><span class="sxs-lookup"><span data-stu-id="4100b-110">EXAMPLES</span></span>

### <span data-ttu-id="4100b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4100b-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="4100b-112">등록 그룹에 대한 할당 정책 및 허브를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="4100b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="4100b-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="4100b-114">등록 그룹의 초기 쌍 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-114">Update an enrollment group's initial twin state.</span></span>

## <span data-ttu-id="4100b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4100b-115">PARAMETERS</span></span>

### <span data-ttu-id="4100b-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="4100b-116">-AllocationPolicy</span></span>
<span data-ttu-id="4100b-117">허브에 할당된 디바이스에 대한 할당 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="4100b-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4100b-118">-ApiVersion</span></span>
<span data-ttu-id="4100b-119">사용자 지정 할당 요청의 프로비전 서비스의 API 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="4100b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4100b-120">-DefaultProfile</span></span>
<span data-ttu-id="4100b-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4100b-122">-Desired</span><span class="sxs-lookup"><span data-stu-id="4100b-122">-Desired</span></span>
<span data-ttu-id="4100b-123">초기 쌍 desired 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="4100b-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="4100b-124">-DpsName</span></span>
<span data-ttu-id="4100b-125">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="4100b-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4100b-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="4100b-126">-DpsObject</span></span>
<span data-ttu-id="4100b-127">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="4100b-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="4100b-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="4100b-128">-EdgeEnabled</span></span>
<span data-ttu-id="4100b-129">에지 사용률을 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="4100b-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="4100b-130">-IotHub</span></span>
<span data-ttu-id="4100b-131">대상 IoT Hub의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="4100b-132">여러 IoT Hub에 공백으로 구분된 목록을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="4100b-132">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="4100b-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="4100b-133">-IotHubHostName</span></span>
<span data-ttu-id="4100b-134">대상 IoT Hub의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="4100b-135">-Name</span><span class="sxs-lookup"><span data-stu-id="4100b-135">-Name</span></span>
<span data-ttu-id="4100b-136">등록 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-136">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="4100b-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="4100b-137">-ProvisioningStatus</span></span>
<span data-ttu-id="4100b-138">등록 항목을 설정하거나 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="4100b-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="4100b-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="4100b-140">다른 Iot Hub에 다시 프로비전할 때 처리할 디바이스 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="4100b-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4100b-141">-ResourceGroupName</span></span>
<span data-ttu-id="4100b-142">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="4100b-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4100b-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4100b-143">-ResourceId</span></span>
<span data-ttu-id="4100b-144">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="4100b-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4100b-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="4100b-145">-Tag</span></span>
<span data-ttu-id="4100b-146">초기 쌍 태그.</span><span class="sxs-lookup"><span data-stu-id="4100b-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="4100b-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="4100b-147">-WebhookUrl</span></span>
<span data-ttu-id="4100b-148">사용자 지정 할당 요청에 사용되는 웹후크 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="4100b-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4100b-149">-Confirm</span></span>
<span data-ttu-id="4100b-150">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4100b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4100b-151">-WhatIf</span></span>
<span data-ttu-id="4100b-152">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4100b-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4100b-153">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4100b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4100b-154">CommonParameters</span></span>
<span data-ttu-id="4100b-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4100b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4100b-156">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4100b-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4100b-157">입력</span><span class="sxs-lookup"><span data-stu-id="4100b-157">INPUTS</span></span>

### <span data-ttu-id="4100b-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="4100b-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="4100b-159">System.String</span><span class="sxs-lookup"><span data-stu-id="4100b-159">System.String</span></span>

## <span data-ttu-id="4100b-160">출력</span><span class="sxs-lookup"><span data-stu-id="4100b-160">OUTPUTS</span></span>

### <span data-ttu-id="4100b-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="4100b-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="4100b-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4100b-162">NOTES</span></span>

## <span data-ttu-id="4100b-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4100b-163">RELATED LINKS</span></span>

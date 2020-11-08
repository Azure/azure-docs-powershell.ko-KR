---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8a81df2081420f8d218e094ff43f22e8dd9cc5c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215492"
---
# <span data-ttu-id="6d608-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="6d608-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="6d608-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d608-102">SYNOPSIS</span></span>
<span data-ttu-id="6d608-103">장치 등록 레코드를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="6d608-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d608-104">SYNTAX</span></span>

### <span data-ttu-id="6d608-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6d608-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d608-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6d608-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d608-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6d608-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d608-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6d608-108">DESCRIPTION</span></span>
<span data-ttu-id="6d608-109">Azure IoT Hub 디바이스 프로비저닝 서비스에서 디바이스 등록을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="6d608-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6d608-110">EXAMPLES</span></span>

### <span data-ttu-id="6d608-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6d608-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="6d608-112">등록 레코드에 대 한 할당 정책 및 허브를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-112">Update allocation policy and hubs for an enrollment record.</span></span>

## <span data-ttu-id="6d608-113">변수</span><span class="sxs-lookup"><span data-stu-id="6d608-113">PARAMETERS</span></span>

### <span data-ttu-id="6d608-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="6d608-114">-AllocationPolicy</span></span>
<span data-ttu-id="6d608-115">허브에 할당 된 장치에 대 한 할당 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-115">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="6d608-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6d608-116">-ApiVersion</span></span>
<span data-ttu-id="6d608-117">사용자 지정 할당 요청에서 제공 하는 프로비저닝 서비스의 API 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="6d608-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d608-118">-DefaultProfile</span></span>
<span data-ttu-id="6d608-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d608-120">-원하는</span><span class="sxs-lookup"><span data-stu-id="6d608-120">-Desired</span></span>
<span data-ttu-id="6d608-121">초기 트윈 필요 속성.</span><span class="sxs-lookup"><span data-stu-id="6d608-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="6d608-122">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6d608-122">-DeviceId</span></span>
<span data-ttu-id="6d608-123">IoT Hub 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-123">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="6d608-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="6d608-124">-DpsName</span></span>
<span data-ttu-id="6d608-125">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="6d608-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="6d608-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="6d608-126">-DpsObject</span></span>
<span data-ttu-id="6d608-127">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="6d608-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="6d608-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="6d608-128">-EdgeEnabled</span></span>
<span data-ttu-id="6d608-129">가장자리를 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="6d608-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="6d608-130">-IotHub</span></span>
<span data-ttu-id="6d608-131">대상 IoT Hub의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="6d608-132">여러 IoT Hub에 공백으로 구분 된 목록을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-132">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="6d608-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="6d608-133">-IotHubHostName</span></span>
<span data-ttu-id="6d608-134">대상 IoT Hub의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="6d608-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="6d608-135">-ProvisioningStatus</span></span>
<span data-ttu-id="6d608-136">등록 항목을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-136">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="6d608-137">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="6d608-137">-RegistrationId</span></span>
<span data-ttu-id="6d608-138">개별 등록 등록 id입니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-138">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="6d608-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="6d608-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="6d608-140">다른 Iot Hub로 다시 프로 비전 할 때 처리 될 장치 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="6d608-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d608-141">-ResourceGroupName</span></span>
<span data-ttu-id="6d608-142">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6d608-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d608-143">-ResourceId</span></span>
<span data-ttu-id="6d608-144">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="6d608-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="6d608-145">태그</span><span class="sxs-lookup"><span data-stu-id="6d608-145">-Tag</span></span>
<span data-ttu-id="6d608-146">초기 트윈 태그</span><span class="sxs-lookup"><span data-stu-id="6d608-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="6d608-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="6d608-147">-WebhookUrl</span></span>
<span data-ttu-id="6d608-148">사용자 지정 할당 요청에 사용 되는 webhook URL입니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="6d608-149">-확인</span><span class="sxs-lookup"><span data-stu-id="6d608-149">-Confirm</span></span>
<span data-ttu-id="6d608-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d608-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d608-151">-WhatIf</span></span>
<span data-ttu-id="6d608-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d608-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d608-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d608-154">CommonParameters</span></span>
<span data-ttu-id="6d608-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d608-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d608-156">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d608-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d608-157">입력</span><span class="sxs-lookup"><span data-stu-id="6d608-157">INPUTS</span></span>

### <span data-ttu-id="6d608-158">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="6d608-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="6d608-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6d608-159">System.String</span></span>

## <span data-ttu-id="6d608-160">출력</span><span class="sxs-lookup"><span data-stu-id="6d608-160">OUTPUTS</span></span>

### <span data-ttu-id="6d608-161">DeviceProvisioningServices. PSIndividualEnrollment/. \*</span><span class="sxs-lookup"><span data-stu-id="6d608-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="6d608-162">상속자</span><span class="sxs-lookup"><span data-stu-id="6d608-162">NOTES</span></span>

## <span data-ttu-id="6d608-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d608-163">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 511d0445f7c27acf7ace059852f6e4a8b23655b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985077"
---
# <span data-ttu-id="9a4e8-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="9a4e8-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="9a4e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a4e8-102">SYNOPSIS</span></span>
<span data-ttu-id="9a4e8-103">디바이스 등록 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="9a4e8-104">구문</span><span class="sxs-lookup"><span data-stu-id="9a4e8-104">SYNTAX</span></span>

### <span data-ttu-id="9a4e8-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9a4e8-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a4e8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9a4e8-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a4e8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9a4e8-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a4e8-108">설명</span><span class="sxs-lookup"><span data-stu-id="9a4e8-108">DESCRIPTION</span></span>
<span data-ttu-id="9a4e8-109">Azure IoT Hub 디바이스 프로비전 서비스에서 등록 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="9a4e8-110">예제</span><span class="sxs-lookup"><span data-stu-id="9a4e8-110">EXAMPLES</span></span>

### <span data-ttu-id="9a4e8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9a4e8-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="9a4e8-112">등록 그룹에 대한 할당 정책 및 허브를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="9a4e8-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="9a4e8-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="9a4e8-114">등록 그룹의 초기 쌍 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-114">Update an enrollment group's initial twin state.</span></span>

### <span data-ttu-id="9a4e8-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="9a4e8-115">Example 3</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -PrimaryKey "newPrimaryKey" -SecondaryKey "newSecondaryKey"
```

<span data-ttu-id="9a4e8-116">대칭 키 등록 그룹의 기본 키 및 보조 키 업데이트</span><span class="sxs-lookup"><span data-stu-id="9a4e8-116">Update a symmetric key enrollment group's primary and secondary keys</span></span>

## <span data-ttu-id="9a4e8-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9a4e8-117">PARAMETERS</span></span>

### <span data-ttu-id="9a4e8-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="9a4e8-118">-AllocationPolicy</span></span>
<span data-ttu-id="9a4e8-119">허브에 할당된 디바이스에 대한 할당 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="9a4e8-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9a4e8-120">-ApiVersion</span></span>
<span data-ttu-id="9a4e8-121">사용자 지정 할당 요청의 프로비전 서비스의 API 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="9a4e8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a4e8-122">-DefaultProfile</span></span>
<span data-ttu-id="9a4e8-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a4e8-124">-desired</span><span class="sxs-lookup"><span data-stu-id="9a4e8-124">-Desired</span></span>
<span data-ttu-id="9a4e8-125">초기 쌍 원하는 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-125">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="9a4e8-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="9a4e8-126">-DpsName</span></span>
<span data-ttu-id="9a4e8-127">IoT 디바이스 프로비전 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="9a4e8-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9a4e8-128">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="9a4e8-128">-DpsObject</span></span>
<span data-ttu-id="9a4e8-129">IoT 디바이스 프로비전 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="9a4e8-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="9a4e8-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9a4e8-130">-EdgeEnabled</span></span>
<span data-ttu-id="9a4e8-131">에지 활성화를 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="9a4e8-132">-IotHub</span><span class="sxs-lookup"><span data-stu-id="9a4e8-132">-IotHub</span></span>
<span data-ttu-id="9a4e8-133">대상 IoT Hub의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="9a4e8-134">여러 IoT Hubs에 대해 공백으로 구분된 목록을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-134">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="9a4e8-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="9a4e8-135">-IotHubHostName</span></span>
<span data-ttu-id="9a4e8-136">대상 IoT Hub의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="9a4e8-137">-Name</span><span class="sxs-lookup"><span data-stu-id="9a4e8-137">-Name</span></span>
<span data-ttu-id="9a4e8-138">등록 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-138">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="9a4e8-139">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="9a4e8-139">-PrimaryCAName</span></span>
<span data-ttu-id="9a4e8-140">기본 루트 CA 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-140">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="9a4e8-141">루트 CA 인증서를 증명하는 것이 필요한 경우 루트 ca 이름을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-141">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="9a4e8-142">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="9a4e8-142">-PrimaryCertificate</span></span>
<span data-ttu-id="9a4e8-143">기본 인증서를 포함하는 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-143">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="9a4e8-144">X509 인증서 .cer 파일 또는 .pem 파일 경로의 Base-64 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-144">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="9a4e8-145">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="9a4e8-145">-PrimaryKey</span></span>
<span data-ttu-id="9a4e8-146">base64 형식으로 저장된 기본 대칭 공유 액세스 키입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-146">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="9a4e8-147">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="9a4e8-147">-ProvisioningStatus</span></span>
<span data-ttu-id="9a4e8-148">등록 항목을 사용하도록 설정하거나 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-148">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="9a4e8-149">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="9a4e8-149">-ReprovisionPolicy</span></span>
<span data-ttu-id="9a4e8-150">다른 Iot Hub로 다시 프로비전할 때 처리할 디바이스 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-150">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="9a4e8-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a4e8-151">-ResourceGroupName</span></span>
<span data-ttu-id="9a4e8-152">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="9a4e8-152">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9a4e8-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a4e8-153">-ResourceId</span></span>
<span data-ttu-id="9a4e8-154">IoT 디바이스 프로비전 서비스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9a4e8-154">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="9a4e8-155">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="9a4e8-155">-RootCertificate</span></span>
<span data-ttu-id="9a4e8-156">루트 인증서를 사용하여 X509attestation을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-156">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="9a4e8-157">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="9a4e8-157">-SecondaryCAName</span></span>
<span data-ttu-id="9a4e8-158">보조 루트 CA 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-158">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="9a4e8-159">루트 CA 인증서를 증명하는 것이 필요한 경우 루트 ca 이름을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-159">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="9a4e8-160">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="9a4e8-160">-SecondaryCertificate</span></span>
<span data-ttu-id="9a4e8-161">보조 인증서를 포함하는 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-161">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="9a4e8-162">X509 인증서 .cer 파일 또는 .pem 파일 경로의 Base-64 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-162">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="9a4e8-163">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="9a4e8-163">-SecondaryKey</span></span>
<span data-ttu-id="9a4e8-164">base64 형식으로 저장된 보조 대칭 공유 액세스 키입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-164">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="9a4e8-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="9a4e8-165">-Tag</span></span>
<span data-ttu-id="9a4e8-166">초기 쌍 태그.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-166">Initial twin tags.</span></span>

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

### <span data-ttu-id="9a4e8-167">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="9a4e8-167">-WebhookUrl</span></span>
<span data-ttu-id="9a4e8-168">사용자 지정 할당 요청에 사용되는 웹후크 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-168">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="9a4e8-169">-확인</span><span class="sxs-lookup"><span data-stu-id="9a4e8-169">-Confirm</span></span>
<span data-ttu-id="9a4e8-170">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a4e8-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a4e8-171">-WhatIf</span></span>
<span data-ttu-id="9a4e8-172">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a4e8-173">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a4e8-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a4e8-174">CommonParameters</span></span>
<span data-ttu-id="9a4e8-175">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a4e8-176">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9a4e8-176">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a4e8-177">입력</span><span class="sxs-lookup"><span data-stu-id="9a4e8-177">INPUTS</span></span>

### <span data-ttu-id="9a4e8-178">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="9a4e8-178">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="9a4e8-179">System.String</span><span class="sxs-lookup"><span data-stu-id="9a4e8-179">System.String</span></span>

## <span data-ttu-id="9a4e8-180">출력</span><span class="sxs-lookup"><span data-stu-id="9a4e8-180">OUTPUTS</span></span>

### <span data-ttu-id="9a4e8-181">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="9a4e8-181">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="9a4e8-182">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9a4e8-182">NOTES</span></span>

## <span data-ttu-id="9a4e8-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a4e8-183">RELATED LINKS</span></span>

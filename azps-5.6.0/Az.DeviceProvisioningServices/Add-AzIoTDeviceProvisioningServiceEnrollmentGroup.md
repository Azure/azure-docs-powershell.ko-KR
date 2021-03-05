---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 89a1bede6ff90b58b83a7c401860c66430958fcc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996688"
---
# <span data-ttu-id="d60ba-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="d60ba-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="d60ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d60ba-102">SYNOPSIS</span></span>
<span data-ttu-id="d60ba-103">디바이스 등록 그룹을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="d60ba-104">구문</span><span class="sxs-lookup"><span data-stu-id="d60ba-104">SYNTAX</span></span>

### <span data-ttu-id="d60ba-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d60ba-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d60ba-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d60ba-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d60ba-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d60ba-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d60ba-108">설명</span><span class="sxs-lookup"><span data-stu-id="d60ba-108">DESCRIPTION</span></span>
<span data-ttu-id="d60ba-109">Azure IoT Hub 디바이스 프로비전 서비스에서 등록 그룹을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="d60ba-110">예제</span><span class="sxs-lookup"><span data-stu-id="d60ba-110">EXAMPLES</span></span>

### <span data-ttu-id="d60ba-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d60ba-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="d60ba-112">인증 형식 SymmetricKey를 사용하여 등록 만들기</span><span class="sxs-lookup"><span data-stu-id="d60ba-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="d60ba-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d60ba-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="d60ba-114">등록 유형 X509를 사용하여 등록 만들기</span><span class="sxs-lookup"><span data-stu-id="d60ba-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="d60ba-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="d60ba-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="d60ba-116">인증 형식 SymmetricKey 및 초기 쌍 상태로 등록을 만드면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="d60ba-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d60ba-117">PARAMETERS</span></span>

### <span data-ttu-id="d60ba-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="d60ba-118">-AllocationPolicy</span></span>
<span data-ttu-id="d60ba-119">허브에 할당된 디바이스에 대한 할당 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="d60ba-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d60ba-120">-ApiVersion</span></span>
<span data-ttu-id="d60ba-121">사용자 지정 할당 요청의 프로비전 서비스의 API 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="d60ba-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="d60ba-122">-AttestationType</span></span>
<span data-ttu-id="d60ba-123">Attestation 메커니즘입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-123">Attestation Mechanism.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAttestationMechanismType
Parameter Sets: (All)
Aliases:
Accepted values: None, Tpm, X509, SymmetricKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d60ba-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d60ba-124">-DefaultProfile</span></span>
<span data-ttu-id="d60ba-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d60ba-126">-desired</span><span class="sxs-lookup"><span data-stu-id="d60ba-126">-Desired</span></span>
<span data-ttu-id="d60ba-127">초기 쌍 원하는 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-127">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="d60ba-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="d60ba-128">-DpsName</span></span>
<span data-ttu-id="d60ba-129">IoT 디바이스 프로비전 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="d60ba-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d60ba-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="d60ba-130">-DpsObject</span></span>
<span data-ttu-id="d60ba-131">IoT 디바이스 프로비전 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="d60ba-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d60ba-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="d60ba-132">-EdgeEnabled</span></span>
<span data-ttu-id="d60ba-133">에지 활성화를 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="d60ba-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="d60ba-134">-IotHub</span></span>
<span data-ttu-id="d60ba-135">대상 IoT Hub의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="d60ba-136">여러 IoT Hubs에 대해 공백으로 구분된 목록을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="d60ba-136">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="d60ba-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="d60ba-137">-IotHubHostName</span></span>
<span data-ttu-id="d60ba-138">대상 IoT Hub의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="d60ba-139">-Name</span><span class="sxs-lookup"><span data-stu-id="d60ba-139">-Name</span></span>
<span data-ttu-id="d60ba-140">등록 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-140">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="d60ba-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="d60ba-141">-PrimaryCAName</span></span>
<span data-ttu-id="d60ba-142">기본 루트 CA 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="d60ba-143">루트 CA 인증서를 증명하는 것이 필요한 경우 루트 ca 이름을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="d60ba-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="d60ba-144">-PrimaryCertificate</span></span>
<span data-ttu-id="d60ba-145">기본 인증서를 포함하는 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="d60ba-146">X509 인증서 .cer 파일 또는 .pem 파일 경로의 Base-64 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="d60ba-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="d60ba-147">-PrimaryKey</span></span>
<span data-ttu-id="d60ba-148">base64 형식으로 저장된 기본 대칭 공유 액세스 키입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="d60ba-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="d60ba-149">-ProvisioningStatus</span></span>
<span data-ttu-id="d60ba-150">등록 항목을 사용하도록 설정하거나 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="d60ba-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="d60ba-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="d60ba-152">다른 Iot Hub로 다시 프로비전할 때 처리할 디바이스 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="d60ba-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d60ba-153">-ResourceGroupName</span></span>
<span data-ttu-id="d60ba-154">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="d60ba-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d60ba-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d60ba-155">-ResourceId</span></span>
<span data-ttu-id="d60ba-156">IoT 디바이스 프로비전 서비스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d60ba-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d60ba-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="d60ba-157">-RootCertificate</span></span>
<span data-ttu-id="d60ba-158">루트 인증서를 사용하여 X509attestation을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-158">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="d60ba-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="d60ba-159">-SecondaryCAName</span></span>
<span data-ttu-id="d60ba-160">보조 루트 CA 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="d60ba-161">루트 CA 인증서를 증명하는 것이 필요한 경우 루트 ca 이름을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="d60ba-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="d60ba-162">-SecondaryCertificate</span></span>
<span data-ttu-id="d60ba-163">보조 인증서를 포함하는 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="d60ba-164">X509 인증서 .cer 파일 또는 .pem 파일 경로의 Base-64 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="d60ba-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="d60ba-165">-SecondaryKey</span></span>
<span data-ttu-id="d60ba-166">base64 형식으로 저장된 보조 대칭 공유 액세스 키입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="d60ba-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="d60ba-167">-Tag</span></span>
<span data-ttu-id="d60ba-168">초기 쌍 태그.</span><span class="sxs-lookup"><span data-stu-id="d60ba-168">Initial twin tags.</span></span>

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

### <span data-ttu-id="d60ba-169">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="d60ba-169">-WebhookUrl</span></span>
<span data-ttu-id="d60ba-170">사용자 지정 할당 요청에 사용되는 웹후크 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="d60ba-171">-확인</span><span class="sxs-lookup"><span data-stu-id="d60ba-171">-Confirm</span></span>
<span data-ttu-id="d60ba-172">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d60ba-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d60ba-173">-WhatIf</span></span>
<span data-ttu-id="d60ba-174">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d60ba-175">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d60ba-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d60ba-176">CommonParameters</span></span>
<span data-ttu-id="d60ba-177">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d60ba-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d60ba-178">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d60ba-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d60ba-179">입력</span><span class="sxs-lookup"><span data-stu-id="d60ba-179">INPUTS</span></span>

### <span data-ttu-id="d60ba-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="d60ba-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="d60ba-181">System.String</span><span class="sxs-lookup"><span data-stu-id="d60ba-181">System.String</span></span>

## <span data-ttu-id="d60ba-182">출력</span><span class="sxs-lookup"><span data-stu-id="d60ba-182">OUTPUTS</span></span>

### <span data-ttu-id="d60ba-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="d60ba-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="d60ba-184">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d60ba-184">NOTES</span></span>

## <span data-ttu-id="d60ba-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d60ba-185">RELATED LINKS</span></span>

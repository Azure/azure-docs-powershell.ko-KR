---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 7c5c2f747b5de24e1ccf3a4cf047930746c0d863
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215529"
---
# <span data-ttu-id="39cfd-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="39cfd-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="39cfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39cfd-102">SYNOPSIS</span></span>
<span data-ttu-id="39cfd-103">장치 등록 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="39cfd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39cfd-104">SYNTAX</span></span>

### <span data-ttu-id="39cfd-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="39cfd-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39cfd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="39cfd-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39cfd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="39cfd-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39cfd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="39cfd-108">DESCRIPTION</span></span>
<span data-ttu-id="39cfd-109">Azure IoT Hub 디바이스 프로비저닝 서비스에서 등록 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="39cfd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="39cfd-110">EXAMPLES</span></span>

### <span data-ttu-id="39cfd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="39cfd-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="39cfd-112">증명 형식 SymmetricKey를 사용 하 여 등록 만들기</span><span class="sxs-lookup"><span data-stu-id="39cfd-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="39cfd-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="39cfd-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="39cfd-114">증명 형식 X509를 사용 하 여 등록 만들기</span><span class="sxs-lookup"><span data-stu-id="39cfd-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="39cfd-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="39cfd-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag
```

<span data-ttu-id="39cfd-116">증명 형식 SymmetricKey 및 초기 트윈 상태를 사용 하 여 등록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="39cfd-117">변수</span><span class="sxs-lookup"><span data-stu-id="39cfd-117">PARAMETERS</span></span>

### <span data-ttu-id="39cfd-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="39cfd-118">-AllocationPolicy</span></span>
<span data-ttu-id="39cfd-119">허브에 할당 된 장치에 대 한 할당 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="39cfd-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="39cfd-120">-ApiVersion</span></span>
<span data-ttu-id="39cfd-121">사용자 지정 할당 요청에서 제공 하는 프로비저닝 서비스의 API 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="39cfd-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="39cfd-122">-AttestationType</span></span>
<span data-ttu-id="39cfd-123">증명 메커니즘.</span><span class="sxs-lookup"><span data-stu-id="39cfd-123">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="39cfd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39cfd-124">-DefaultProfile</span></span>
<span data-ttu-id="39cfd-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39cfd-126">-원하는</span><span class="sxs-lookup"><span data-stu-id="39cfd-126">-Desired</span></span>
<span data-ttu-id="39cfd-127">초기 트윈 필요 속성.</span><span class="sxs-lookup"><span data-stu-id="39cfd-127">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="39cfd-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="39cfd-128">-DpsName</span></span>
<span data-ttu-id="39cfd-129">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="39cfd-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="39cfd-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="39cfd-130">-DpsObject</span></span>
<span data-ttu-id="39cfd-131">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="39cfd-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="39cfd-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="39cfd-132">-EdgeEnabled</span></span>
<span data-ttu-id="39cfd-133">가장자리를 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="39cfd-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="39cfd-134">-IotHub</span></span>
<span data-ttu-id="39cfd-135">대상 IoT Hub의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="39cfd-136">여러 IoT Hub에 공백으로 구분 된 목록을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-136">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="39cfd-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="39cfd-137">-IotHubHostName</span></span>
<span data-ttu-id="39cfd-138">대상 IoT Hub의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="39cfd-139">-이름</span><span class="sxs-lookup"><span data-stu-id="39cfd-139">-Name</span></span>
<span data-ttu-id="39cfd-140">등록 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-140">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="39cfd-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="39cfd-141">-PrimaryCAName</span></span>
<span data-ttu-id="39cfd-142">주 루트 CA 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="39cfd-143">루트 CA 인증서가 있는 증명을 원하는 경우 루트 ca 이름을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="39cfd-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="39cfd-144">-PrimaryCertificate</span></span>
<span data-ttu-id="39cfd-145">기본 인증서를 포함 하는 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="39cfd-146">Base-64는 X509 인증서 .cer 파일 또는 pem 파일 경로의 표시입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="39cfd-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="39cfd-147">-PrimaryKey</span></span>
<span data-ttu-id="39cfd-148">Base64 형식으로 저장 된 기본 대칭 공유 액세스 키입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="39cfd-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="39cfd-149">-ProvisioningStatus</span></span>
<span data-ttu-id="39cfd-150">등록 항목을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="39cfd-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="39cfd-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="39cfd-152">다른 Iot Hub로 다시 프로 비전 할 때 처리 될 장치 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="39cfd-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39cfd-153">-ResourceGroupName</span></span>
<span data-ttu-id="39cfd-154">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="39cfd-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39cfd-155">-ResourceId</span></span>
<span data-ttu-id="39cfd-156">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="39cfd-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="39cfd-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="39cfd-157">-RootCertificate</span></span>
<span data-ttu-id="39cfd-158">루트 인증서를 사용 하 여 X509attestation를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-158">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="39cfd-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="39cfd-159">-SecondaryCAName</span></span>
<span data-ttu-id="39cfd-160">보조 루트 CA 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="39cfd-161">루트 CA 인증서가 있는 증명을 원하는 경우 루트 ca 이름을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="39cfd-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="39cfd-162">-SecondaryCertificate</span></span>
<span data-ttu-id="39cfd-163">보조 인증서를 포함 하는 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="39cfd-164">Base-64는 X509 인증서 .cer 파일 또는 pem 파일 경로의 표시입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="39cfd-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="39cfd-165">-SecondaryKey</span></span>
<span data-ttu-id="39cfd-166">Base64 형식으로 저장 된 보조 대칭 공유 액세스 키입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="39cfd-167">태그</span><span class="sxs-lookup"><span data-stu-id="39cfd-167">-Tag</span></span>
<span data-ttu-id="39cfd-168">초기 트윈 태그</span><span class="sxs-lookup"><span data-stu-id="39cfd-168">Initial twin tags.</span></span>

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

### <span data-ttu-id="39cfd-169">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="39cfd-169">-WebhookUrl</span></span>
<span data-ttu-id="39cfd-170">사용자 지정 할당 요청에 사용 되는 webhook URL입니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="39cfd-171">-확인</span><span class="sxs-lookup"><span data-stu-id="39cfd-171">-Confirm</span></span>
<span data-ttu-id="39cfd-172">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39cfd-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39cfd-173">-WhatIf</span></span>
<span data-ttu-id="39cfd-174">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39cfd-175">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39cfd-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39cfd-176">CommonParameters</span></span>
<span data-ttu-id="39cfd-177">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39cfd-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39cfd-178">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39cfd-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39cfd-179">입력</span><span class="sxs-lookup"><span data-stu-id="39cfd-179">INPUTS</span></span>

### <span data-ttu-id="39cfd-180">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="39cfd-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="39cfd-181">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="39cfd-181">System.String</span></span>

## <span data-ttu-id="39cfd-182">출력</span><span class="sxs-lookup"><span data-stu-id="39cfd-182">OUTPUTS</span></span>

### <span data-ttu-id="39cfd-183">DeviceProvisioningServices. PSEnrollmentGroup/. \*</span><span class="sxs-lookup"><span data-stu-id="39cfd-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="39cfd-184">상속자</span><span class="sxs-lookup"><span data-stu-id="39cfd-184">NOTES</span></span>

## <span data-ttu-id="39cfd-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39cfd-185">RELATED LINKS</span></span>

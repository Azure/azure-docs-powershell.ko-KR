---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: b3c97abdee88615eedb2bb1f4452309326a4ebfa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196409"
---
# <span data-ttu-id="af3d1-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="af3d1-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="af3d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af3d1-102">SYNOPSIS</span></span>
<span data-ttu-id="af3d1-103">디바이스 등록 레코드를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="af3d1-104">구문</span><span class="sxs-lookup"><span data-stu-id="af3d1-104">SYNTAX</span></span>

### <span data-ttu-id="af3d1-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="af3d1-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af3d1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="af3d1-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af3d1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="af3d1-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 -AttestationType <PSAttestationMechanismType> [-DeviceId <String>] [-EndorsementKey <String>]
 [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af3d1-108">설명</span><span class="sxs-lookup"><span data-stu-id="af3d1-108">DESCRIPTION</span></span>
<span data-ttu-id="af3d1-109">Azure IoT Hub Device Provisioning Service에서 디바이스 등록을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="af3d1-110">예제</span><span class="sxs-lookup"><span data-stu-id="af3d1-110">EXAMPLES</span></span>

### <span data-ttu-id="af3d1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="af3d1-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="af3d1-112">SymmetricKey 형식의 등록 만들기</span><span class="sxs-lookup"><span data-stu-id="af3d1-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="af3d1-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="af3d1-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="af3d1-114">TPM 등록을 사용하여 등록을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="af3d1-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="af3d1-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="af3d1-116">X509 형식의 등록 만들기</span><span class="sxs-lookup"><span data-stu-id="af3d1-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="af3d1-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="af3d1-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="af3d1-118">SymmetricKey 및 초기 쌍 상태를 사용하여 등록을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="af3d1-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af3d1-119">PARAMETERS</span></span>

### <span data-ttu-id="af3d1-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="af3d1-120">-AllocationPolicy</span></span>
<span data-ttu-id="af3d1-121">허브에 할당된 디바이스에 대한 할당 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="af3d1-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="af3d1-122">-ApiVersion</span></span>
<span data-ttu-id="af3d1-123">사용자 지정 할당 요청의 프로비전 서비스의 API 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="af3d1-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="af3d1-124">-AttestationType</span></span>
<span data-ttu-id="af3d1-125">Attestation 메커니즘.</span><span class="sxs-lookup"><span data-stu-id="af3d1-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="af3d1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af3d1-126">-DefaultProfile</span></span>
<span data-ttu-id="af3d1-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af3d1-128">-Desired</span><span class="sxs-lookup"><span data-stu-id="af3d1-128">-Desired</span></span>
<span data-ttu-id="af3d1-129">초기 쌍 desired 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="af3d1-130">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="af3d1-130">-DeviceId</span></span>
<span data-ttu-id="af3d1-131">IoT Hub 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="af3d1-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="af3d1-132">-DpsName</span></span>
<span data-ttu-id="af3d1-133">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="af3d1-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="af3d1-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="af3d1-134">-DpsObject</span></span>
<span data-ttu-id="af3d1-135">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="af3d1-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="af3d1-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="af3d1-136">-EdgeEnabled</span></span>
<span data-ttu-id="af3d1-137">에지 사용률을 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="af3d1-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="af3d1-138">-EndorsementKey</span></span>
<span data-ttu-id="af3d1-139">TPM 디바이스에 대한 TPM의 증권 키입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="af3d1-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="af3d1-140">-IotHub</span></span>
<span data-ttu-id="af3d1-141">대상 IoT Hub의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="af3d1-142">여러 IoT Hub에 공백으로 구분된 목록을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="af3d1-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="af3d1-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="af3d1-143">-IotHubHostName</span></span>
<span data-ttu-id="af3d1-144">대상 IoT Hub의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="af3d1-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="af3d1-145">-PrimaryCAName</span></span>
<span data-ttu-id="af3d1-146">기본 루트 CA 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="af3d1-147">루트 CA 인증서를 증명하는 것이 필요한 경우 루트 ca 이름을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="af3d1-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="af3d1-148">-PrimaryCertificate</span></span>
<span data-ttu-id="af3d1-149">기본 인증서를 포함하는 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="af3d1-150">X509 인증서 .cer 파일 또는 .pem 파일 경로의 Base-64 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="af3d1-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="af3d1-151">-PrimaryKey</span></span>
<span data-ttu-id="af3d1-152">base64 형식으로 저장된 기본 대칭 공유 액세스 키입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="af3d1-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="af3d1-153">-ProvisioningStatus</span></span>
<span data-ttu-id="af3d1-154">등록 항목을 설정하거나 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="af3d1-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="af3d1-155">-RegistrationId</span></span>
<span data-ttu-id="af3d1-156">개별 등록 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="af3d1-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="af3d1-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="af3d1-158">다른 Iot Hub에 다시 프로비전할 때 처리할 디바이스 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="af3d1-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af3d1-159">-ResourceGroupName</span></span>
<span data-ttu-id="af3d1-160">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="af3d1-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="af3d1-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af3d1-161">-ResourceId</span></span>
<span data-ttu-id="af3d1-162">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="af3d1-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="af3d1-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="af3d1-163">-RootCertificate</span></span>
<span data-ttu-id="af3d1-164">루트 인증서를 사용하여 X509attestation을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="af3d1-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="af3d1-165">-SecondaryCAName</span></span>
<span data-ttu-id="af3d1-166">보조 루트 CA 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="af3d1-167">루트 CA 인증서를 증명하는 것이 필요한 경우 루트 ca 이름을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="af3d1-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="af3d1-168">-SecondaryCertificate</span></span>
<span data-ttu-id="af3d1-169">보조 인증서를 포함하는 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="af3d1-170">X509 인증서 .cer 파일 또는 .pem 파일 경로의 Base-64 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="af3d1-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="af3d1-171">-SecondaryKey</span></span>
<span data-ttu-id="af3d1-172">base64 형식으로 저장된 보조 대칭 공유 액세스 키입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="af3d1-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="af3d1-173">-StorageRootKey</span></span>
<span data-ttu-id="af3d1-174">TPM 디바이스에 대한 TPM 저장소 루트 키입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="af3d1-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="af3d1-175">-Tag</span></span>
<span data-ttu-id="af3d1-176">초기 쌍 태그.</span><span class="sxs-lookup"><span data-stu-id="af3d1-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="af3d1-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="af3d1-177">-WebhookUrl</span></span>
<span data-ttu-id="af3d1-178">사용자 지정 할당 요청에 사용되는 웹후크 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="af3d1-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af3d1-179">-Confirm</span></span>
<span data-ttu-id="af3d1-180">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af3d1-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af3d1-181">-WhatIf</span></span>
<span data-ttu-id="af3d1-182">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="af3d1-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af3d1-183">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af3d1-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af3d1-184">CommonParameters</span></span>
<span data-ttu-id="af3d1-185">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="af3d1-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af3d1-186">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="af3d1-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af3d1-187">입력</span><span class="sxs-lookup"><span data-stu-id="af3d1-187">INPUTS</span></span>

### <span data-ttu-id="af3d1-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="af3d1-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="af3d1-189">System.String</span><span class="sxs-lookup"><span data-stu-id="af3d1-189">System.String</span></span>

## <span data-ttu-id="af3d1-190">출력</span><span class="sxs-lookup"><span data-stu-id="af3d1-190">OUTPUTS</span></span>

### <span data-ttu-id="af3d1-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="af3d1-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="af3d1-192">참고 사항</span><span class="sxs-lookup"><span data-stu-id="af3d1-192">NOTES</span></span>

## <span data-ttu-id="af3d1-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af3d1-193">RELATED LINKS</span></span>

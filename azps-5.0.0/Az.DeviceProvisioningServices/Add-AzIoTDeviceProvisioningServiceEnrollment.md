---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: e02d9c1ca9a5d45f081f168c3d8736d502f52094
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215534"
---
# <span data-ttu-id="78b4e-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="78b4e-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="78b4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78b4e-102">SYNOPSIS</span></span>
<span data-ttu-id="78b4e-103">장치 등록 레코드를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="78b4e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78b4e-104">SYNTAX</span></span>

### <span data-ttu-id="78b4e-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="78b4e-105">ResourceSet (Default)</span></span>
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

### <span data-ttu-id="78b4e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="78b4e-106">InputObjectSet</span></span>
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

### <span data-ttu-id="78b4e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="78b4e-107">ResourceIdSet</span></span>
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

## <span data-ttu-id="78b4e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="78b4e-108">DESCRIPTION</span></span>
<span data-ttu-id="78b4e-109">Azure IoT Hub 디바이스 프로비저닝 서비스에서 디바이스 등록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="78b4e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="78b4e-110">EXAMPLES</span></span>

### <span data-ttu-id="78b4e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="78b4e-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="78b4e-112">증명 형식 SymmetricKey를 사용 하 여 등록 만들기</span><span class="sxs-lookup"><span data-stu-id="78b4e-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="78b4e-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="78b4e-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="78b4e-114">TPM 증명을 사용 하 여 등록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="78b4e-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="78b4e-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="78b4e-116">증명 형식 X509를 사용 하 여 등록 만들기</span><span class="sxs-lookup"><span data-stu-id="78b4e-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="78b4e-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="78b4e-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag
```

<span data-ttu-id="78b4e-118">증명 형식 SymmetricKey 및 초기 트윈 상태를 사용 하 여 등록을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="78b4e-119">변수</span><span class="sxs-lookup"><span data-stu-id="78b4e-119">PARAMETERS</span></span>

### <span data-ttu-id="78b4e-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="78b4e-120">-AllocationPolicy</span></span>
<span data-ttu-id="78b4e-121">허브에 할당 된 장치에 대 한 할당 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="78b4e-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="78b4e-122">-ApiVersion</span></span>
<span data-ttu-id="78b4e-123">사용자 지정 할당 요청에서 제공 하는 프로비저닝 서비스의 API 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="78b4e-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="78b4e-124">-AttestationType</span></span>
<span data-ttu-id="78b4e-125">증명 메커니즘.</span><span class="sxs-lookup"><span data-stu-id="78b4e-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="78b4e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78b4e-126">-DefaultProfile</span></span>
<span data-ttu-id="78b4e-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78b4e-128">-원하는</span><span class="sxs-lookup"><span data-stu-id="78b4e-128">-Desired</span></span>
<span data-ttu-id="78b4e-129">초기 트윈 필요 속성.</span><span class="sxs-lookup"><span data-stu-id="78b4e-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="78b4e-130">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="78b4e-130">-DeviceId</span></span>
<span data-ttu-id="78b4e-131">IoT Hub 디바이스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="78b4e-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="78b4e-132">-DpsName</span></span>
<span data-ttu-id="78b4e-133">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="78b4e-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="78b4e-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="78b4e-134">-DpsObject</span></span>
<span data-ttu-id="78b4e-135">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="78b4e-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="78b4e-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="78b4e-136">-EdgeEnabled</span></span>
<span data-ttu-id="78b4e-137">가장자리를 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="78b4e-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="78b4e-138">-EndorsementKey</span></span>
<span data-ttu-id="78b4e-139">TPM 장치에 대 한 TPM 인증 키입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="78b4e-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="78b4e-140">-IotHub</span></span>
<span data-ttu-id="78b4e-141">대상 IoT Hub의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="78b4e-142">여러 IoT Hub에 공백으로 구분 된 목록을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="78b4e-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="78b4e-143">-IotHubHostName</span></span>
<span data-ttu-id="78b4e-144">대상 IoT Hub의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="78b4e-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="78b4e-145">-PrimaryCAName</span></span>
<span data-ttu-id="78b4e-146">주 루트 CA 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="78b4e-147">루트 CA 인증서가 있는 증명을 원하는 경우 루트 ca 이름을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="78b4e-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="78b4e-148">-PrimaryCertificate</span></span>
<span data-ttu-id="78b4e-149">기본 인증서를 포함 하는 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="78b4e-150">Base-64는 X509 인증서 .cer 파일 또는 pem 파일 경로의 표시입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="78b4e-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="78b4e-151">-PrimaryKey</span></span>
<span data-ttu-id="78b4e-152">Base64 형식으로 저장 된 기본 대칭 공유 액세스 키입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="78b4e-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="78b4e-153">-ProvisioningStatus</span></span>
<span data-ttu-id="78b4e-154">등록 항목을 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="78b4e-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="78b4e-155">-RegistrationId</span></span>
<span data-ttu-id="78b4e-156">개별 등록 등록 id입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="78b4e-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="78b4e-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="78b4e-158">다른 Iot Hub로 다시 프로 비전 할 때 처리 될 장치 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="78b4e-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78b4e-159">-ResourceGroupName</span></span>
<span data-ttu-id="78b4e-160">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="78b4e-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78b4e-161">-ResourceId</span></span>
<span data-ttu-id="78b4e-162">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="78b4e-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="78b4e-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="78b4e-163">-RootCertificate</span></span>
<span data-ttu-id="78b4e-164">루트 인증서를 사용 하 여 X509attestation를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="78b4e-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="78b4e-165">-SecondaryCAName</span></span>
<span data-ttu-id="78b4e-166">보조 루트 CA 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="78b4e-167">루트 CA 인증서가 있는 증명을 원하는 경우 루트 ca 이름을 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="78b4e-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="78b4e-168">-SecondaryCertificate</span></span>
<span data-ttu-id="78b4e-169">보조 인증서를 포함 하는 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="78b4e-170">Base-64는 X509 인증서 .cer 파일 또는 pem 파일 경로의 표시입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="78b4e-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="78b4e-171">-SecondaryKey</span></span>
<span data-ttu-id="78b4e-172">Base64 형식으로 저장 된 보조 대칭 공유 액세스 키입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="78b4e-173">-Storager이 Tkey</span><span class="sxs-lookup"><span data-stu-id="78b4e-173">-StorageRootKey</span></span>
<span data-ttu-id="78b4e-174">TPM 장치에 대 한 TPM 저장소 루트 키입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="78b4e-175">태그</span><span class="sxs-lookup"><span data-stu-id="78b4e-175">-Tag</span></span>
<span data-ttu-id="78b4e-176">초기 트윈 태그</span><span class="sxs-lookup"><span data-stu-id="78b4e-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="78b4e-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="78b4e-177">-WebhookUrl</span></span>
<span data-ttu-id="78b4e-178">사용자 지정 할당 요청에 사용 되는 webhook URL입니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="78b4e-179">-확인</span><span class="sxs-lookup"><span data-stu-id="78b4e-179">-Confirm</span></span>
<span data-ttu-id="78b4e-180">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78b4e-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78b4e-181">-WhatIf</span></span>
<span data-ttu-id="78b4e-182">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78b4e-183">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78b4e-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b4e-184">CommonParameters</span></span>
<span data-ttu-id="78b4e-185">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78b4e-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b4e-186">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78b4e-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b4e-187">입력</span><span class="sxs-lookup"><span data-stu-id="78b4e-187">INPUTS</span></span>

### <span data-ttu-id="78b4e-188">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="78b4e-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="78b4e-189">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="78b4e-189">System.String</span></span>

## <span data-ttu-id="78b4e-190">출력</span><span class="sxs-lookup"><span data-stu-id="78b4e-190">OUTPUTS</span></span>

### <span data-ttu-id="78b4e-191">DeviceProvisioningServices. PSIndividualEnrollment/. \*</span><span class="sxs-lookup"><span data-stu-id="78b4e-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="78b4e-192">상속자</span><span class="sxs-lookup"><span data-stu-id="78b4e-192">NOTES</span></span>

## <span data-ttu-id="78b4e-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78b4e-193">RELATED LINKS</span></span>

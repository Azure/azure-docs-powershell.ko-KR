---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 9b995a0ed80bf32b770fe6b157a283534d01f743
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492004"
---
# <span data-ttu-id="d0dd5-101">Set-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="d0dd5-101">Set-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="d0dd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="d0dd5-103">Azure IoT Hub Device Provisioning Service 인증서를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d0dd5-103">Verify an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="d0dd5-104">구문</span><span class="sxs-lookup"><span data-stu-id="d0dd5-104">SYNTAX</span></span>

### <span data-ttu-id="d0dd5-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d0dd5-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0dd5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d0dd5-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0dd5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d0dd5-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0dd5-108">설명</span><span class="sxs-lookup"><span data-stu-id="d0dd5-108">DESCRIPTION</span></span>
<span data-ttu-id="d0dd5-109">generate-verification-code를 호출하여 얻은 확인 코드를 포함하는 확인 인증서를 업로드하여 인증서를 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="d0dd5-109">Verify a certificate by uploading a verification certificate containing the verification code obtained by calling generate-verification-code.</span></span> <span data-ttu-id="d0dd5-110">소유 증명 프로세스의 마지막 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="d0dd5-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="d0dd5-111">Azure IoT Hub Device Provisioning Service의 CA 인증서에 대한 자세한 설명은 다음을 참조하세요. https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span><span class="sxs-lookup"><span data-stu-id="d0dd5-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span></span>

## <span data-ttu-id="d0dd5-112">예제</span><span class="sxs-lookup"><span data-stu-id="d0dd5-112">EXAMPLES</span></span>

### <span data-ttu-id="d0dd5-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="d0dd5-113">Example 1</span></span>
```
PS C:\> Set-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="d0dd5-114">"mycertificate" 개인 키의 소유권을 확인해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0dd5-114">Verify ownership of the "mycertificate" private key.</span></span>

### <span data-ttu-id="d0dd5-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="d0dd5-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | Set-AzIoTDpsCertificate -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="d0dd5-116">파이프라인을 사용하여 "mycertificate" 개인 키의 소유권을 검증합니다.</span><span class="sxs-lookup"><span data-stu-id="d0dd5-116">Verify ownership of the "mycertificate" private key using pipeline.</span></span>

## <span data-ttu-id="d0dd5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0dd5-117">PARAMETERS</span></span>

### <span data-ttu-id="d0dd5-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="d0dd5-118">-CertificateName</span></span>
<span data-ttu-id="d0dd5-119">Iot 디바이스 프로비전 서비스 인증서의 이름</span><span class="sxs-lookup"><span data-stu-id="d0dd5-119">Name of the Iot device provisioning service certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0dd5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0dd5-120">-DefaultProfile</span></span>
<span data-ttu-id="d0dd5-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0dd5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0dd5-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="d0dd5-122">-Etag</span></span>
<span data-ttu-id="d0dd5-123">인증서의 Etag</span><span class="sxs-lookup"><span data-stu-id="d0dd5-123">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0dd5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0dd5-124">-InputObject</span></span>
<span data-ttu-id="d0dd5-125">IoT Device Provisioning Service Certificate 개체</span><span class="sxs-lookup"><span data-stu-id="d0dd5-125">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0dd5-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d0dd5-126">-Name</span></span>
<span data-ttu-id="d0dd5-127">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="d0dd5-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d0dd5-128">-Path</span><span class="sxs-lookup"><span data-stu-id="d0dd5-128">-Path</span></span>
<span data-ttu-id="d0dd5-129">x509 인증서 .cer 파일 또는 .pem 파일 경로의 base-64 표현</span><span class="sxs-lookup"><span data-stu-id="d0dd5-129">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0dd5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0dd5-130">-ResourceGroupName</span></span>
<span data-ttu-id="d0dd5-131">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="d0dd5-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d0dd5-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0dd5-132">-ResourceId</span></span>
<span data-ttu-id="d0dd5-133">IoT Device Provisioning Service 인증서 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d0dd5-133">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="d0dd5-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0dd5-134">-Confirm</span></span>
<span data-ttu-id="d0dd5-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0dd5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0dd5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0dd5-136">-WhatIf</span></span>
<span data-ttu-id="d0dd5-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d0dd5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0dd5-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0dd5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0dd5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0dd5-139">CommonParameters</span></span>
<span data-ttu-id="d0dd5-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d0dd5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0dd5-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d0dd5-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0dd5-142">입력</span><span class="sxs-lookup"><span data-stu-id="d0dd5-142">INPUTS</span></span>

### <span data-ttu-id="d0dd5-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="d0dd5-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="d0dd5-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d0dd5-144">System.String</span></span>

## <span data-ttu-id="d0dd5-145">출력</span><span class="sxs-lookup"><span data-stu-id="d0dd5-145">OUTPUTS</span></span>

### <span data-ttu-id="d0dd5-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="d0dd5-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="d0dd5-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d0dd5-147">NOTES</span></span>

## <span data-ttu-id="d0dd5-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0dd5-148">RELATED LINKS</span></span>

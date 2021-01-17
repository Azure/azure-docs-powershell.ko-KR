---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: d4dcf52a3a705042f994c8106bd931a8b704a049
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492032"
---
# <span data-ttu-id="c0e5e-101">Add-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="c0e5e-101">Add-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="c0e5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e5e-103">Azure IoT Hub Device Provisioning Service 인증서를 만들고 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c0e5e-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="c0e5e-104">구문</span><span class="sxs-lookup"><span data-stu-id="c0e5e-104">SYNTAX</span></span>

### <span data-ttu-id="c0e5e-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c0e5e-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0e5e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c0e5e-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0e5e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c0e5e-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0e5e-108">설명</span><span class="sxs-lookup"><span data-stu-id="c0e5e-108">DESCRIPTION</span></span>
<span data-ttu-id="c0e5e-109">새 인증서를 업로드하거나 기존 인증서를 동일한 이름으로 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="c0e5e-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="c0e5e-110">Azure IoT Hub Device Provisioning Service의 CA 인증서에 대한 자세한 설명은 https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c0e5e-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="c0e5e-111">예제</span><span class="sxs-lookup"><span data-stu-id="c0e5e-111">EXAMPLES</span></span>

### <span data-ttu-id="c0e5e-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="c0e5e-112">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="c0e5e-113">AZURE IoT Hub 디바이스 프로비전 서비스에 CA 인증서 CER 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="c0e5e-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="c0e5e-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="c0e5e-114">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="c0e5e-115">새 CER 파일을 업로드하여 IoT Hub 디바이스 프로비전 서비스에서 CA 인증서를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c0e5e-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="c0e5e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0e5e-116">PARAMETERS</span></span>

### <span data-ttu-id="c0e5e-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c0e5e-117">-CertificateName</span></span>
<span data-ttu-id="c0e5e-118">Iot 디바이스 프로비전 서비스 인증서의 이름</span><span class="sxs-lookup"><span data-stu-id="c0e5e-118">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="c0e5e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e5e-119">-DefaultProfile</span></span>
<span data-ttu-id="c0e5e-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0e5e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0e5e-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="c0e5e-121">-Etag</span></span>
<span data-ttu-id="c0e5e-122">인증서의 Etag</span><span class="sxs-lookup"><span data-stu-id="c0e5e-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="c0e5e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0e5e-123">-InputObject</span></span>
<span data-ttu-id="c0e5e-124">IoT Device Provisioning Service Certificate 개체</span><span class="sxs-lookup"><span data-stu-id="c0e5e-124">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="c0e5e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c0e5e-125">-Name</span></span>
<span data-ttu-id="c0e5e-126">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="c0e5e-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c0e5e-127">-Path</span><span class="sxs-lookup"><span data-stu-id="c0e5e-127">-Path</span></span>
<span data-ttu-id="c0e5e-128">x509 인증서 .cer 파일 또는 .pem 파일 경로의 base-64 표현</span><span class="sxs-lookup"><span data-stu-id="c0e5e-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e5e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0e5e-129">-ResourceGroupName</span></span>
<span data-ttu-id="c0e5e-130">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="c0e5e-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c0e5e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0e5e-131">-ResourceId</span></span>
<span data-ttu-id="c0e5e-132">IoT Device Provisioning Service 인증서 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c0e5e-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="c0e5e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0e5e-133">-Confirm</span></span>
<span data-ttu-id="c0e5e-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0e5e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0e5e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0e5e-135">-WhatIf</span></span>
<span data-ttu-id="c0e5e-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c0e5e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0e5e-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0e5e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0e5e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e5e-138">CommonParameters</span></span>
<span data-ttu-id="c0e5e-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c0e5e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e5e-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c0e5e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e5e-141">입력</span><span class="sxs-lookup"><span data-stu-id="c0e5e-141">INPUTS</span></span>

### <span data-ttu-id="c0e5e-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="c0e5e-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="c0e5e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c0e5e-143">System.String</span></span>

## <span data-ttu-id="c0e5e-144">출력</span><span class="sxs-lookup"><span data-stu-id="c0e5e-144">OUTPUTS</span></span>

### <span data-ttu-id="c0e5e-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="c0e5e-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="c0e5e-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c0e5e-146">NOTES</span></span>

## <span data-ttu-id="c0e5e-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0e5e-147">RELATED LINKS</span></span>

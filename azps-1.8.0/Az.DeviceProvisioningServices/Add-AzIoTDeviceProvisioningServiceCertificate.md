---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 28c37988f25418e36b99b752a3be2e2ff923bbc7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700931"
---
# <span data-ttu-id="0c2be-101">Add-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="0c2be-101">Add-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="0c2be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c2be-102">SYNOPSIS</span></span>
<span data-ttu-id="0c2be-103">Azure IoT Hub 디바이스 프로비저닝 서비스 인증서를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c2be-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="0c2be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0c2be-104">SYNTAX</span></span>

### <span data-ttu-id="0c2be-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0c2be-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c2be-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0c2be-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c2be-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0c2be-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c2be-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0c2be-108">DESCRIPTION</span></span>
<span data-ttu-id="0c2be-109">새 인증서를 업로드 하거나 같은 이름으로 기존 인증서를 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="0c2be-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="0c2be-110">Azure IoT Hub Device 프로비저닝 서비스의 CA 인증서에 대 한 자세한 설명은을 참조 https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates 하세요.</span><span class="sxs-lookup"><span data-stu-id="0c2be-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="0c2be-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0c2be-111">EXAMPLES</span></span>

### <span data-ttu-id="0c2be-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="0c2be-112">Example 1</span></span>
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

<span data-ttu-id="0c2be-113">CA 인증서 CER 파일을 Azure IoT Hub 디바이스 프로비저닝 서비스에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c2be-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="0c2be-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="0c2be-114">Example 2</span></span>
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

<span data-ttu-id="0c2be-115">새 CER 파일을 업로드 하 여 IoT hub 디바이스 프로비저닝 서비스에서 CA 인증서를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c2be-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="0c2be-116">변수</span><span class="sxs-lookup"><span data-stu-id="0c2be-116">PARAMETERS</span></span>

### <span data-ttu-id="0c2be-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="0c2be-117">-CertificateName</span></span>
<span data-ttu-id="0c2be-118">Iot device 프로 비전 서비스 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c2be-118">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="0c2be-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c2be-119">-DefaultProfile</span></span>
<span data-ttu-id="0c2be-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c2be-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c2be-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="0c2be-121">-Etag</span></span>
<span data-ttu-id="0c2be-122">인증서의 Etag</span><span class="sxs-lookup"><span data-stu-id="0c2be-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="0c2be-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c2be-123">-InputObject</span></span>
<span data-ttu-id="0c2be-124">IoT Device 프로 비전 서비스 인증서 개체</span><span class="sxs-lookup"><span data-stu-id="0c2be-124">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="0c2be-125">-이름</span><span class="sxs-lookup"><span data-stu-id="0c2be-125">-Name</span></span>
<span data-ttu-id="0c2be-126">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="0c2be-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0c2be-127">-Path</span><span class="sxs-lookup"><span data-stu-id="0c2be-127">-Path</span></span>
<span data-ttu-id="0c2be-128">base-64에 대 한 X509 인증서 .cer 파일 또는 pem 파일 경로</span><span class="sxs-lookup"><span data-stu-id="0c2be-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="0c2be-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c2be-129">-ResourceGroupName</span></span>
<span data-ttu-id="0c2be-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c2be-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0c2be-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c2be-131">-ResourceId</span></span>
<span data-ttu-id="0c2be-132">IoT Device 프로 비전 서비스 인증서 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="0c2be-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="0c2be-133">-확인</span><span class="sxs-lookup"><span data-stu-id="0c2be-133">-Confirm</span></span>
<span data-ttu-id="0c2be-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c2be-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c2be-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c2be-135">-WhatIf</span></span>
<span data-ttu-id="0c2be-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c2be-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c2be-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c2be-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c2be-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c2be-138">CommonParameters</span></span>
<span data-ttu-id="0c2be-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c2be-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c2be-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c2be-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c2be-141">입력</span><span class="sxs-lookup"><span data-stu-id="0c2be-141">INPUTS</span></span>

### <span data-ttu-id="0c2be-142">DeviceProvisioningServices. PSCertificateResponse/. \*</span><span class="sxs-lookup"><span data-stu-id="0c2be-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="0c2be-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0c2be-143">System.String</span></span>

## <span data-ttu-id="0c2be-144">출력</span><span class="sxs-lookup"><span data-stu-id="0c2be-144">OUTPUTS</span></span>

### <span data-ttu-id="0c2be-145">DeviceProvisioningServices. PSCertificateResponse/. \*</span><span class="sxs-lookup"><span data-stu-id="0c2be-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="0c2be-146">상속자</span><span class="sxs-lookup"><span data-stu-id="0c2be-146">NOTES</span></span>

## <span data-ttu-id="0c2be-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c2be-147">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 659998a6a82c08ab57697767276e2357002a4182
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700910"
---
# <span data-ttu-id="578fa-101">Set-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="578fa-101">Set-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="578fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="578fa-102">SYNOPSIS</span></span>
<span data-ttu-id="578fa-103">Azure IoT Hub 디바이스 프로 비전 서비스 인증서를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="578fa-103">Verify an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="578fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="578fa-104">SYNTAX</span></span>

### <span data-ttu-id="578fa-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="578fa-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="578fa-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="578fa-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="578fa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="578fa-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="578fa-108">설명은</span><span class="sxs-lookup"><span data-stu-id="578fa-108">DESCRIPTION</span></span>
<span data-ttu-id="578fa-109">유효성 검사-코드 생성을 호출 하 여 얻은 확인 코드를 포함 하는 확인 인증서를 업로드 하 여 인증서를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="578fa-109">Verify a certificate by uploading a verification certificate containing the verification code obtained by calling generate-verification-code.</span></span> <span data-ttu-id="578fa-110">이는 소유 증명 프로세스의 마지막 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="578fa-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="578fa-111">Azure IoT Hub Device 프로비저닝 서비스의 CA 인증서에 대 한 자세한 설명은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span><span class="sxs-lookup"><span data-stu-id="578fa-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span></span>

## <span data-ttu-id="578fa-112">예제의</span><span class="sxs-lookup"><span data-stu-id="578fa-112">EXAMPLES</span></span>

### <span data-ttu-id="578fa-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="578fa-113">Example 1</span></span>
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

<span data-ttu-id="578fa-114">"Mycertificate" 개인 키의 소유권을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="578fa-114">Verify ownership of the "mycertificate" private key.</span></span>

### <span data-ttu-id="578fa-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="578fa-115">Example 2</span></span>
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

<span data-ttu-id="578fa-116">파이프라인을 사용 하 여 "mycertificate" 개인 키의 소유권을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="578fa-116">Verify ownership of the "mycertificate" private key using pipeline.</span></span>

## <span data-ttu-id="578fa-117">변수</span><span class="sxs-lookup"><span data-stu-id="578fa-117">PARAMETERS</span></span>

### <span data-ttu-id="578fa-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="578fa-118">-CertificateName</span></span>
<span data-ttu-id="578fa-119">Iot device 프로 비전 서비스 인증서의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="578fa-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="578fa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="578fa-120">-DefaultProfile</span></span>
<span data-ttu-id="578fa-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="578fa-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="578fa-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="578fa-122">-Etag</span></span>
<span data-ttu-id="578fa-123">인증서의 Etag</span><span class="sxs-lookup"><span data-stu-id="578fa-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="578fa-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="578fa-124">-InputObject</span></span>
<span data-ttu-id="578fa-125">IoT Device 프로 비전 서비스 인증서 개체</span><span class="sxs-lookup"><span data-stu-id="578fa-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="578fa-126">-이름</span><span class="sxs-lookup"><span data-stu-id="578fa-126">-Name</span></span>
<span data-ttu-id="578fa-127">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="578fa-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="578fa-128">-Path</span><span class="sxs-lookup"><span data-stu-id="578fa-128">-Path</span></span>
<span data-ttu-id="578fa-129">base-64에 대 한 X509 인증서 .cer 파일 또는 pem 파일 경로</span><span class="sxs-lookup"><span data-stu-id="578fa-129">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="578fa-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="578fa-130">-ResourceGroupName</span></span>
<span data-ttu-id="578fa-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="578fa-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="578fa-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="578fa-132">-ResourceId</span></span>
<span data-ttu-id="578fa-133">IoT Device 프로 비전 서비스 인증서 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="578fa-133">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="578fa-134">-확인</span><span class="sxs-lookup"><span data-stu-id="578fa-134">-Confirm</span></span>
<span data-ttu-id="578fa-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="578fa-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="578fa-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="578fa-136">-WhatIf</span></span>
<span data-ttu-id="578fa-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="578fa-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="578fa-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="578fa-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="578fa-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="578fa-139">CommonParameters</span></span>
<span data-ttu-id="578fa-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="578fa-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="578fa-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="578fa-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="578fa-142">입력</span><span class="sxs-lookup"><span data-stu-id="578fa-142">INPUTS</span></span>

### <span data-ttu-id="578fa-143">DeviceProvisioningServices. PSCertificateResponse/. \*</span><span class="sxs-lookup"><span data-stu-id="578fa-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="578fa-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="578fa-144">System.String</span></span>

## <span data-ttu-id="578fa-145">출력</span><span class="sxs-lookup"><span data-stu-id="578fa-145">OUTPUTS</span></span>

### <span data-ttu-id="578fa-146">DeviceProvisioningServices. PSCertificateResponse/. \*</span><span class="sxs-lookup"><span data-stu-id="578fa-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="578fa-147">상속자</span><span class="sxs-lookup"><span data-stu-id="578fa-147">NOTES</span></span>

## <span data-ttu-id="578fa-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="578fa-148">RELATED LINKS</span></span>

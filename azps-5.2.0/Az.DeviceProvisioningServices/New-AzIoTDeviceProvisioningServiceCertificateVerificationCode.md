---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 2822af07d4c33f80c5f748cddb4f70b6334a518c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328740"
---
# <span data-ttu-id="9157b-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="9157b-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="9157b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9157b-102">SYNOPSIS</span></span>
<span data-ttu-id="9157b-103">Azure IoT Hub Device Provisioning Service 인증서에 대한 확인 코드를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9157b-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="9157b-104">구문</span><span class="sxs-lookup"><span data-stu-id="9157b-104">SYNTAX</span></span>

### <span data-ttu-id="9157b-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9157b-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9157b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9157b-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9157b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9157b-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9157b-108">설명</span><span class="sxs-lookup"><span data-stu-id="9157b-108">DESCRIPTION</span></span>
<span data-ttu-id="9157b-109">이 확인 코드는 인증서에 대한 소유 증명 단계를 완료하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="9157b-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="9157b-110">루트 인증서 개인 키로 서명된 새 인증서의 CN으로 이 확인 코드를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9157b-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="9157b-111">Azure IoT Hub Device Provisioning Service의 CA 인증서에 대한 자세한 설명은 https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9157b-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="9157b-112">예제</span><span class="sxs-lookup"><span data-stu-id="9157b-112">EXAMPLES</span></span>

### <span data-ttu-id="9157b-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="9157b-113">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningServiceCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="9157b-114">"mycertificate"에 대한 확인 코드를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9157b-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="9157b-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="9157b-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | New-AzIoTDpsCVC

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="9157b-116">파이프라인을 사용하여 "mycertificate"에 대한 확인 코드를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9157b-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="9157b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9157b-117">PARAMETERS</span></span>

### <span data-ttu-id="9157b-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="9157b-118">-CertificateName</span></span>
<span data-ttu-id="9157b-119">Iot 디바이스 프로비전 서비스 인증서의 이름</span><span class="sxs-lookup"><span data-stu-id="9157b-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="9157b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9157b-120">-DefaultProfile</span></span>
<span data-ttu-id="9157b-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9157b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9157b-122">-Etag</span><span class="sxs-lookup"><span data-stu-id="9157b-122">-Etag</span></span>
<span data-ttu-id="9157b-123">인증서의 Etag</span><span class="sxs-lookup"><span data-stu-id="9157b-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="9157b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9157b-124">-InputObject</span></span>
<span data-ttu-id="9157b-125">IoT Device Provisioning Service Certificate 개체</span><span class="sxs-lookup"><span data-stu-id="9157b-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="9157b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9157b-126">-Name</span></span>
<span data-ttu-id="9157b-127">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="9157b-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9157b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9157b-128">-ResourceGroupName</span></span>
<span data-ttu-id="9157b-129">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="9157b-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9157b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9157b-130">-ResourceId</span></span>
<span data-ttu-id="9157b-131">IoT Device Provisioning Service 인증서 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9157b-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="9157b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9157b-132">-Confirm</span></span>
<span data-ttu-id="9157b-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9157b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9157b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9157b-134">-WhatIf</span></span>
<span data-ttu-id="9157b-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9157b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9157b-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9157b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9157b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9157b-137">CommonParameters</span></span>
<span data-ttu-id="9157b-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9157b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9157b-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9157b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9157b-140">입력</span><span class="sxs-lookup"><span data-stu-id="9157b-140">INPUTS</span></span>

### <span data-ttu-id="9157b-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="9157b-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="9157b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9157b-142">System.String</span></span>

## <span data-ttu-id="9157b-143">출력</span><span class="sxs-lookup"><span data-stu-id="9157b-143">OUTPUTS</span></span>

### <span data-ttu-id="9157b-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="9157b-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="9157b-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9157b-145">NOTES</span></span>

## <span data-ttu-id="9157b-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9157b-146">RELATED LINKS</span></span>

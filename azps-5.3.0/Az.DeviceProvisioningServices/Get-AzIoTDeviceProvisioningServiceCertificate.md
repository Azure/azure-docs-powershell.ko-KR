---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: aa51001163e4559dd0d3ef7edfb48abd3448c0b6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492018"
---
# <span data-ttu-id="c4634-101">Get-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="c4634-101">Get-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="c4634-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4634-102">SYNOPSIS</span></span>
<span data-ttu-id="c4634-103">Azure IoT Hub Device Provisioning Service 내에 포함된 모든 인증서 또는 특정 인증서를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c4634-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="c4634-104">구문</span><span class="sxs-lookup"><span data-stu-id="c4634-104">SYNTAX</span></span>

### <span data-ttu-id="c4634-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c4634-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4634-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c4634-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4634-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c4634-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4634-108">설명</span><span class="sxs-lookup"><span data-stu-id="c4634-108">DESCRIPTION</span></span>
<span data-ttu-id="c4634-109">Azure IoT Hub Device Provisioning Service의 CA 인증서에 대한 자세한 설명은 https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c4634-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="c4634-110">예제</span><span class="sxs-lookup"><span data-stu-id="c4634-110">EXAMPLES</span></span>

### <span data-ttu-id="c4634-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c4634-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate"

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

<span data-ttu-id="c4634-112">Azure IoT Hub 디바이스 프로비저닝 서비스에서 "mycertificate"에 대한 세부 정보를 보여 니다.</span><span class="sxs-lookup"><span data-stu-id="c4634-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="c4634-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c4634-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="c4634-114">파이프라인을 사용하여 "myiotdps"의 모든 인증서를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c4634-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="c4634-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4634-115">PARAMETERS</span></span>

### <span data-ttu-id="c4634-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c4634-116">-CertificateName</span></span>
<span data-ttu-id="c4634-117">인증서의 이름</span><span class="sxs-lookup"><span data-stu-id="c4634-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="c4634-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4634-118">-DefaultProfile</span></span>
<span data-ttu-id="c4634-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4634-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4634-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="c4634-120">-DpsObject</span></span>
<span data-ttu-id="c4634-121">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="c4634-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c4634-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c4634-122">-Name</span></span>
<span data-ttu-id="c4634-123">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="c4634-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c4634-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4634-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4634-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="c4634-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c4634-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4634-126">-ResourceId</span></span>
<span data-ttu-id="c4634-127">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c4634-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c4634-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4634-128">CommonParameters</span></span>
<span data-ttu-id="c4634-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c4634-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4634-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c4634-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4634-131">입력</span><span class="sxs-lookup"><span data-stu-id="c4634-131">INPUTS</span></span>

### <span data-ttu-id="c4634-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c4634-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="c4634-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c4634-133">System.String</span></span>

## <span data-ttu-id="c4634-134">출력</span><span class="sxs-lookup"><span data-stu-id="c4634-134">OUTPUTS</span></span>

### <span data-ttu-id="c4634-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="c4634-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="c4634-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c4634-136">NOTES</span></span>

## <span data-ttu-id="c4634-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4634-137">RELATED LINKS</span></span>

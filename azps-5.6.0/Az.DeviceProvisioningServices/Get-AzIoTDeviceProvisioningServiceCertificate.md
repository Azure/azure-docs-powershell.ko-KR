---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 788759abe543d3bddf3c67abe2ed37aafca6be3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978544"
---
# <span data-ttu-id="2d113-101">Get-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="2d113-101">Get-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="2d113-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d113-102">SYNOPSIS</span></span>
<span data-ttu-id="2d113-103">Azure IoT Hub 디바이스 프로비전 서비스에 포함된 모든 인증서 또는 특정 인증서를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="2d113-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="2d113-104">구문</span><span class="sxs-lookup"><span data-stu-id="2d113-104">SYNTAX</span></span>

### <span data-ttu-id="2d113-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2d113-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d113-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2d113-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d113-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2d113-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d113-108">설명</span><span class="sxs-lookup"><span data-stu-id="2d113-108">DESCRIPTION</span></span>
<span data-ttu-id="2d113-109">Azure IoT Hub Device Provisioning Service의 CA 인증서에 대한 자세한 설명은 을 https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2d113-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="2d113-110">예제</span><span class="sxs-lookup"><span data-stu-id="2d113-110">EXAMPLES</span></span>

### <span data-ttu-id="2d113-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2d113-111">Example 1</span></span>
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

<span data-ttu-id="2d113-112">Azure IoT Hub 디바이스 프로비전 서비스에서 "mycertificate"에 대한 세부 정보를 보여 니다.</span><span class="sxs-lookup"><span data-stu-id="2d113-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="2d113-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="2d113-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="2d113-114">파이프라인을 사용하여 "myiotdps"에 모든 인증서를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="2d113-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="2d113-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2d113-115">PARAMETERS</span></span>

### <span data-ttu-id="2d113-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="2d113-116">-CertificateName</span></span>
<span data-ttu-id="2d113-117">인증서 이름</span><span class="sxs-lookup"><span data-stu-id="2d113-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="2d113-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d113-118">-DefaultProfile</span></span>
<span data-ttu-id="2d113-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d113-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d113-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="2d113-120">-DpsObject</span></span>
<span data-ttu-id="2d113-121">IoT 디바이스 프로비전 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="2d113-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="2d113-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2d113-122">-Name</span></span>
<span data-ttu-id="2d113-123">IoT 디바이스 프로비전 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="2d113-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2d113-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d113-124">-ResourceGroupName</span></span>
<span data-ttu-id="2d113-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="2d113-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2d113-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d113-126">-ResourceId</span></span>
<span data-ttu-id="2d113-127">IoT 디바이스 프로비전 서비스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="2d113-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2d113-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d113-128">CommonParameters</span></span>
<span data-ttu-id="2d113-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2d113-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d113-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2d113-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d113-131">입력</span><span class="sxs-lookup"><span data-stu-id="2d113-131">INPUTS</span></span>

### <span data-ttu-id="2d113-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2d113-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="2d113-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2d113-133">System.String</span></span>

## <span data-ttu-id="2d113-134">출력</span><span class="sxs-lookup"><span data-stu-id="2d113-134">OUTPUTS</span></span>

### <span data-ttu-id="2d113-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="2d113-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="2d113-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2d113-136">NOTES</span></span>

## <span data-ttu-id="2d113-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d113-137">RELATED LINKS</span></span>

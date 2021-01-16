---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 62f9a2d77ce3a5b34b25c98d681bcfba55ae62e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338277"
---
# <span data-ttu-id="96644-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="96644-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="96644-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96644-102">SYNOPSIS</span></span>
<span data-ttu-id="96644-103">Azure IoT Hub 디바이스 프로비전 서비스에서 연결된 IoT Hub의 세부 정보를 모두 나열하거나 세부 정보를 보여 주면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96644-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="96644-104">구문</span><span class="sxs-lookup"><span data-stu-id="96644-104">SYNTAX</span></span>

### <span data-ttu-id="96644-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="96644-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96644-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="96644-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96644-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="96644-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96644-108">설명</span><span class="sxs-lookup"><span data-stu-id="96644-108">DESCRIPTION</span></span>
<span data-ttu-id="96644-109">Azure IoT Hub Device Provisioning Service에 대한 소개는 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="96644-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="96644-110">예제</span><span class="sxs-lookup"><span data-stu-id="96644-110">EXAMPLES</span></span>

### <span data-ttu-id="96644-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="96644-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="96644-112">연결된 모든 IoT Hub를 "myiotdps"에 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="96644-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="96644-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="96644-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="96644-114">Azure IoT Hub 디바이스 프로비전 서비스에서 연결된 IoT Hub "myiothub1"에 대한 세부 정보를 보여 니다.</span><span class="sxs-lookup"><span data-stu-id="96644-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="96644-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96644-115">PARAMETERS</span></span>

### <span data-ttu-id="96644-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96644-116">-DefaultProfile</span></span>
<span data-ttu-id="96644-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96644-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96644-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="96644-118">-DpsObject</span></span>
<span data-ttu-id="96644-119">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="96644-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="96644-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="96644-120">-LinkedHubName</span></span>
<span data-ttu-id="96644-121">연결된 IoT Hub의 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="96644-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="96644-122">-Name</span><span class="sxs-lookup"><span data-stu-id="96644-122">-Name</span></span>
<span data-ttu-id="96644-123">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="96644-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="96644-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96644-124">-ResourceGroupName</span></span>
<span data-ttu-id="96644-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="96644-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="96644-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96644-126">-ResourceId</span></span>
<span data-ttu-id="96644-127">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="96644-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="96644-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96644-128">CommonParameters</span></span>
<span data-ttu-id="96644-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="96644-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96644-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="96644-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96644-131">입력</span><span class="sxs-lookup"><span data-stu-id="96644-131">INPUTS</span></span>

### <span data-ttu-id="96644-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="96644-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="96644-133">System.String</span><span class="sxs-lookup"><span data-stu-id="96644-133">System.String</span></span>

## <span data-ttu-id="96644-134">출력</span><span class="sxs-lookup"><span data-stu-id="96644-134">OUTPUTS</span></span>

### <span data-ttu-id="96644-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="96644-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="96644-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="96644-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="96644-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="96644-137">NOTES</span></span>

## <span data-ttu-id="96644-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96644-138">RELATED LINKS</span></span>

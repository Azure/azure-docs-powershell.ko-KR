---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: 5aff957c16fa6fefb52706f70016092a37cdcb3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980443"
---
# <span data-ttu-id="40dae-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="40dae-101">Get-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="40dae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40dae-102">SYNOPSIS</span></span>
<span data-ttu-id="40dae-103">Azure IoT Hub 디바이스 프로비전 서비스에 연결된 IoT Hub의 세부 정보를 모두 나열하거나 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="40dae-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="40dae-104">구문</span><span class="sxs-lookup"><span data-stu-id="40dae-104">SYNTAX</span></span>

### <span data-ttu-id="40dae-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="40dae-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40dae-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="40dae-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40dae-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="40dae-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40dae-108">설명</span><span class="sxs-lookup"><span data-stu-id="40dae-108">DESCRIPTION</span></span>
<span data-ttu-id="40dae-109">Azure IoT Hub 디바이스 프로비전 서비스에 대한 소개는 https://docs.microsoft.com/azure/iot-dps/about-iot-dps 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="40dae-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="40dae-110">예제</span><span class="sxs-lookup"><span data-stu-id="40dae-110">EXAMPLES</span></span>

### <span data-ttu-id="40dae-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="40dae-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="40dae-112">연결된 모든 IoT 허브를 "myiotdps"에 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="40dae-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="40dae-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="40dae-113">Example 2</span></span>
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

<span data-ttu-id="40dae-114">Azure IoT Hub 디바이스 프로비전 서비스에서 연결된 IoT Hub "myiothub1"에 대한 세부 정보를 보여 니다.</span><span class="sxs-lookup"><span data-stu-id="40dae-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="40dae-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="40dae-115">PARAMETERS</span></span>

### <span data-ttu-id="40dae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40dae-116">-DefaultProfile</span></span>
<span data-ttu-id="40dae-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40dae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40dae-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="40dae-118">-DpsObject</span></span>
<span data-ttu-id="40dae-119">IoT 디바이스 프로비전 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="40dae-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="40dae-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="40dae-120">-LinkedHubName</span></span>
<span data-ttu-id="40dae-121">연결된 IoT Hub의 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="40dae-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="40dae-122">-Name</span><span class="sxs-lookup"><span data-stu-id="40dae-122">-Name</span></span>
<span data-ttu-id="40dae-123">IoT 디바이스 프로비전 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="40dae-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="40dae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40dae-124">-ResourceGroupName</span></span>
<span data-ttu-id="40dae-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="40dae-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="40dae-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40dae-126">-ResourceId</span></span>
<span data-ttu-id="40dae-127">IoT 디바이스 프로비전 서비스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="40dae-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="40dae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40dae-128">CommonParameters</span></span>
<span data-ttu-id="40dae-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="40dae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40dae-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="40dae-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40dae-131">입력</span><span class="sxs-lookup"><span data-stu-id="40dae-131">INPUTS</span></span>

### <span data-ttu-id="40dae-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="40dae-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="40dae-133">System.String</span><span class="sxs-lookup"><span data-stu-id="40dae-133">System.String</span></span>

## <span data-ttu-id="40dae-134">출력</span><span class="sxs-lookup"><span data-stu-id="40dae-134">OUTPUTS</span></span>

### <span data-ttu-id="40dae-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="40dae-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="40dae-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span><span class="sxs-lookup"><span data-stu-id="40dae-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="40dae-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="40dae-137">NOTES</span></span>

## <span data-ttu-id="40dae-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40dae-138">RELATED LINKS</span></span>

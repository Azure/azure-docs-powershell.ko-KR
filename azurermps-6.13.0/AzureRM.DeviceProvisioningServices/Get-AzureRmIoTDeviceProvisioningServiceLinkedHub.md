---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: bae363b984f148ff55f34eaa04b1ba85eaad4449
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524427"
---
# <span data-ttu-id="c5fd9-101">Get-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="c5fd9-101">Get-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="c5fd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="c5fd9-103">Azure IoT Hub device 프로비저닝 서비스의 연결 된 IoT hub에 대 한 세부 정보를 모두 나열 하거나 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-103">List all or show details of linked IoT hubs in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5fd9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c5fd9-104">SYNTAX</span></span>

### <span data-ttu-id="c5fd9-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c5fd9-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5fd9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c5fd9-106">InputObjectSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-DpsObject] <PSProvisioningServiceDescription>
 [-LinkedHubName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5fd9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c5fd9-107">ResourceIdSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5fd9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c5fd9-108">DESCRIPTION</span></span>
<span data-ttu-id="c5fd9-109">Azure IoT Hub Device 프로비저닝 서비스에 대 한 소개는를 참조 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 하세요.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="c5fd9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c5fd9-110">EXAMPLES</span></span>

### <span data-ttu-id="c5fd9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c5fd9-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps"

LinkedHubName                   Location    AllocationWeight    ApplyAllocationPolicy
-------------                   --------    ----------------    ---------------------
myiothub1.azure-devices.net     eastus      2
myiothub2.azure-devices.net     westus2                         true
```

<span data-ttu-id="c5fd9-112">"Myiotdps"에 연결 된 모든 IoT hub를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-112">List all linked IoT hubs in "myiotdps".</span></span>

### <span data-ttu-id="c5fd9-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c5fd9-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub1"

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub1.azure-devices.net
ConnectionString      : HostName=myiothub1.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 2
ApplyAllocationPolicy :
Location              : eastus
```

<span data-ttu-id="c5fd9-114">Azure IoT Hub 디바이스 프로비저닝 서비스에서 연결 된 IoT hub "myiothub1"의 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-114">Show details of linked IoT hub "myiothub1" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="c5fd9-115">변수</span><span class="sxs-lookup"><span data-stu-id="c5fd9-115">PARAMETERS</span></span>

### <span data-ttu-id="c5fd9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5fd9-116">-DefaultProfile</span></span>
<span data-ttu-id="c5fd9-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5fd9-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="c5fd9-118">-DpsObject</span></span>
<span data-ttu-id="c5fd9-119">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="c5fd9-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c5fd9-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="c5fd9-120">-LinkedHubName</span></span>
<span data-ttu-id="c5fd9-121">연결 된 IoT Hub의 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="c5fd9-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="c5fd9-122">-이름</span><span class="sxs-lookup"><span data-stu-id="c5fd9-122">-Name</span></span>
<span data-ttu-id="c5fd9-123">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="c5fd9-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c5fd9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5fd9-124">-ResourceGroupName</span></span>
<span data-ttu-id="c5fd9-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c5fd9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5fd9-126">-ResourceId</span></span>
<span data-ttu-id="c5fd9-127">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="c5fd9-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c5fd9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5fd9-128">CommonParameters</span></span>
<span data-ttu-id="c5fd9-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5fd9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5fd9-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5fd9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5fd9-131">입력</span><span class="sxs-lookup"><span data-stu-id="c5fd9-131">INPUTS</span></span>

### <span data-ttu-id="c5fd9-132">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="c5fd9-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="c5fd9-133">매개 변수: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c5fd9-133">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="c5fd9-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c5fd9-134">System.String</span></span>

## <span data-ttu-id="c5fd9-135">출력</span><span class="sxs-lookup"><span data-stu-id="c5fd9-135">OUTPUTS</span></span>

### <span data-ttu-id="c5fd9-136">DeviceProvisioningServices. PSIotHubDefinitionDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="c5fd9-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="c5fd9-137">DeviceProvisioningServices. PSIotHubDefinitions/. \*</span><span class="sxs-lookup"><span data-stu-id="c5fd9-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitions</span></span>

## <span data-ttu-id="c5fd9-138">상속자</span><span class="sxs-lookup"><span data-stu-id="c5fd9-138">NOTES</span></span>

## <span data-ttu-id="c5fd9-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5fd9-139">RELATED LINKS</span></span>

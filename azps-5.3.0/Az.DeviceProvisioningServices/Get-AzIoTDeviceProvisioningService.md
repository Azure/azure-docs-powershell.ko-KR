---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ab6dd43cff746d670fe05d66d983836433323728
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492020"
---
# <span data-ttu-id="a507a-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="a507a-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="a507a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a507a-102">SYNOPSIS</span></span>
<span data-ttu-id="a507a-103">Azure IoT Hub 디바이스 프로비전 서비스의 세부 정보를 모두 나열하거나 세부 정보를 보여 주거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="a507a-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="a507a-104">구문</span><span class="sxs-lookup"><span data-stu-id="a507a-104">SYNTAX</span></span>

### <span data-ttu-id="a507a-105">ListIotDpsByResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="a507a-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a507a-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="a507a-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a507a-107">설명</span><span class="sxs-lookup"><span data-stu-id="a507a-107">DESCRIPTION</span></span>
<span data-ttu-id="a507a-108">Azure IoT Hub Device Provisioning Service에 대한 소개는 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a507a-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="a507a-109">예제</span><span class="sxs-lookup"><span data-stu-id="a507a-109">EXAMPLES</span></span>

### <span data-ttu-id="a507a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a507a-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="a507a-111">구독의 모든 Azure IoT Hub 디바이스 프로비전 서비스를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="a507a-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="a507a-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="a507a-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="a507a-113">리소스 그룹 'myresourcegroup'에 모든 Azure IoT Hub 디바이스 프로비전 서비스를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="a507a-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="a507a-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="a507a-114">Example 3</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : eastus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="a507a-115">Azure IoT Hub 디바이스 프로비전 서비스 'myiotdps'에 대한 세부 정보를 보여 니다.</span><span class="sxs-lookup"><span data-stu-id="a507a-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="a507a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a507a-116">PARAMETERS</span></span>

### <span data-ttu-id="a507a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a507a-117">-DefaultProfile</span></span>
<span data-ttu-id="a507a-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a507a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a507a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a507a-119">-Name</span></span>
<span data-ttu-id="a507a-120">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="a507a-120">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a507a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a507a-121">-ResourceGroupName</span></span>
<span data-ttu-id="a507a-122">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="a507a-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotDpsByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a507a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a507a-123">CommonParameters</span></span>
<span data-ttu-id="a507a-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a507a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a507a-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a507a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a507a-126">입력</span><span class="sxs-lookup"><span data-stu-id="a507a-126">INPUTS</span></span>

### <span data-ttu-id="a507a-127">없음</span><span class="sxs-lookup"><span data-stu-id="a507a-127">None</span></span>

## <span data-ttu-id="a507a-128">출력</span><span class="sxs-lookup"><span data-stu-id="a507a-128">OUTPUTS</span></span>

### <span data-ttu-id="a507a-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="a507a-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="a507a-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a507a-130">NOTES</span></span>

## <span data-ttu-id="a507a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a507a-131">RELATED LINKS</span></span>

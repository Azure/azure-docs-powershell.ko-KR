---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ab6dd43cff746d670fe05d66d983836433323728
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215521"
---
# <span data-ttu-id="550f6-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="550f6-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="550f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="550f6-102">SYNOPSIS</span></span>
<span data-ttu-id="550f6-103">Azure IoT Hub 디바이스 프로비저닝 서비스의 모든 세부 정보를 나열 하거나 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="550f6-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="550f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="550f6-104">SYNTAX</span></span>

### <span data-ttu-id="550f6-105">ListIotDpsByResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="550f6-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="550f6-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="550f6-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="550f6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="550f6-107">DESCRIPTION</span></span>
<span data-ttu-id="550f6-108">Azure IoT Hub Device 프로비저닝 서비스에 대 한 소개는를 참조 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 하세요.</span><span class="sxs-lookup"><span data-stu-id="550f6-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="550f6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="550f6-109">EXAMPLES</span></span>

### <span data-ttu-id="550f6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="550f6-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="550f6-111">구독의 모든 Azure IoT Hub 디바이스 프로비저닝 서비스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="550f6-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="550f6-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="550f6-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="550f6-113">리소스 그룹 ' myresourcegroup '의 모든 Azure IoT Hub 디바이스 프로비저닝 서비스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="550f6-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="550f6-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="550f6-114">Example 3</span></span>
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

<span data-ttu-id="550f6-115">Azure IoT Hub device 프로비저닝 서비스 ' myiotdps '의 세부 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="550f6-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="550f6-116">변수</span><span class="sxs-lookup"><span data-stu-id="550f6-116">PARAMETERS</span></span>

### <span data-ttu-id="550f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="550f6-117">-DefaultProfile</span></span>
<span data-ttu-id="550f6-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="550f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="550f6-119">-이름</span><span class="sxs-lookup"><span data-stu-id="550f6-119">-Name</span></span>
<span data-ttu-id="550f6-120">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="550f6-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="550f6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="550f6-121">-ResourceGroupName</span></span>
<span data-ttu-id="550f6-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="550f6-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="550f6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="550f6-123">CommonParameters</span></span>
<span data-ttu-id="550f6-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="550f6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="550f6-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="550f6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="550f6-126">입력</span><span class="sxs-lookup"><span data-stu-id="550f6-126">INPUTS</span></span>

### <span data-ttu-id="550f6-127">않아야</span><span class="sxs-lookup"><span data-stu-id="550f6-127">None</span></span>

## <span data-ttu-id="550f6-128">출력</span><span class="sxs-lookup"><span data-stu-id="550f6-128">OUTPUTS</span></span>

### <span data-ttu-id="550f6-129">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="550f6-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="550f6-130">상속자</span><span class="sxs-lookup"><span data-stu-id="550f6-130">NOTES</span></span>

## <span data-ttu-id="550f6-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="550f6-131">RELATED LINKS</span></span>

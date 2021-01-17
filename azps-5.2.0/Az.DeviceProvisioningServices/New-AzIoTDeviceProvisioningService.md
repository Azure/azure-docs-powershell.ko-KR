---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 482acd4f82320bbc14c5bf95c113304a8720019b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340929"
---
# <span data-ttu-id="7c015-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="7c015-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="7c015-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c015-102">SYNOPSIS</span></span>
<span data-ttu-id="7c015-103">Azure IoT Hub 디바이스 프로비전 서비스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7c015-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="7c015-104">구문</span><span class="sxs-lookup"><span data-stu-id="7c015-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c015-105">설명</span><span class="sxs-lookup"><span data-stu-id="7c015-105">DESCRIPTION</span></span>
<span data-ttu-id="7c015-106">Azure IoT Hub Device Provisioning Service에 대한 소개는 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7c015-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="7c015-107">예제</span><span class="sxs-lookup"><span data-stu-id="7c015-107">EXAMPLES</span></span>

### <span data-ttu-id="7c015-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c015-108">Example 1</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag $tags

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {[key1, value1]}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="7c015-109">리소스 그룹의 지역에서 표준 가격 책정 계층 S1 및 태그를 사용하여 Azure IoT Hub 디바이스 프로비전 서비스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c015-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1 and tags, in the region of the resource group.</span></span>

### <span data-ttu-id="7c015-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="7c015-110">Example 2</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Location "eastus"

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
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="7c015-111">'eastus' 지역에 표준 가격 책정 계층 S1을 사용하여 Azure IoT Hub 디바이스 프로비전 서비스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c015-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="7c015-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c015-112">PARAMETERS</span></span>

### <span data-ttu-id="7c015-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="7c015-113">-AllocationPolicy</span></span>
<span data-ttu-id="7c015-114">IoT Device Provisioning Service 할당 정책</span><span class="sxs-lookup"><span data-stu-id="7c015-114">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c015-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c015-115">-DefaultProfile</span></span>
<span data-ttu-id="7c015-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c015-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c015-117">-Location</span><span class="sxs-lookup"><span data-stu-id="7c015-117">-Location</span></span>
<span data-ttu-id="7c015-118">위치</span><span class="sxs-lookup"><span data-stu-id="7c015-118">Location</span></span>

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

### <span data-ttu-id="7c015-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7c015-119">-Name</span></span>
<span data-ttu-id="7c015-120">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="7c015-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7c015-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c015-121">-ResourceGroupName</span></span>
<span data-ttu-id="7c015-122">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="7c015-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c015-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7c015-123">-SkuName</span></span>
<span data-ttu-id="7c015-124">SKU</span><span class="sxs-lookup"><span data-stu-id="7c015-124">Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: S1

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c015-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="7c015-125">-Tag</span></span>
<span data-ttu-id="7c015-126">IoT Device Provisioning Service 인스턴스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="7c015-126">IoT Device Provisioning Service instance tags.</span></span> <span data-ttu-id="7c015-127">해시 테이블 형식의 키-값 쌍에 있는 속성 바입니다.</span><span class="sxs-lookup"><span data-stu-id="7c015-127">Property bag in key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c015-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c015-128">-Confirm</span></span>
<span data-ttu-id="7c015-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c015-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c015-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c015-130">-WhatIf</span></span>
<span data-ttu-id="7c015-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7c015-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c015-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c015-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c015-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c015-133">CommonParameters</span></span>
<span data-ttu-id="7c015-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7c015-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c015-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7c015-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c015-136">입력</span><span class="sxs-lookup"><span data-stu-id="7c015-136">INPUTS</span></span>

### <span data-ttu-id="7c015-137">없음</span><span class="sxs-lookup"><span data-stu-id="7c015-137">None</span></span>

## <span data-ttu-id="7c015-138">출력</span><span class="sxs-lookup"><span data-stu-id="7c015-138">OUTPUTS</span></span>

### <span data-ttu-id="7c015-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="7c015-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="7c015-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7c015-140">NOTES</span></span>

## <span data-ttu-id="7c015-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c015-141">RELATED LINKS</span></span>

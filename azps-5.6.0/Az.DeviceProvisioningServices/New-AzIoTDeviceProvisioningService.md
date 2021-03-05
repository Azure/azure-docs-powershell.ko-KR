---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: bb6094644b9f2cbd831aa8d64a142d5888a5bcc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013648"
---
# <span data-ttu-id="1074b-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="1074b-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="1074b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1074b-102">SYNOPSIS</span></span>
<span data-ttu-id="1074b-103">Azure IoT Hub 디바이스 프로비전 서비스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1074b-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="1074b-104">구문</span><span class="sxs-lookup"><span data-stu-id="1074b-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1074b-105">설명</span><span class="sxs-lookup"><span data-stu-id="1074b-105">DESCRIPTION</span></span>
<span data-ttu-id="1074b-106">Azure IoT Hub 디바이스 프로비전 서비스에 대한 소개는 https://docs.microsoft.com/azure/iot-dps/about-iot-dps 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1074b-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="1074b-107">예제</span><span class="sxs-lookup"><span data-stu-id="1074b-107">EXAMPLES</span></span>

### <span data-ttu-id="1074b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1074b-108">Example 1</span></span>
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

<span data-ttu-id="1074b-109">리소스 그룹의 지역에서 표준 가격 책정 계층 S1 및 태그를 사용하여 Azure IoT Hub 디바이스 프로비전 서비스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1074b-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1 and tags, in the region of the resource group.</span></span>

### <span data-ttu-id="1074b-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="1074b-110">Example 2</span></span>
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

<span data-ttu-id="1074b-111">'eastus' 지역에서 표준 가격 책정 계층 S1을 사용하여 Azure IoT Hub 디바이스 프로비전 서비스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1074b-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="1074b-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1074b-112">PARAMETERS</span></span>

### <span data-ttu-id="1074b-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="1074b-113">-AllocationPolicy</span></span>
<span data-ttu-id="1074b-114">IoT 디바이스 프로비전 서비스 할당 정책</span><span class="sxs-lookup"><span data-stu-id="1074b-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="1074b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1074b-115">-DefaultProfile</span></span>
<span data-ttu-id="1074b-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1074b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1074b-117">-Location</span><span class="sxs-lookup"><span data-stu-id="1074b-117">-Location</span></span>
<span data-ttu-id="1074b-118">위치</span><span class="sxs-lookup"><span data-stu-id="1074b-118">Location</span></span>

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

### <span data-ttu-id="1074b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1074b-119">-Name</span></span>
<span data-ttu-id="1074b-120">IoT 디바이스 프로비전 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="1074b-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="1074b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1074b-121">-ResourceGroupName</span></span>
<span data-ttu-id="1074b-122">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="1074b-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1074b-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1074b-123">-SkuName</span></span>
<span data-ttu-id="1074b-124">Sku</span><span class="sxs-lookup"><span data-stu-id="1074b-124">Sku</span></span>

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

### <span data-ttu-id="1074b-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="1074b-125">-Tag</span></span>
<span data-ttu-id="1074b-126">IoT Device Provisioning Service 인스턴스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="1074b-126">IoT Device Provisioning Service instance tags.</span></span> <span data-ttu-id="1074b-127">해시 테이블의 키 값 쌍의 속성 가방입니다.</span><span class="sxs-lookup"><span data-stu-id="1074b-127">Property bag in key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="1074b-128">-확인</span><span class="sxs-lookup"><span data-stu-id="1074b-128">-Confirm</span></span>
<span data-ttu-id="1074b-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1074b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1074b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1074b-130">-WhatIf</span></span>
<span data-ttu-id="1074b-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1074b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1074b-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1074b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1074b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1074b-133">CommonParameters</span></span>
<span data-ttu-id="1074b-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1074b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1074b-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1074b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1074b-136">입력</span><span class="sxs-lookup"><span data-stu-id="1074b-136">INPUTS</span></span>

### <span data-ttu-id="1074b-137">없음</span><span class="sxs-lookup"><span data-stu-id="1074b-137">None</span></span>

## <span data-ttu-id="1074b-138">출력</span><span class="sxs-lookup"><span data-stu-id="1074b-138">OUTPUTS</span></span>

### <span data-ttu-id="1074b-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="1074b-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="1074b-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1074b-140">NOTES</span></span>

## <span data-ttu-id="1074b-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1074b-141">RELATED LINKS</span></span>

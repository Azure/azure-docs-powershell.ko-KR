---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: 9665b0ae486c12aec350db572aee6fc4f718ed43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529589"
---
# <span data-ttu-id="cb8f3-101">New-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="cb8f3-101">New-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="cb8f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="cb8f3-103">Azure IoT Hub 디바이스 프로비저닝 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cb8f3-103">Create an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb8f3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cb8f3-104">SYNTAX</span></span>

```
New-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb8f3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cb8f3-105">DESCRIPTION</span></span>
<span data-ttu-id="cb8f3-106">Azure IoT Hub Device 프로비저닝 서비스에 대 한 소개는를 참조 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 하세요.</span><span class="sxs-lookup"><span data-stu-id="cb8f3-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="cb8f3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cb8f3-107">EXAMPLES</span></span>

### <span data-ttu-id="cb8f3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cb8f3-108">Example 1</span></span>
```
PS C:\> New-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
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

<span data-ttu-id="cb8f3-109">표준 가격 책정 계층 S1 (리소스 그룹의 영역)을 사용 하 여 Azure IoT Hub 디바이스 프로 비전 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cb8f3-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="cb8f3-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="cb8f3-110">Example 2</span></span>
```
PS C:\> New-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Location "eastus"

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

<span data-ttu-id="cb8f3-111">' E us ' 지역에서 표준 가격 책정 계층 S1을 사용 하 여 Azure IoT Hub 디바이스 프로비저닝 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cb8f3-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="cb8f3-112">변수</span><span class="sxs-lookup"><span data-stu-id="cb8f3-112">PARAMETERS</span></span>

### <span data-ttu-id="cb8f3-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="cb8f3-113">-AllocationPolicy</span></span>
<span data-ttu-id="cb8f3-114">IoT Device 프로 비전 서비스 할당 정책</span><span class="sxs-lookup"><span data-stu-id="cb8f3-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="cb8f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb8f3-115">-DefaultProfile</span></span>
<span data-ttu-id="cb8f3-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb8f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb8f3-117">-위치</span><span class="sxs-lookup"><span data-stu-id="cb8f3-117">-Location</span></span>
<span data-ttu-id="cb8f3-118">Location</span><span class="sxs-lookup"><span data-stu-id="cb8f3-118">Location</span></span>

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

### <span data-ttu-id="cb8f3-119">-이름</span><span class="sxs-lookup"><span data-stu-id="cb8f3-119">-Name</span></span>
<span data-ttu-id="cb8f3-120">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="cb8f3-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="cb8f3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb8f3-121">-ResourceGroupName</span></span>
<span data-ttu-id="cb8f3-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cb8f3-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cb8f3-123">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="cb8f3-123">-SkuName</span></span>
<span data-ttu-id="cb8f3-124">제품</span><span class="sxs-lookup"><span data-stu-id="cb8f3-124">Sku</span></span>

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

### <span data-ttu-id="cb8f3-125">-확인</span><span class="sxs-lookup"><span data-stu-id="cb8f3-125">-Confirm</span></span>
<span data-ttu-id="cb8f3-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb8f3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb8f3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb8f3-127">-WhatIf</span></span>
<span data-ttu-id="cb8f3-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cb8f3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb8f3-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb8f3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb8f3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb8f3-130">CommonParameters</span></span>
<span data-ttu-id="cb8f3-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cb8f3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb8f3-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb8f3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb8f3-133">입력</span><span class="sxs-lookup"><span data-stu-id="cb8f3-133">INPUTS</span></span>

### <span data-ttu-id="cb8f3-134">않아야</span><span class="sxs-lookup"><span data-stu-id="cb8f3-134">None</span></span>

## <span data-ttu-id="cb8f3-135">출력</span><span class="sxs-lookup"><span data-stu-id="cb8f3-135">OUTPUTS</span></span>

### <span data-ttu-id="cb8f3-136">DeviceProvisioningServices. PSProvisioningServiceDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="cb8f3-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="cb8f3-137">상속자</span><span class="sxs-lookup"><span data-stu-id="cb8f3-137">NOTES</span></span>

## <span data-ttu-id="cb8f3-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb8f3-138">RELATED LINKS</span></span>

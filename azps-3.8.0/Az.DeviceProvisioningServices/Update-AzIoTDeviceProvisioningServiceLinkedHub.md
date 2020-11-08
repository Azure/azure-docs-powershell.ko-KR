---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: cc8d2ec0602213bdbfd50ac89e5199952cea424c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042342"
---
# <span data-ttu-id="87565-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="87565-101">Update-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="87565-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87565-102">SYNOPSIS</span></span>
<span data-ttu-id="87565-103">Azure IoT Hub 디바이스 프로비저닝 서비스에서 연결 된 IoT hub를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="87565-103">Update a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="87565-104">구문과</span><span class="sxs-lookup"><span data-stu-id="87565-104">SYNTAX</span></span>

### <span data-ttu-id="87565-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="87565-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-AllocationWeight <Int32>] [-ApplyAllocationPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87565-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="87565-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87565-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="87565-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-AllocationWeight <Int32>] [-ApplyAllocationPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87565-108">설명은</span><span class="sxs-lookup"><span data-stu-id="87565-108">DESCRIPTION</span></span>
<span data-ttu-id="87565-109">Azure IoT Hub Device 프로비저닝 서비스에 대 한 소개는를 참조 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 하세요.</span><span class="sxs-lookup"><span data-stu-id="87565-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="87565-110">예제의</span><span class="sxs-lookup"><span data-stu-id="87565-110">EXAMPLES</span></span>

### <span data-ttu-id="87565-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="87565-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -AllocationWeight 10 -ApplyAllocationPolicy $true

ResourceGroupName     : myresourcegroup
Name                  : myiotdps
LinkedHubName         : myiothub.azure-devices.net
ConnectionString      : HostName=myiothub.azure-devices.net;SharedAccessKeyName=iothubowner;SharedAccessKey=****
AllocationWeight      : 10
ApplyAllocationPolicy : True
Location              : eastus
```

<span data-ttu-id="87565-112">Azure IoT Hub 디바이스 프로비저닝 서비스에서 연결 된 IoT hub "myiothub.azure-devices.net"를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="87565-112">Update linked IoT hub "myiothub.azure-devices.net" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="87565-113">변수</span><span class="sxs-lookup"><span data-stu-id="87565-113">PARAMETERS</span></span>

### <span data-ttu-id="87565-114">-AllocationWeight</span><span class="sxs-lookup"><span data-stu-id="87565-114">-AllocationWeight</span></span>
<span data-ttu-id="87565-115">IoT Hub의 할당 중량</span><span class="sxs-lookup"><span data-stu-id="87565-115">Allocation weight of the IoT Hub</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87565-116">-ApplyAllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="87565-116">-ApplyAllocationPolicy</span></span>
<span data-ttu-id="87565-117">IoT Hub에 할당 정책 적용</span><span class="sxs-lookup"><span data-stu-id="87565-117">Apply allocation policy to the IoT Hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87565-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87565-118">-DefaultProfile</span></span>
<span data-ttu-id="87565-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="87565-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87565-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87565-120">-InputObject</span></span>
<span data-ttu-id="87565-121">IoT Device 프로비저닝 서비스 개체</span><span class="sxs-lookup"><span data-stu-id="87565-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87565-122">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="87565-122">-LinkedHubName</span></span>
<span data-ttu-id="87565-123">연결 된 IoT Hub의 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="87565-123">Host name of linked IoT Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87565-124">-이름</span><span class="sxs-lookup"><span data-stu-id="87565-124">-Name</span></span>
<span data-ttu-id="87565-125">IoT Device 프로비저닝 서비스의 이름</span><span class="sxs-lookup"><span data-stu-id="87565-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="87565-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87565-126">-ResourceGroupName</span></span>
<span data-ttu-id="87565-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87565-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="87565-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87565-128">-ResourceId</span></span>
<span data-ttu-id="87565-129">IoT Device 프로 비전 서비스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="87565-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="87565-130">-확인</span><span class="sxs-lookup"><span data-stu-id="87565-130">-Confirm</span></span>
<span data-ttu-id="87565-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="87565-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87565-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87565-132">-WhatIf</span></span>
<span data-ttu-id="87565-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="87565-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87565-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87565-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87565-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87565-135">CommonParameters</span></span>
<span data-ttu-id="87565-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="87565-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87565-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87565-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87565-138">입력</span><span class="sxs-lookup"><span data-stu-id="87565-138">INPUTS</span></span>

### <span data-ttu-id="87565-139">DeviceProvisioningServices. PSIotHubDefinitionDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="87565-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="87565-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="87565-140">System.String</span></span>

## <span data-ttu-id="87565-141">출력</span><span class="sxs-lookup"><span data-stu-id="87565-141">OUTPUTS</span></span>

### <span data-ttu-id="87565-142">DeviceProvisioningServices. PSIotHubDefinitionDescription/. \*</span><span class="sxs-lookup"><span data-stu-id="87565-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

## <span data-ttu-id="87565-143">상속자</span><span class="sxs-lookup"><span data-stu-id="87565-143">NOTES</span></span>

## <span data-ttu-id="87565-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87565-144">RELATED LINKS</span></span>

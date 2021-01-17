---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 4701070ae7810b86ff7567f73b39606909d7fa10
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340946"
---
# <span data-ttu-id="396e5-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="396e5-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="396e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="396e5-102">SYNOPSIS</span></span>
<span data-ttu-id="396e5-103">Azure IoT Hub 디바이스 프로비전 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="396e5-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="396e5-104">구문</span><span class="sxs-lookup"><span data-stu-id="396e5-104">SYNTAX</span></span>

### <span data-ttu-id="396e5-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="396e5-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="396e5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="396e5-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="396e5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="396e5-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="396e5-108">설명</span><span class="sxs-lookup"><span data-stu-id="396e5-108">DESCRIPTION</span></span>
<span data-ttu-id="396e5-109">Azure IoT Hub Device Provisioning Service에 대한 소개는 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="396e5-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="396e5-110">예제</span><span class="sxs-lookup"><span data-stu-id="396e5-110">EXAMPLES</span></span>

### <span data-ttu-id="396e5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="396e5-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="396e5-112">Azure IoT Hub 디바이스 프로비전 서비스 'myiotdps'를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="396e5-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="396e5-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="396e5-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="396e5-114">파이프라인을 사용하여 Azure IoT Hub 디바이스 프로비전 서비스 'myiotdps'를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="396e5-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="396e5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="396e5-115">PARAMETERS</span></span>

### <span data-ttu-id="396e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="396e5-116">-DefaultProfile</span></span>
<span data-ttu-id="396e5-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="396e5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="396e5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="396e5-118">-InputObject</span></span>
<span data-ttu-id="396e5-119">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="396e5-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="396e5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="396e5-120">-Name</span></span>
<span data-ttu-id="396e5-121">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="396e5-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="396e5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="396e5-122">-PassThru</span></span>
<span data-ttu-id="396e5-123">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="396e5-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="396e5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="396e5-124">-ResourceGroupName</span></span>
<span data-ttu-id="396e5-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="396e5-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="396e5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="396e5-126">-ResourceId</span></span>
<span data-ttu-id="396e5-127">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="396e5-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="396e5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="396e5-128">-Confirm</span></span>
<span data-ttu-id="396e5-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="396e5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="396e5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="396e5-130">-WhatIf</span></span>
<span data-ttu-id="396e5-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="396e5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="396e5-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="396e5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="396e5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="396e5-133">CommonParameters</span></span>
<span data-ttu-id="396e5-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="396e5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="396e5-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="396e5-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="396e5-136">입력</span><span class="sxs-lookup"><span data-stu-id="396e5-136">INPUTS</span></span>

### <span data-ttu-id="396e5-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="396e5-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="396e5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="396e5-138">System.String</span></span>

## <span data-ttu-id="396e5-139">출력</span><span class="sxs-lookup"><span data-stu-id="396e5-139">OUTPUTS</span></span>

### <span data-ttu-id="396e5-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="396e5-140">System.Boolean</span></span>

## <span data-ttu-id="396e5-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="396e5-141">NOTES</span></span>

## <span data-ttu-id="396e5-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="396e5-142">RELATED LINKS</span></span>

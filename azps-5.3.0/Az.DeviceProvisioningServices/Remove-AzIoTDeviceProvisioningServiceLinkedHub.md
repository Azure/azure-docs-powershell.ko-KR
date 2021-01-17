---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: b4ff0c778eb5185623160f977cdbecbaa0d85994
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376951"
---
# <span data-ttu-id="8fbc1-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="8fbc1-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="8fbc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fbc1-102">SYNOPSIS</span></span>
<span data-ttu-id="8fbc1-103">Azure IoT Hub 디바이스 프로비전 서비스에서 연결된 IoT Hub를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="8fbc1-104">구문</span><span class="sxs-lookup"><span data-stu-id="8fbc1-104">SYNTAX</span></span>

### <span data-ttu-id="8fbc1-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8fbc1-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8fbc1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8fbc1-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fbc1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8fbc1-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fbc1-108">설명</span><span class="sxs-lookup"><span data-stu-id="8fbc1-108">DESCRIPTION</span></span>
<span data-ttu-id="8fbc1-109">Azure IoT Hub Device Provisioning Service에 대한 소개는 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 다음을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="8fbc1-110">예제</span><span class="sxs-lookup"><span data-stu-id="8fbc1-110">EXAMPLES</span></span>

### <span data-ttu-id="8fbc1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8fbc1-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="8fbc1-112">Azure IoT Hub 디바이스 프로비전 서비스에서 연결된 IoT Hub "myiothub"를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="8fbc1-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="8fbc1-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="8fbc1-114">파이프라인을 사용하여 Azure IoT Hub 디바이스 프로비전 서비스에서 연결된 IoT Hub "myiothub"를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="8fbc1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fbc1-115">PARAMETERS</span></span>

### <span data-ttu-id="8fbc1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fbc1-116">-DefaultProfile</span></span>
<span data-ttu-id="8fbc1-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fbc1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fbc1-118">-InputObject</span></span>
<span data-ttu-id="8fbc1-119">IoT Device Provisioning Service 개체</span><span class="sxs-lookup"><span data-stu-id="8fbc1-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="8fbc1-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="8fbc1-120">-LinkedHubName</span></span>
<span data-ttu-id="8fbc1-121">연결된 IoT Hub의 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="8fbc1-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="8fbc1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8fbc1-122">-Name</span></span>
<span data-ttu-id="8fbc1-123">IoT Device Provisioning Service의 이름</span><span class="sxs-lookup"><span data-stu-id="8fbc1-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="8fbc1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8fbc1-124">-PassThru</span></span>
<span data-ttu-id="8fbc1-125">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="8fbc1-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8fbc1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fbc1-126">-ResourceGroupName</span></span>
<span data-ttu-id="8fbc1-127">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="8fbc1-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8fbc1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fbc1-128">-ResourceId</span></span>
<span data-ttu-id="8fbc1-129">IoT Device Provisioning Service 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="8fbc1-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="8fbc1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fbc1-130">-Confirm</span></span>
<span data-ttu-id="8fbc1-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fbc1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fbc1-132">-WhatIf</span></span>
<span data-ttu-id="8fbc1-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8fbc1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fbc1-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fbc1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fbc1-135">CommonParameters</span></span>
<span data-ttu-id="8fbc1-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fbc1-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8fbc1-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fbc1-138">입력</span><span class="sxs-lookup"><span data-stu-id="8fbc1-138">INPUTS</span></span>

### <span data-ttu-id="8fbc1-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="8fbc1-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="8fbc1-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8fbc1-140">System.String</span></span>

## <span data-ttu-id="8fbc1-141">출력</span><span class="sxs-lookup"><span data-stu-id="8fbc1-141">OUTPUTS</span></span>

### <span data-ttu-id="8fbc1-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8fbc1-142">System.Boolean</span></span>

## <span data-ttu-id="8fbc1-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8fbc1-143">NOTES</span></span>

## <span data-ttu-id="8fbc1-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8fbc1-144">RELATED LINKS</span></span>

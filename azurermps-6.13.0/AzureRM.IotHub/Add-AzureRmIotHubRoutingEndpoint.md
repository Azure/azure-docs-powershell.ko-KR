---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: d251d3159111437cd06880a49069aee7aca6d80f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529567"
---
# <span data-ttu-id="cddcc-101">Add-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="cddcc-101">Add-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="cddcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cddcc-102">SYNOPSIS</span></span>
<span data-ttu-id="cddcc-103">IoT Hub에 끝점 추가</span><span class="sxs-lookup"><span data-stu-id="cddcc-103">Add an endpoint to your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cddcc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cddcc-104">SYNTAX</span></span>

### <span data-ttu-id="cddcc-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="cddcc-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cddcc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cddcc-106">InputObjectSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cddcc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cddcc-107">ResourceIdSet</span></span>
```
Add-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String>
 [-EndpointType] <PSEndpointType> [-EndpointResourceGroup] <String> [-EndpointSubscriptionId] <String>
 [-ConnectionString] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cddcc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cddcc-108">DESCRIPTION</span></span>
<span data-ttu-id="cddcc-109">IoT Hub에 새 끝점을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cddcc-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="cddcc-110">지원 되는 끝점에 대 한 자세한 내용은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="cddcc-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="cddcc-111">예제의</span><span class="sxs-lookup"><span data-stu-id="cddcc-111">EXAMPLES</span></span>

### <span data-ttu-id="cddcc-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="cddcc-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="cddcc-113">"Myiothub" IoT Hub에 EventHub 유형의 새 끝점 "E2"를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cddcc-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="cddcc-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="cddcc-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : avro
```

<span data-ttu-id="cddcc-115">"Myiothub" IoT Hub에 AzureStorageContainer 유형의 새 끝점 "S1"을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cddcc-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="cddcc-116">변수</span><span class="sxs-lookup"><span data-stu-id="cddcc-116">PARAMETERS</span></span>

### <span data-ttu-id="cddcc-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="cddcc-117">-ConnectionString</span></span>
<span data-ttu-id="cddcc-118">라우팅 끝점의 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="cddcc-118">Connection string of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddcc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cddcc-119">-DefaultProfile</span></span>
<span data-ttu-id="cddcc-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cddcc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cddcc-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cddcc-121">-EndpointName</span></span>
<span data-ttu-id="cddcc-122">라우팅 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cddcc-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="cddcc-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cddcc-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="cddcc-124">끝점 resoure의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="cddcc-124">Resource group of the Endpoint resoure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddcc-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cddcc-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="cddcc-126">끝점 리소스의 SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cddcc-126">SubscriptionId of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddcc-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="cddcc-127">-EndpointType</span></span>
<span data-ttu-id="cddcc-128">라우팅 끝점의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="cddcc-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cddcc-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cddcc-129">-InputObject</span></span>
<span data-ttu-id="cddcc-130">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="cddcc-130">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cddcc-131">-이름</span><span class="sxs-lookup"><span data-stu-id="cddcc-131">-Name</span></span>
<span data-ttu-id="cddcc-132">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="cddcc-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cddcc-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cddcc-133">-ResourceGroupName</span></span>
<span data-ttu-id="cddcc-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cddcc-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cddcc-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cddcc-135">-ResourceId</span></span>
<span data-ttu-id="cddcc-136">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="cddcc-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cddcc-137">-확인</span><span class="sxs-lookup"><span data-stu-id="cddcc-137">-Confirm</span></span>
<span data-ttu-id="cddcc-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cddcc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cddcc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cddcc-139">-WhatIf</span></span>
<span data-ttu-id="cddcc-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cddcc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cddcc-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cddcc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cddcc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cddcc-142">CommonParameters</span></span>
<span data-ttu-id="cddcc-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cddcc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cddcc-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cddcc-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cddcc-145">입력</span><span class="sxs-lookup"><span data-stu-id="cddcc-145">INPUTS</span></span>

### <span data-ttu-id="cddcc-146">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="cddcc-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="cddcc-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cddcc-147">System.String</span></span>

## <span data-ttu-id="cddcc-148">출력</span><span class="sxs-lookup"><span data-stu-id="cddcc-148">OUTPUTS</span></span>

### <span data-ttu-id="cddcc-149">IotHub. PSRoutingEventHubEndpoint/. \*</span><span class="sxs-lookup"><span data-stu-id="cddcc-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="cddcc-150">IotHub. Psroutingservicebusendpoint 끝점 Microsoft Azure. IotHub.. w a m. Service라우팅. IotHub. \*. \*. \* \*. \* \*. \* PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cddcc-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="cddcc-151">상속자</span><span class="sxs-lookup"><span data-stu-id="cddcc-151">NOTES</span></span>

## <span data-ttu-id="cddcc-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cddcc-152">RELATED LINKS</span></span>

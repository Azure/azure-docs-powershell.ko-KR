---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 8b3d139d822452231451a1f07907ac20cdf3589c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495361"
---
# <span data-ttu-id="86dc1-101">Get-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="86dc1-101">Get-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="86dc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86dc1-102">SYNOPSIS</span></span>
<span data-ttu-id="86dc1-103">IoT Hub에 대한 모든 엔드포인트에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="86dc1-103">Get information on all the endpoints for your IoT Hub</span></span>

## <span data-ttu-id="86dc1-104">구문</span><span class="sxs-lookup"><span data-stu-id="86dc1-104">SYNTAX</span></span>

### <span data-ttu-id="86dc1-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="86dc1-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointType <PSEndpointType>]
 [-EndpointName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86dc1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="86dc1-106">InputObjectSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86dc1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="86dc1-107">ResourceIdSet</span></span>
```
Get-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointType <PSEndpointType>] [-EndpointName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86dc1-108">설명</span><span class="sxs-lookup"><span data-stu-id="86dc1-108">DESCRIPTION</span></span>
<span data-ttu-id="86dc1-109">엔드포인트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="86dc1-109">Get information on the endpoint.</span></span>

## <span data-ttu-id="86dc1-110">예제</span><span class="sxs-lookup"><span data-stu-id="86dc1-110">EXAMPLES</span></span>

### <span data-ttu-id="86dc1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="86dc1-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub"

Name EndpointType           AzureResource
---- ------------           -------------
E1   EventHub               resourcegroup1/event1
E2   EventHub               resourcegroup1/event2
S1   AzureStorageContainer  mystorage1/container
```

<span data-ttu-id="86dc1-112">"myiothub" IoT Hub에서 모든 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="86dc1-112">Get all the endpoints from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="86dc1-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="86dc1-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName SubscriptionId                       EndpointName
----------------- --------------                       ------------
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E1
resourcegroup1    91d12343-a3de-345d-b2ea-135792468abc E2
```

<span data-ttu-id="86dc1-114">"myiothub" IoT Hub에서 EventHub 유형의 모든 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="86dc1-114">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span> 

### <span data-ttu-id="86dc1-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="86dc1-115">Example 3</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointType EventHub

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="86dc1-116">"myiothub" IoT Hub에서 EventHub 유형의 모든 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="86dc1-116">Get all the endpoints of type EventHub from "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="86dc1-117">예제 4</span><span class="sxs-lookup"><span data-stu-id="86dc1-117">Example 4</span></span>
```
PS C:\> Get-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E1

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E1
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="86dc1-118">"myiothub" IoT Hub에서 엔드포인트 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="86dc1-118">Get an endpoint information from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="86dc1-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86dc1-119">PARAMETERS</span></span>

### <span data-ttu-id="86dc1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86dc1-120">-DefaultProfile</span></span>
<span data-ttu-id="86dc1-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86dc1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86dc1-122">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="86dc1-122">-EndpointName</span></span>
<span data-ttu-id="86dc1-123">라우팅 엔드포인트의 이름</span><span class="sxs-lookup"><span data-stu-id="86dc1-123">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="86dc1-124">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="86dc1-124">-EndpointType</span></span>
<span data-ttu-id="86dc1-125">라우팅 엔드포인트의 유형</span><span class="sxs-lookup"><span data-stu-id="86dc1-125">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86dc1-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86dc1-126">-InputObject</span></span>
<span data-ttu-id="86dc1-127">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="86dc1-127">IotHub Object</span></span>

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

### <span data-ttu-id="86dc1-128">-Name</span><span class="sxs-lookup"><span data-stu-id="86dc1-128">-Name</span></span>
<span data-ttu-id="86dc1-129">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="86dc1-129">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="86dc1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86dc1-130">-ResourceGroupName</span></span>
<span data-ttu-id="86dc1-131">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="86dc1-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="86dc1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86dc1-132">-ResourceId</span></span>
<span data-ttu-id="86dc1-133">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="86dc1-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="86dc1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86dc1-134">CommonParameters</span></span>
<span data-ttu-id="86dc1-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="86dc1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86dc1-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="86dc1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86dc1-137">입력</span><span class="sxs-lookup"><span data-stu-id="86dc1-137">INPUTS</span></span>

### <span data-ttu-id="86dc1-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="86dc1-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="86dc1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="86dc1-139">System.String</span></span>

## <span data-ttu-id="86dc1-140">출력</span><span class="sxs-lookup"><span data-stu-id="86dc1-140">OUTPUTS</span></span>

### <span data-ttu-id="86dc1-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="86dc1-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="86dc1-142">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="86dc1-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.PowerShell.Cmdlets.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="86dc1-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="86dc1-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="86dc1-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span><span class="sxs-lookup"><span data-stu-id="86dc1-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties[]</span></span>

### <span data-ttu-id="86dc1-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="86dc1-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="86dc1-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span><span class="sxs-lookup"><span data-stu-id="86dc1-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties[]</span></span>

### <span data-ttu-id="86dc1-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="86dc1-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

### <span data-ttu-id="86dc1-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span><span class="sxs-lookup"><span data-stu-id="86dc1-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties[]</span></span>

### <span data-ttu-id="86dc1-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span><span class="sxs-lookup"><span data-stu-id="86dc1-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint[]</span></span>

## <span data-ttu-id="86dc1-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="86dc1-150">NOTES</span></span>

## <span data-ttu-id="86dc1-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86dc1-151">RELATED LINKS</span></span>

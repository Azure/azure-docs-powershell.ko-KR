---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 74ec300e1189cd93ac29fba917ee44590da0d650
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988218"
---
# <span data-ttu-id="9398d-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="9398d-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="9398d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9398d-102">SYNOPSIS</span></span>
<span data-ttu-id="9398d-103">IoT Hub에 엔드포인트 추가</span><span class="sxs-lookup"><span data-stu-id="9398d-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="9398d-104">구문</span><span class="sxs-lookup"><span data-stu-id="9398d-104">SYNTAX</span></span>

### <span data-ttu-id="9398d-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9398d-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9398d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9398d-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9398d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9398d-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9398d-108">설명</span><span class="sxs-lookup"><span data-stu-id="9398d-108">DESCRIPTION</span></span>
<span data-ttu-id="9398d-109">IoT Hub에 새 엔드포인트를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9398d-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="9398d-110">지원되는 엔드포인트에 대한 자세한 내용은 https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="9398d-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="9398d-111">예제</span><span class="sxs-lookup"><span data-stu-id="9398d-111">EXAMPLES</span></span>

### <span data-ttu-id="9398d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9398d-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="9398d-113">"myiothub" IoT Hub에 EventHub 형식의 새 엔드포인트 "E2"를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9398d-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="9398d-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="9398d-114">Example 2</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName S1 -EndpointType AzureStorageContainer -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'DefaultEndpointsProtocol=https;AccountName=mystorage1;AccountKey=*****;EndpointSuffix=core.windows.net' -ContainerName container -Encoding json

ResourceGroupName       : resourcegroup1
SubscriptionId          : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName            : S1
ContainerName           : container
ConnectionString        : DefaultEndpointsProtocol=https;EndpointSuffix=core.windows.net;AccountName=mystorage1;AccountKey=****
FileNameFormat          : {iothub}/{partition}/{YYYY}/{MM}/{DD}/{HH}/{mm}
BatchFrequencyInSeconds : 300
MaxChunkSizeInBytes     : 314572800
Encoding                : json
```

<span data-ttu-id="9398d-115">"myiothub" IoT Hub에 AzureStorageContainer 형식의 새 엔드포인트 "S1"을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9398d-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="9398d-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9398d-116">PARAMETERS</span></span>

### <span data-ttu-id="9398d-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="9398d-117">-ConnectionString</span></span>
<span data-ttu-id="9398d-118">라우팅 엔드포인트의 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="9398d-118">Connection string of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9398d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9398d-119">-DefaultProfile</span></span>
<span data-ttu-id="9398d-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9398d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9398d-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9398d-121">-EndpointName</span></span>
<span data-ttu-id="9398d-122">라우팅 엔드포인트의 이름</span><span class="sxs-lookup"><span data-stu-id="9398d-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="9398d-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9398d-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="9398d-124">엔드포인트 리소스의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="9398d-124">Resource group of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9398d-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9398d-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="9398d-126">Endpoint 리소스의 SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9398d-126">SubscriptionId of the Endpoint resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9398d-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="9398d-127">-EndpointType</span></span>
<span data-ttu-id="9398d-128">라우팅 엔드포인트 유형</span><span class="sxs-lookup"><span data-stu-id="9398d-128">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9398d-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="9398d-129">-ContainerName</span></span>
<span data-ttu-id="9398d-130">저장소 컨테이너의 이름</span><span class="sxs-lookup"><span data-stu-id="9398d-130">Name of the storage container</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9398d-131">-인코딩</span><span class="sxs-lookup"><span data-stu-id="9398d-131">-Encoding</span></span>
<span data-ttu-id="9398d-132">데이터를 라우팅할 형식을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="9398d-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="9398d-133">JSON 또는 AVRO를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9398d-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="9398d-134">기본값은 AVRO로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="9398d-134">The default is set to AVRO.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:
Accepted values: JSON, AVRO

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9398d-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9398d-135">-InputObject</span></span>
<span data-ttu-id="9398d-136">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="9398d-136">IotHub Object</span></span>

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

### <span data-ttu-id="9398d-137">-Name</span><span class="sxs-lookup"><span data-stu-id="9398d-137">-Name</span></span>
<span data-ttu-id="9398d-138">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="9398d-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9398d-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9398d-139">-ResourceGroupName</span></span>
<span data-ttu-id="9398d-140">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="9398d-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9398d-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9398d-141">-ResourceId</span></span>
<span data-ttu-id="9398d-142">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9398d-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9398d-143">-확인</span><span class="sxs-lookup"><span data-stu-id="9398d-143">-Confirm</span></span>
<span data-ttu-id="9398d-144">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9398d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9398d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9398d-145">-WhatIf</span></span>
<span data-ttu-id="9398d-146">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9398d-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9398d-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9398d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9398d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9398d-148">CommonParameters</span></span>
<span data-ttu-id="9398d-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9398d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9398d-150">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9398d-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9398d-151">입력</span><span class="sxs-lookup"><span data-stu-id="9398d-151">INPUTS</span></span>

### <span data-ttu-id="9398d-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9398d-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9398d-153">System.String</span><span class="sxs-lookup"><span data-stu-id="9398d-153">System.String</span></span>

## <span data-ttu-id="9398d-154">출력</span><span class="sxs-lookup"><span data-stu-id="9398d-154">OUTPUTS</span></span>

### <span data-ttu-id="9398d-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span><span class="sxs-lookup"><span data-stu-id="9398d-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="9398d-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span><span class="sxs-lookup"><span data-stu-id="9398d-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="9398d-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="9398d-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="9398d-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9398d-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="9398d-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9398d-159">NOTES</span></span>

## <span data-ttu-id="9398d-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9398d-160">RELATED LINKS</span></span>

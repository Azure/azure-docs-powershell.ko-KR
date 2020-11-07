---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Add-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 9715e7ee505fce0b34039d74d35e53b7138d7160
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876745"
---
# <span data-ttu-id="ea9fc-101">Add-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="ea9fc-101">Add-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="ea9fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea9fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ea9fc-103">IoT Hub에 끝점 추가</span><span class="sxs-lookup"><span data-stu-id="ea9fc-103">Add an endpoint to your IoT Hub</span></span>

## <span data-ttu-id="ea9fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea9fc-104">SYNTAX</span></span>

### <span data-ttu-id="ea9fc-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ea9fc-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName] <String>
 -EndpointType <PSEndpointType> -EndpointResourceGroup <String> -EndpointSubscriptionId <String>
 -ConnectionString <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea9fc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ea9fc-106">InputObjectSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea9fc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ea9fc-107">ResourceIdSet</span></span>
```
Add-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName] <String> -EndpointType <PSEndpointType>
 -EndpointResourceGroup <String> -EndpointSubscriptionId <String> -ConnectionString <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea9fc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ea9fc-108">DESCRIPTION</span></span>
<span data-ttu-id="ea9fc-109">IoT Hub에 새 끝점을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea9fc-109">Add a new endpoint in your IoT Hub.</span></span> <span data-ttu-id="ea9fc-110">지원 되는 끝점에 대 한 자세한 내용은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span><span class="sxs-lookup"><span data-stu-id="ea9fc-110">To learn about the endpoints that are supported, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints</span></span>

## <span data-ttu-id="ea9fc-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ea9fc-111">EXAMPLES</span></span>

### <span data-ttu-id="ea9fc-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ea9fc-112">Example 1</span></span>
```
PS C:\> Add-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -EndpointType EventHub -EndpointResourceGroup resourcegroup1 -EndpointSubscriptionId 91d12343-a3de-345d-b2ea-135792468abc -ConnectionString 'Endpoint=sb://myeventhub1.servicebus.windows.net/;SharedAccessKeyName=access1;SharedAccessKey=*****=;EntityPath=event11'

ResourceGroupName : resourcegroup1
SubscriptionId    : 91d12343-a3de-345d-b2ea-135792468abc
EndpointName      : E2
ConnectionString  : Endpoint=sb://myeventhub1.servicebus.windows.net:5671/;SharedAccessKeyName=iothubroutes_myeventhub1;SharedAccessKey=****;EntityPath=event1
```

<span data-ttu-id="ea9fc-113">"Myiothub" IoT Hub에 EventHub 유형의 새 끝점 "E2"를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea9fc-113">Add a new endpoint "E2" of type EventHub to an "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="ea9fc-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="ea9fc-114">Example 2</span></span>
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

<span data-ttu-id="ea9fc-115">"Myiothub" IoT Hub에 AzureStorageContainer 유형의 새 끝점 "S1"을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea9fc-115">Add a new endpoint "S1" of type AzureStorageContainer to an "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="ea9fc-116">변수</span><span class="sxs-lookup"><span data-stu-id="ea9fc-116">PARAMETERS</span></span>

### <span data-ttu-id="ea9fc-117">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="ea9fc-117">-ConnectionString</span></span>
<span data-ttu-id="ea9fc-118">라우팅 끝점의 연결 문자열</span><span class="sxs-lookup"><span data-stu-id="ea9fc-118">Connection string of the Routing Endpoint</span></span>

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

### <span data-ttu-id="ea9fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea9fc-119">-DefaultProfile</span></span>
<span data-ttu-id="ea9fc-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea9fc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea9fc-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ea9fc-121">-EndpointName</span></span>
<span data-ttu-id="ea9fc-122">라우팅 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea9fc-122">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="ea9fc-123">-EndpointResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ea9fc-123">-EndpointResourceGroup</span></span>
<span data-ttu-id="ea9fc-124">끝점 리소스의 리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="ea9fc-124">Resource group of the Endpoint resource</span></span>

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

### <span data-ttu-id="ea9fc-125">-EndpointSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea9fc-125">-EndpointSubscriptionId</span></span>
<span data-ttu-id="ea9fc-126">끝점 리소스의 SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea9fc-126">SubscriptionId of the Endpoint resource</span></span>

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

### <span data-ttu-id="ea9fc-127">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="ea9fc-127">-EndpointType</span></span>
<span data-ttu-id="ea9fc-128">라우팅 끝점의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ea9fc-128">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="ea9fc-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ea9fc-129">-ContainerName</span></span>
<span data-ttu-id="ea9fc-130">저장소 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea9fc-130">Name of the storage container</span></span>

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

### <span data-ttu-id="ea9fc-131">-인코딩</span><span class="sxs-lookup"><span data-stu-id="ea9fc-131">-Encoding</span></span>
<span data-ttu-id="ea9fc-132">데이터를 라우팅하는 데 사용할 형식을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea9fc-132">Select the format in which you want to route your data in.</span></span> <span data-ttu-id="ea9fc-133">JSON 또는 AVRO를 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea9fc-133">You can select JSON or AVRO.</span></span> <span data-ttu-id="ea9fc-134">기본값은 AVRO로 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea9fc-134">The default is set to AVRO.</span></span>

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

### <span data-ttu-id="ea9fc-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea9fc-135">-InputObject</span></span>
<span data-ttu-id="ea9fc-136">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="ea9fc-136">IotHub Object</span></span>

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

### <span data-ttu-id="ea9fc-137">-이름</span><span class="sxs-lookup"><span data-stu-id="ea9fc-137">-Name</span></span>
<span data-ttu-id="ea9fc-138">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="ea9fc-138">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ea9fc-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea9fc-139">-ResourceGroupName</span></span>
<span data-ttu-id="ea9fc-140">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea9fc-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ea9fc-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea9fc-141">-ResourceId</span></span>
<span data-ttu-id="ea9fc-142">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="ea9fc-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ea9fc-143">-확인</span><span class="sxs-lookup"><span data-stu-id="ea9fc-143">-Confirm</span></span>
<span data-ttu-id="ea9fc-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea9fc-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea9fc-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea9fc-145">-WhatIf</span></span>
<span data-ttu-id="ea9fc-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea9fc-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea9fc-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea9fc-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea9fc-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea9fc-148">CommonParameters</span></span>
<span data-ttu-id="ea9fc-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea9fc-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea9fc-150">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea9fc-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea9fc-151">입력</span><span class="sxs-lookup"><span data-stu-id="ea9fc-151">INPUTS</span></span>

### <span data-ttu-id="ea9fc-152">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="ea9fc-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ea9fc-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ea9fc-153">System.String</span></span>

## <span data-ttu-id="ea9fc-154">출력</span><span class="sxs-lookup"><span data-stu-id="ea9fc-154">OUTPUTS</span></span>

### <span data-ttu-id="ea9fc-155">IotHub. PSRoutingEventHubEndpoint/. \*</span><span class="sxs-lookup"><span data-stu-id="ea9fc-155">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>

### <span data-ttu-id="ea9fc-156">IotHub를 통해 PSRoutingServiceBusQueueEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ea9fc-156">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint</span></span>

### <span data-ttu-id="ea9fc-157">IotHub. Psroutingservice Stopicendpoint.</span><span class="sxs-lookup"><span data-stu-id="ea9fc-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint</span></span>

### <span data-ttu-id="ea9fc-158">IotHub. PSRoutingStorageContainerEndpoint/. \*</span><span class="sxs-lookup"><span data-stu-id="ea9fc-158">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint</span></span>

## <span data-ttu-id="ea9fc-159">상속자</span><span class="sxs-lookup"><span data-stu-id="ea9fc-159">NOTES</span></span>

## <span data-ttu-id="ea9fc-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea9fc-160">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoutingEndpoint.md
ms.openlocfilehash: 6caad4faec3dd292f902689757b82b90091afcde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535884"
---
# <span data-ttu-id="13e85-101">Remove-AzureRmIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="13e85-101">Remove-AzureRmIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="13e85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13e85-102">SYNOPSIS</span></span>
<span data-ttu-id="13e85-103">IoT Hub의 끝점 삭제</span><span class="sxs-lookup"><span data-stu-id="13e85-103">Delete an endpoint for your IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13e85-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13e85-104">SYNTAX</span></span>

### <span data-ttu-id="13e85-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="13e85-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13e85-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="13e85-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13e85-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="13e85-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13e85-108">설명은</span><span class="sxs-lookup"><span data-stu-id="13e85-108">DESCRIPTION</span></span>
<span data-ttu-id="13e85-109">끝점을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="13e85-109">Delete an endpoint.</span></span> <span data-ttu-id="13e85-110">이 끝점을 사용 하는 모든 경로를 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="13e85-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="13e85-111">예제의</span><span class="sxs-lookup"><span data-stu-id="13e85-111">EXAMPLES</span></span>

### <span data-ttu-id="13e85-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="13e85-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="13e85-113">"Myiothub" IoT Hub에서 "E2" 끝점을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="13e85-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="13e85-114">변수</span><span class="sxs-lookup"><span data-stu-id="13e85-114">PARAMETERS</span></span>

### <span data-ttu-id="13e85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13e85-115">-DefaultProfile</span></span>
<span data-ttu-id="13e85-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13e85-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13e85-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="13e85-117">-EndpointName</span></span>
<span data-ttu-id="13e85-118">라우팅 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13e85-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="13e85-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="13e85-119">-EndpointType</span></span>
<span data-ttu-id="13e85-120">라우팅 끝점의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="13e85-120">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13e85-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13e85-121">-InputObject</span></span>
<span data-ttu-id="13e85-122">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="13e85-122">IotHub Object</span></span>

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

### <span data-ttu-id="13e85-123">-이름</span><span class="sxs-lookup"><span data-stu-id="13e85-123">-Name</span></span>
<span data-ttu-id="13e85-124">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="13e85-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="13e85-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13e85-125">-PassThru</span></span>
<span data-ttu-id="13e85-126">Boolean 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13e85-126">Allows to return the boolean object.</span></span> <span data-ttu-id="13e85-127">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13e85-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="13e85-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13e85-128">-ResourceGroupName</span></span>
<span data-ttu-id="13e85-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13e85-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="13e85-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13e85-130">-ResourceId</span></span>
<span data-ttu-id="13e85-131">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="13e85-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="13e85-132">-확인</span><span class="sxs-lookup"><span data-stu-id="13e85-132">-Confirm</span></span>
<span data-ttu-id="13e85-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="13e85-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13e85-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13e85-134">-WhatIf</span></span>
<span data-ttu-id="13e85-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="13e85-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13e85-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13e85-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13e85-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13e85-137">CommonParameters</span></span>
<span data-ttu-id="13e85-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13e85-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13e85-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13e85-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13e85-140">입력</span><span class="sxs-lookup"><span data-stu-id="13e85-140">INPUTS</span></span>

### <span data-ttu-id="13e85-141">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="13e85-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="13e85-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="13e85-142">System.String</span></span>

## <span data-ttu-id="13e85-143">출력</span><span class="sxs-lookup"><span data-stu-id="13e85-143">OUTPUTS</span></span>

### <span data-ttu-id="13e85-144">IotHub. PSRoutingEventHubEndpoint/. \*</span><span class="sxs-lookup"><span data-stu-id="13e85-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubEndpoint</span></span>
<span data-ttu-id="13e85-145">System.webserver. 목록 `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List` 1 [[Microsoft. IotHub.-PSRoutingServiceBusQueueEndpointProperties, IotHub, Version = 3.1.3.0, Culture = 중립, PublicKeyToken = null]] Microsoft azure.-IotHub.-Psroutingservice Stopicendpoint system.webserver,. 목록 `1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List` 1 [[Microsoft Azure. 명령]을 표시 합니다. IotHub, PSRoutingStorageContainerProperties, IotHub, Version = 3.1.3.0, Culture = 중립, PublicKeyToken = null]] System.webserver. List ' 1 [[Microsoft Azure. IotHub. PSRoutingCustomEndpoint, Microsoft Azure. IotHub, Version = 3.1.3.0, Culture = 중립, PublicKeyToken = null]]을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="13e85-145">System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingEventHubProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusQueueEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpoint System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingServiceBusTopicEndpointProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]
Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerEndpoint
System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingStorageContainerProperties, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]] System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingCustomEndpoint, Microsoft.Azure.Commands.IotHub, Version=3.1.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="13e85-146">상속자</span><span class="sxs-lookup"><span data-stu-id="13e85-146">NOTES</span></span>

## <span data-ttu-id="13e85-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13e85-147">RELATED LINKS</span></span>

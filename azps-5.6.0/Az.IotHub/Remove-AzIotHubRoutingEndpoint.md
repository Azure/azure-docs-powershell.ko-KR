---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 1b14ce37d03e1840336696792493e30701a09bfe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997831"
---
# <span data-ttu-id="0d99b-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d99b-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="0d99b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d99b-102">SYNOPSIS</span></span>
<span data-ttu-id="0d99b-103">IoT Hub에 대한 엔드포인트 삭제</span><span class="sxs-lookup"><span data-stu-id="0d99b-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="0d99b-104">구문</span><span class="sxs-lookup"><span data-stu-id="0d99b-104">SYNTAX</span></span>

### <span data-ttu-id="0d99b-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0d99b-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d99b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0d99b-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d99b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0d99b-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d99b-108">설명</span><span class="sxs-lookup"><span data-stu-id="0d99b-108">DESCRIPTION</span></span>
<span data-ttu-id="0d99b-109">엔드포인트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="0d99b-109">Delete an endpoint.</span></span> <span data-ttu-id="0d99b-110">이 엔드포인트를 사용하는 모든 경로를 삭제해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d99b-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="0d99b-111">예제</span><span class="sxs-lookup"><span data-stu-id="0d99b-111">EXAMPLES</span></span>

### <span data-ttu-id="0d99b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="0d99b-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="0d99b-113">"myiothub" IoT Hub에서 엔드포인트 "E2"를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="0d99b-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="0d99b-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0d99b-114">PARAMETERS</span></span>

### <span data-ttu-id="0d99b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d99b-115">-DefaultProfile</span></span>
<span data-ttu-id="0d99b-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d99b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d99b-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0d99b-117">-EndpointName</span></span>
<span data-ttu-id="0d99b-118">라우팅 엔드포인트의 이름</span><span class="sxs-lookup"><span data-stu-id="0d99b-118">Name of the Routing Endpoint</span></span>

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

### <span data-ttu-id="0d99b-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="0d99b-119">-EndpointType</span></span>
<span data-ttu-id="0d99b-120">라우팅 엔드포인트 유형</span><span class="sxs-lookup"><span data-stu-id="0d99b-120">Type of the Routing Endpoint</span></span>

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

### <span data-ttu-id="0d99b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d99b-121">-InputObject</span></span>
<span data-ttu-id="0d99b-122">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="0d99b-122">IotHub Object</span></span>

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

### <span data-ttu-id="0d99b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0d99b-123">-Name</span></span>
<span data-ttu-id="0d99b-124">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="0d99b-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0d99b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d99b-125">-PassThru</span></span>
<span data-ttu-id="0d99b-126">부울 개체를 반환할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d99b-126">Allows to return the boolean object.</span></span> <span data-ttu-id="0d99b-127">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d99b-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0d99b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d99b-128">-ResourceGroupName</span></span>
<span data-ttu-id="0d99b-129">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="0d99b-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0d99b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d99b-130">-ResourceId</span></span>
<span data-ttu-id="0d99b-131">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="0d99b-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0d99b-132">-확인</span><span class="sxs-lookup"><span data-stu-id="0d99b-132">-Confirm</span></span>
<span data-ttu-id="0d99b-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d99b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d99b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d99b-134">-WhatIf</span></span>
<span data-ttu-id="0d99b-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0d99b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d99b-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d99b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d99b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d99b-137">CommonParameters</span></span>
<span data-ttu-id="0d99b-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0d99b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d99b-139">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0d99b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d99b-140">입력</span><span class="sxs-lookup"><span data-stu-id="0d99b-140">INPUTS</span></span>

### <span data-ttu-id="0d99b-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0d99b-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0d99b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0d99b-142">System.String</span></span>

## <span data-ttu-id="0d99b-143">출력</span><span class="sxs-lookup"><span data-stu-id="0d99b-143">OUTPUTS</span></span>

### <span data-ttu-id="0d99b-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0d99b-144">System.Boolean</span></span>

## <span data-ttu-id="0d99b-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0d99b-145">NOTES</span></span>

## <span data-ttu-id="0d99b-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d99b-146">RELATED LINKS</span></span>

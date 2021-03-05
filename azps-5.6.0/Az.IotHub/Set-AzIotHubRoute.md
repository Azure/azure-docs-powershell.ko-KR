---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: 2cac00b1510c658b01d815d281ef16cef02b1dc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004107"
---
# <span data-ttu-id="c00b3-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="c00b3-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="c00b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c00b3-102">SYNOPSIS</span></span>
<span data-ttu-id="c00b3-103">IoT Hub에서 경로 업데이트</span><span class="sxs-lookup"><span data-stu-id="c00b3-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="c00b3-104">구문</span><span class="sxs-lookup"><span data-stu-id="c00b3-104">SYNTAX</span></span>

### <span data-ttu-id="c00b3-105">ResourceSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c00b3-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c00b3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c00b3-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c00b3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c00b3-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c00b3-108">설명</span><span class="sxs-lookup"><span data-stu-id="c00b3-108">DESCRIPTION</span></span>
<span data-ttu-id="c00b3-109">경로를 편집합니다.</span><span class="sxs-lookup"><span data-stu-id="c00b3-109">Edit a route.</span></span> <span data-ttu-id="c00b3-110">데이터 원본, 엔드포인트, 라우팅 쿼리를 포함하여 경로의 모든 필드를 업데이트하고 경로를 사용하도록 설정하거나 사용하지 않도록 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c00b3-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="c00b3-111">예제</span><span class="sxs-lookup"><span data-stu-id="c00b3-111">EXAMPLES</span></span>

### <span data-ttu-id="c00b3-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="c00b3-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="c00b3-113">경로 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c00b3-113">Updating the route information.</span></span>

### <span data-ttu-id="c00b3-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="c00b3-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="c00b3-115">경로 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c00b3-115">Updating the route information.</span></span>

### <span data-ttu-id="c00b3-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="c00b3-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="c00b3-117">경로 정보를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c00b3-117">Updating the route information.</span></span>

## <span data-ttu-id="c00b3-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c00b3-118">PARAMETERS</span></span>

### <span data-ttu-id="c00b3-119">-조건</span><span class="sxs-lookup"><span data-stu-id="c00b3-119">-Condition</span></span>
<span data-ttu-id="c00b3-120">라우팅 규칙을 적용하기 위해 평가된 조건</span><span class="sxs-lookup"><span data-stu-id="c00b3-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="c00b3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c00b3-121">-DefaultProfile</span></span>
<span data-ttu-id="c00b3-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c00b3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c00b3-123">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="c00b3-123">-Enabled</span></span>
<span data-ttu-id="c00b3-124">경로 사용</span><span class="sxs-lookup"><span data-stu-id="c00b3-124">Enable route</span></span>

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

### <span data-ttu-id="c00b3-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c00b3-125">-EndpointName</span></span>
<span data-ttu-id="c00b3-126">라우팅 엔드포인트의 이름</span><span class="sxs-lookup"><span data-stu-id="c00b3-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="c00b3-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c00b3-127">-InputObject</span></span>
<span data-ttu-id="c00b3-128">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="c00b3-128">IotHub Object</span></span>

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

### <span data-ttu-id="c00b3-129">-Name</span><span class="sxs-lookup"><span data-stu-id="c00b3-129">-Name</span></span>
<span data-ttu-id="c00b3-130">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="c00b3-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c00b3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c00b3-131">-ResourceGroupName</span></span>
<span data-ttu-id="c00b3-132">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="c00b3-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c00b3-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c00b3-133">-ResourceId</span></span>
<span data-ttu-id="c00b3-134">IotHub 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c00b3-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c00b3-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="c00b3-135">-RouteName</span></span>
<span data-ttu-id="c00b3-136">경로의 이름</span><span class="sxs-lookup"><span data-stu-id="c00b3-136">Name of the Route</span></span>

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

### <span data-ttu-id="c00b3-137">-Source</span><span class="sxs-lookup"><span data-stu-id="c00b3-137">-Source</span></span>
<span data-ttu-id="c00b3-138">경로의 원본</span><span class="sxs-lookup"><span data-stu-id="c00b3-138">Source of the route</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource]
Parameter Sets: (All)
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00b3-139">-확인</span><span class="sxs-lookup"><span data-stu-id="c00b3-139">-Confirm</span></span>
<span data-ttu-id="c00b3-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c00b3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c00b3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c00b3-141">-WhatIf</span></span>
<span data-ttu-id="c00b3-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c00b3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c00b3-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c00b3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c00b3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c00b3-144">CommonParameters</span></span>
<span data-ttu-id="c00b3-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c00b3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c00b3-146">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c00b3-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c00b3-147">입력</span><span class="sxs-lookup"><span data-stu-id="c00b3-147">INPUTS</span></span>

### <span data-ttu-id="c00b3-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c00b3-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c00b3-149">System.String</span><span class="sxs-lookup"><span data-stu-id="c00b3-149">System.String</span></span>

## <span data-ttu-id="c00b3-150">출력</span><span class="sxs-lookup"><span data-stu-id="c00b3-150">OUTPUTS</span></span>

### <span data-ttu-id="c00b3-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span><span class="sxs-lookup"><span data-stu-id="c00b3-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="c00b3-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c00b3-152">NOTES</span></span>

## <span data-ttu-id="c00b3-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c00b3-153">RELATED LINKS</span></span>

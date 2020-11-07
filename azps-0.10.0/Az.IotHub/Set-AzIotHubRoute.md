---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Set-AzIotHubRoute.md
ms.openlocfilehash: 4df4b5415a0fffc2f2482540088b36964cfa89ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875851"
---
# <span data-ttu-id="afddc-101">Set-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="afddc-101">Set-AzIotHubRoute</span></span>

## <span data-ttu-id="afddc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afddc-102">SYNOPSIS</span></span>
<span data-ttu-id="afddc-103">IoT Hub에서 경로 업데이트</span><span class="sxs-lookup"><span data-stu-id="afddc-103">Update a route in IoT Hub</span></span>

## <span data-ttu-id="afddc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="afddc-104">SYNTAX</span></span>

### <span data-ttu-id="afddc-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="afddc-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String>
 [-Source <PSRoutingSource>] [-EndpointName <String>] [-Condition <String>] [-Enabled]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afddc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="afddc-106">InputObjectSet</span></span>
```
Set-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afddc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="afddc-107">ResourceIdSet</span></span>
```
Set-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Source <PSRoutingSource>]
 [-EndpointName <String>] [-Condition <String>] [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afddc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="afddc-108">DESCRIPTION</span></span>
<span data-ttu-id="afddc-109">경로를 편집 합니다.</span><span class="sxs-lookup"><span data-stu-id="afddc-109">Edit a route.</span></span> <span data-ttu-id="afddc-110">데이터 원본, 끝점, 라우팅 쿼리를 비롯 하 여 경로에 있는 모든 필드를 업데이트할 수 있으며, 경로를 설정 하거나 해제할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afddc-110">You can update all the fields in a route including the data source, endpoint, routing query and also enable or disable the route.</span></span>

## <span data-ttu-id="afddc-111">예제의</span><span class="sxs-lookup"><span data-stu-id="afddc-111">EXAMPLES</span></span>

### <span data-ttu-id="afddc-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="afddc-112">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Source TwinChangeEvents 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : events
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="afddc-113">경로 정보 업데이트</span><span class="sxs-lookup"><span data-stu-id="afddc-113">Updating the route information.</span></span>

### <span data-ttu-id="afddc-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="afddc-114">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -EndpointName E1 

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : False
```

<span data-ttu-id="afddc-115">경로 정보 업데이트</span><span class="sxs-lookup"><span data-stu-id="afddc-115">Updating the route information.</span></span>

### <span data-ttu-id="afddc-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="afddc-116">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -Enabled

RouteName     : R1
DataSource    : TwinChangeEvents
EndpointNames : E1
Condition     : true
IsEnabled     : True
```

<span data-ttu-id="afddc-117">경로 정보 업데이트</span><span class="sxs-lookup"><span data-stu-id="afddc-117">Updating the route information.</span></span>

## <span data-ttu-id="afddc-118">변수</span><span class="sxs-lookup"><span data-stu-id="afddc-118">PARAMETERS</span></span>

### <span data-ttu-id="afddc-119">-조건</span><span class="sxs-lookup"><span data-stu-id="afddc-119">-Condition</span></span>
<span data-ttu-id="afddc-120">라우팅 규칙을 적용 하도록 평가 되는 조건</span><span class="sxs-lookup"><span data-stu-id="afddc-120">Condition that is evaluated to apply the routing rule</span></span>

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

### <span data-ttu-id="afddc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afddc-121">-DefaultProfile</span></span>
<span data-ttu-id="afddc-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="afddc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afddc-123">-사용</span><span class="sxs-lookup"><span data-stu-id="afddc-123">-Enabled</span></span>
<span data-ttu-id="afddc-124">경로 사용</span><span class="sxs-lookup"><span data-stu-id="afddc-124">Enable route</span></span>

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

### <span data-ttu-id="afddc-125">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="afddc-125">-EndpointName</span></span>
<span data-ttu-id="afddc-126">라우팅 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afddc-126">Name of the routing endpoint</span></span>

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

### <span data-ttu-id="afddc-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afddc-127">-InputObject</span></span>
<span data-ttu-id="afddc-128">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="afddc-128">IotHub Object</span></span>

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

### <span data-ttu-id="afddc-129">-이름</span><span class="sxs-lookup"><span data-stu-id="afddc-129">-Name</span></span>
<span data-ttu-id="afddc-130">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="afddc-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="afddc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afddc-131">-ResourceGroupName</span></span>
<span data-ttu-id="afddc-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afddc-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="afddc-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afddc-133">-ResourceId</span></span>
<span data-ttu-id="afddc-134">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="afddc-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="afddc-135">-RouteName</span><span class="sxs-lookup"><span data-stu-id="afddc-135">-RouteName</span></span>
<span data-ttu-id="afddc-136">경로의 이름</span><span class="sxs-lookup"><span data-stu-id="afddc-136">Name of the Route</span></span>

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

### <span data-ttu-id="afddc-137">-원본</span><span class="sxs-lookup"><span data-stu-id="afddc-137">-Source</span></span>
<span data-ttu-id="afddc-138">경로의 원본</span><span class="sxs-lookup"><span data-stu-id="afddc-138">Source of the route</span></span>

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

### <span data-ttu-id="afddc-139">-확인</span><span class="sxs-lookup"><span data-stu-id="afddc-139">-Confirm</span></span>
<span data-ttu-id="afddc-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="afddc-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afddc-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afddc-141">-WhatIf</span></span>
<span data-ttu-id="afddc-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="afddc-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afddc-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="afddc-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afddc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afddc-144">CommonParameters</span></span>
<span data-ttu-id="afddc-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="afddc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afddc-146">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afddc-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afddc-147">입력</span><span class="sxs-lookup"><span data-stu-id="afddc-147">INPUTS</span></span>

### <span data-ttu-id="afddc-148">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="afddc-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="afddc-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="afddc-149">System.String</span></span>

## <span data-ttu-id="afddc-150">출력</span><span class="sxs-lookup"><span data-stu-id="afddc-150">OUTPUTS</span></span>

### <span data-ttu-id="afddc-151">IotHub. PSRouteMetadata/. \*</span><span class="sxs-lookup"><span data-stu-id="afddc-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata</span></span>

## <span data-ttu-id="afddc-152">상속자</span><span class="sxs-lookup"><span data-stu-id="afddc-152">NOTES</span></span>

## <span data-ttu-id="afddc-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="afddc-153">RELATED LINKS</span></span>

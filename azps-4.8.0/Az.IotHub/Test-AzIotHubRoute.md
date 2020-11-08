---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/test-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Test-AzIotHubRoute.md
ms.openlocfilehash: eb9d6a7b847c360861fd13bb285bc6f09bb70fbc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211892"
---
# <span data-ttu-id="44fc2-101">Test-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="44fc2-101">Test-AzIotHubRoute</span></span>

## <span data-ttu-id="44fc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="44fc2-103">IoT Hub의 테스트 경로</span><span class="sxs-lookup"><span data-stu-id="44fc2-103">Test routes in IoT Hub</span></span>

## <span data-ttu-id="44fc2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44fc2-104">SYNTAX</span></span>

### <span data-ttu-id="44fc2-105">ResourceSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="44fc2-105">ResourceSet (Default)</span></span>
```
Test-AzIotHubRoute [-Body <String>] [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44fc2-106">InputObjectTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="44fc2-106">InputObjectTestRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44fc2-107">InputObjectTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="44fc2-107">InputObjectTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-InputObject] <PSIotHub> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="44fc2-108">TestRouteSet</span><span class="sxs-lookup"><span data-stu-id="44fc2-108">TestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName] <String> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-ShowError]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44fc2-109">TestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="44fc2-109">TestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="44fc2-110">ResourceIdTestRouteSet</span><span class="sxs-lookup"><span data-stu-id="44fc2-110">ResourceIdTestRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-RouteName] <String> [-Body <String>] [-AppProperty <Hashtable>]
 [-SystemProperty <Hashtable>] [-ShowError] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44fc2-111">ResourceIdTestAllRouteSet</span><span class="sxs-lookup"><span data-stu-id="44fc2-111">ResourceIdTestAllRouteSet</span></span>
```
Test-AzIotHubRoute [-ResourceId] <String> [-Source] <PSRoutingSource> [-Body <String>]
 [-AppProperty <Hashtable>] [-SystemProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44fc2-112">설명은</span><span class="sxs-lookup"><span data-stu-id="44fc2-112">DESCRIPTION</span></span>
<span data-ttu-id="44fc2-113">특정 경로를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="44fc2-113">Test a specific route.</span></span>

## <span data-ttu-id="44fc2-114">예제의</span><span class="sxs-lookup"><span data-stu-id="44fc2-114">EXAMPLES</span></span>

### <span data-ttu-id="44fc2-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="44fc2-115">Example 1</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -Source DeviceMessages

RouteName DataSource     EndpointNames IsEnabled
--------- ----------     ------------- ---------
R1        DeviceMessages events        True
R5        DeviceMessages E1            True
```

<span data-ttu-id="44fc2-116">원본이 "DeviceMessages" 인 모든 경로를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="44fc2-116">Test all route with source "DeviceMessages".</span></span>

### <span data-ttu-id="44fc2-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="44fc2-117">Example 2</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1

Result : true
```

<span data-ttu-id="44fc2-118">특정 경로를 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="44fc2-118">Test a specific route.</span></span>

### <span data-ttu-id="44fc2-119">예제 3</span><span class="sxs-lookup"><span data-stu-id="44fc2-119">Example 3</span></span>
```
PS C:\> Test-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -ShowError

ErrorMessage  Severity LocationStartLine LocationStartColumn LocationEndLine LocationEndColumn
------------  -------- ----------------- ------------------- --------------- -----------------
Syntax error. error    1                 29                  1               30
```

<span data-ttu-id="44fc2-120">특정 경로를 테스트 하 고 실패 이유를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="44fc2-120">Test a specific route and showing the reason of failure.</span></span>

## <span data-ttu-id="44fc2-121">변수</span><span class="sxs-lookup"><span data-stu-id="44fc2-121">PARAMETERS</span></span>

### <span data-ttu-id="44fc2-122">-AppProperty</span><span class="sxs-lookup"><span data-stu-id="44fc2-122">-AppProperty</span></span>
<span data-ttu-id="44fc2-123">Route 메시지의 앱 속성</span><span class="sxs-lookup"><span data-stu-id="44fc2-123">App properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fc2-124">-본문</span><span class="sxs-lookup"><span data-stu-id="44fc2-124">-Body</span></span>
<span data-ttu-id="44fc2-125">경로 메시지의 본문</span><span class="sxs-lookup"><span data-stu-id="44fc2-125">Body of the route message</span></span>

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

### <span data-ttu-id="44fc2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44fc2-126">-DefaultProfile</span></span>
<span data-ttu-id="44fc2-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44fc2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44fc2-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44fc2-128">-InputObject</span></span>
<span data-ttu-id="44fc2-129">IotHub 개체</span><span class="sxs-lookup"><span data-stu-id="44fc2-129">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectTestRouteSet, InputObjectTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44fc2-130">-이름</span><span class="sxs-lookup"><span data-stu-id="44fc2-130">-Name</span></span>
<span data-ttu-id="44fc2-131">Iot Hub의 이름</span><span class="sxs-lookup"><span data-stu-id="44fc2-131">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fc2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44fc2-132">-ResourceGroupName</span></span>
<span data-ttu-id="44fc2-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44fc2-133">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: TestRouteSet, TestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fc2-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44fc2-134">-ResourceId</span></span>
<span data-ttu-id="44fc2-135">IotHub 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="44fc2-135">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdTestRouteSet, ResourceIdTestAllRouteSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44fc2-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="44fc2-136">-RouteName</span></span>
<span data-ttu-id="44fc2-137">경로의 이름</span><span class="sxs-lookup"><span data-stu-id="44fc2-137">Name of the Route</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fc2-138">-ShowError</span><span class="sxs-lookup"><span data-stu-id="44fc2-138">-ShowError</span></span>
<span data-ttu-id="44fc2-139">자세한 오류 표시 (있는 경우)</span><span class="sxs-lookup"><span data-stu-id="44fc2-139">Show detailed error, if exist</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputObjectTestRouteSet, TestRouteSet, ResourceIdTestRouteSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fc2-140">-원본</span><span class="sxs-lookup"><span data-stu-id="44fc2-140">-Source</span></span>
<span data-ttu-id="44fc2-141">경로의 원본</span><span class="sxs-lookup"><span data-stu-id="44fc2-141">Source of the route</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingSource
Parameter Sets: InputObjectTestAllRouteSet, TestAllRouteSet, ResourceIdTestAllRouteSet
Aliases:
Accepted values: Invalid, DeviceMessages, TwinChangeEvents, DeviceLifecycleEvents, DeviceJobLifecycleEvents, DigitalTwinChangeEvents

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fc2-142">-SystemProperty</span><span class="sxs-lookup"><span data-stu-id="44fc2-142">-SystemProperty</span></span>
<span data-ttu-id="44fc2-143">Route 메시지의 시스템 속성</span><span class="sxs-lookup"><span data-stu-id="44fc2-143">System properties of the route message</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44fc2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44fc2-144">CommonParameters</span></span>
<span data-ttu-id="44fc2-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44fc2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44fc2-146">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44fc2-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44fc2-147">입력</span><span class="sxs-lookup"><span data-stu-id="44fc2-147">INPUTS</span></span>

### <span data-ttu-id="44fc2-148">IotHub. PSIotHub/. \*</span><span class="sxs-lookup"><span data-stu-id="44fc2-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="44fc2-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="44fc2-149">System.String</span></span>

## <span data-ttu-id="44fc2-150">출력</span><span class="sxs-lookup"><span data-stu-id="44fc2-150">OUTPUTS</span></span>

### <span data-ttu-id="44fc2-151">IotHub. PSTestRouteResult/. \*</span><span class="sxs-lookup"><span data-stu-id="44fc2-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSTestRouteResult</span></span>

### <span data-ttu-id="44fc2-152">IotHub. PSRouteCompilationError/. \*</span><span class="sxs-lookup"><span data-stu-id="44fc2-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteCompilationError</span></span>

### <span data-ttu-id="44fc2-153">IotHub를 PSRouteProperties []으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="44fc2-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteProperties[]</span></span>

## <span data-ttu-id="44fc2-154">상속자</span><span class="sxs-lookup"><span data-stu-id="44fc2-154">NOTES</span></span>

## <span data-ttu-id="44fc2-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44fc2-155">RELATED LINKS</span></span>

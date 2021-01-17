---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 5a29c0bbad712d99b03ab1ff5347cba5c07b02aa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385428"
---
# <span data-ttu-id="780fe-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="780fe-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="780fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="780fe-102">SYNOPSIS</span></span>
<span data-ttu-id="780fe-103">연결 모니터 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="780fe-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="780fe-104">구문</span><span class="sxs-lookup"><span data-stu-id="780fe-104">SYNTAX</span></span>

### <span data-ttu-id="780fe-105">AzureVM</span><span class="sxs-lookup"><span data-stu-id="780fe-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="780fe-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="780fe-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="780fe-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="780fe-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="780fe-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="780fe-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="780fe-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="780fe-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="780fe-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="780fe-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="780fe-111">설명</span><span class="sxs-lookup"><span data-stu-id="780fe-111">DESCRIPTION</span></span>
<span data-ttu-id="780fe-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet은 연결 모니터 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="780fe-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="780fe-113">예제</span><span class="sxs-lookup"><span data-stu-id="780fe-113">EXAMPLES</span></span>

### <span data-ttu-id="780fe-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="780fe-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="780fe-115">이름 : workspaceEndpoint 형식 : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-0000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace address : Scope : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span><span class="sxs-lookup"><span data-stu-id="780fe-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="780fe-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="780fe-116">PARAMETERS</span></span>

### <span data-ttu-id="780fe-117">-Address</span><span class="sxs-lookup"><span data-stu-id="780fe-117">-Address</span></span>
<span data-ttu-id="780fe-118">연결 모니터 엔드포인트의 주소(IP 또는 도메인 이름).</span><span class="sxs-lookup"><span data-stu-id="780fe-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExternalAddress, MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780fe-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="780fe-119">-AzureSubnet</span></span>
<span data-ttu-id="780fe-120">Azure 서브넷 엔드포인트 스위치.</span><span class="sxs-lookup"><span data-stu-id="780fe-120">Azure Subnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780fe-121">-AzureVM</span><span class="sxs-lookup"><span data-stu-id="780fe-121">-AzureVM</span></span>
<span data-ttu-id="780fe-122">Azure VM 엔드포인트 스위치.</span><span class="sxs-lookup"><span data-stu-id="780fe-122">Azure VM endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780fe-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="780fe-123">-AzureVNet</span></span>
<span data-ttu-id="780fe-124">Azure Vnet 엔드포인트 스위치.</span><span class="sxs-lookup"><span data-stu-id="780fe-124">Azure Vnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVNet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780fe-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="780fe-125">-CoverageLevel</span></span>
<span data-ttu-id="780fe-126">엔드포인트에 대한 테스트 검사입니다.</span><span class="sxs-lookup"><span data-stu-id="780fe-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="780fe-127">지원되는 값은 기본값, 낮음, BelowAverage, Average, AboveAvergae, Full입니다.</span><span class="sxs-lookup"><span data-stu-id="780fe-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780fe-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="780fe-128">-DefaultProfile</span></span>
<span data-ttu-id="780fe-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="780fe-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="780fe-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="780fe-130">-ExcludeItem</span></span>
<span data-ttu-id="780fe-131">엔드포인트 범위에서 제외해야 하는 항목 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="780fe-131">List of items which need to be excluded from endpoint scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780fe-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="780fe-132">-ExternalAddress</span></span>
<span data-ttu-id="780fe-133">외부 주소 엔드포인트 스위치.</span><span class="sxs-lookup"><span data-stu-id="780fe-133">External Address endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExternalAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780fe-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="780fe-134">-IncludeItem</span></span>
<span data-ttu-id="780fe-135">끝점 범위에 포함해야 하는 항목 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="780fe-135">List of items which need to be included into endpont scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, MMAWorkspaceMachine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780fe-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="780fe-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="780fe-137">MMA 작업 영역 컴퓨터 엔드포인트 스위치.</span><span class="sxs-lookup"><span data-stu-id="780fe-137">MMA Workspace Machine endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780fe-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="780fe-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="780fe-139">MMA 작업 영역 네트워크 엔드포인트 스위치.</span><span class="sxs-lookup"><span data-stu-id="780fe-139">MMA Workspace Network endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780fe-140">-Name</span><span class="sxs-lookup"><span data-stu-id="780fe-140">-Name</span></span>
<span data-ttu-id="780fe-141">연결 모니터 엔드포인트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="780fe-141">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="780fe-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="780fe-142">-ResourceId</span></span>
<span data-ttu-id="780fe-143">연결 모니터 엔드포인트의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="780fe-143">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM, AzureVNet, AzureSubnet, MMAWorkspaceMachine, MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="780fe-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="780fe-144">-Confirm</span></span>
<span data-ttu-id="780fe-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="780fe-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="780fe-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="780fe-146">-WhatIf</span></span>
<span data-ttu-id="780fe-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="780fe-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="780fe-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="780fe-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="780fe-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="780fe-149">CommonParameters</span></span>
<span data-ttu-id="780fe-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="780fe-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="780fe-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="780fe-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="780fe-152">입력</span><span class="sxs-lookup"><span data-stu-id="780fe-152">INPUTS</span></span>

### <span data-ttu-id="780fe-153">없음</span><span class="sxs-lookup"><span data-stu-id="780fe-153">None</span></span>

## <span data-ttu-id="780fe-154">출력</span><span class="sxs-lookup"><span data-stu-id="780fe-154">OUTPUTS</span></span>

### <span data-ttu-id="780fe-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="780fe-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="780fe-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="780fe-156">NOTES</span></span>

## <span data-ttu-id="780fe-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="780fe-157">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 5a29c0bbad712d99b03ab1ff5347cba5c07b02aa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309206"
---
# <span data-ttu-id="549fb-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="549fb-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="549fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="549fb-102">SYNOPSIS</span></span>
<span data-ttu-id="549fb-103">연결 모니터 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="549fb-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="549fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="549fb-104">SYNTAX</span></span>

### <span data-ttu-id="549fb-105">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="549fb-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="549fb-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="549fb-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="549fb-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="549fb-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="549fb-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="549fb-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="549fb-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="549fb-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="549fb-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="549fb-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="549fb-111">설명은</span><span class="sxs-lookup"><span data-stu-id="549fb-111">DESCRIPTION</span></span>
<span data-ttu-id="549fb-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet은 연결 모니터 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="549fb-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="549fb-113">예제의</span><span class="sxs-lookup"><span data-stu-id="549fb-113">EXAMPLES</span></span>

### <span data-ttu-id="549fb-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="549fb-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="549fb-115">이름: workspaceEndpoint 유형: MMAWorkspaceMachine ResourceId:/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address: 범위: {"Include": [{"Address": "WIN-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="549fb-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="549fb-116">변수</span><span class="sxs-lookup"><span data-stu-id="549fb-116">PARAMETERS</span></span>

### <span data-ttu-id="549fb-117">-주소</span><span class="sxs-lookup"><span data-stu-id="549fb-117">-Address</span></span>
<span data-ttu-id="549fb-118">연결 모니터 끝점 (IP 또는 도메인 이름)의 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="549fb-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

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

### <span data-ttu-id="549fb-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="549fb-119">-AzureSubnet</span></span>
<span data-ttu-id="549fb-120">Azure 서브넷 끝점 전환</span><span class="sxs-lookup"><span data-stu-id="549fb-120">Azure Subnet endpoint switch.</span></span>

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

### <span data-ttu-id="549fb-121">-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="549fb-121">-AzureVM</span></span>
<span data-ttu-id="549fb-122">Azure VM 끝점 전환</span><span class="sxs-lookup"><span data-stu-id="549fb-122">Azure VM endpoint switch.</span></span>

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

### <span data-ttu-id="549fb-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="549fb-123">-AzureVNet</span></span>
<span data-ttu-id="549fb-124">Azure Vnet 끝점 스위치입니다.</span><span class="sxs-lookup"><span data-stu-id="549fb-124">Azure Vnet endpoint switch.</span></span>

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

### <span data-ttu-id="549fb-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="549fb-125">-CoverageLevel</span></span>
<span data-ttu-id="549fb-126">끝점에 대 한 테스트 검사</span><span class="sxs-lookup"><span data-stu-id="549fb-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="549fb-127">지원 되는 값은 Default, Low, BelowAverage, Average, AboveAvergae, Full입니다.</span><span class="sxs-lookup"><span data-stu-id="549fb-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

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

### <span data-ttu-id="549fb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="549fb-128">-DefaultProfile</span></span>
<span data-ttu-id="549fb-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="549fb-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="549fb-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="549fb-130">-ExcludeItem</span></span>
<span data-ttu-id="549fb-131">끝점 범위에서 제외 해야 하는 항목의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="549fb-131">List of items which need to be excluded from endpoint scope.</span></span>

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

### <span data-ttu-id="549fb-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="549fb-132">-ExternalAddress</span></span>
<span data-ttu-id="549fb-133">외부 주소 끝점 전환</span><span class="sxs-lookup"><span data-stu-id="549fb-133">External Address endpoint switch.</span></span>

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

### <span data-ttu-id="549fb-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="549fb-134">-IncludeItem</span></span>
<span data-ttu-id="549fb-135">Endpont scope에 포함 해야 하는 항목의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="549fb-135">List of items which need to be included into endpont scope.</span></span>

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

### <span data-ttu-id="549fb-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="549fb-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="549fb-137">MMA Workspace 컴퓨터 끝점 스위치.</span><span class="sxs-lookup"><span data-stu-id="549fb-137">MMA Workspace Machine endpoint switch.</span></span>

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

### <span data-ttu-id="549fb-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="549fb-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="549fb-139">MMA Workspace 네트워크 끝점 스위치.</span><span class="sxs-lookup"><span data-stu-id="549fb-139">MMA Workspace Network endpoint switch.</span></span>

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

### <span data-ttu-id="549fb-140">-이름</span><span class="sxs-lookup"><span data-stu-id="549fb-140">-Name</span></span>
<span data-ttu-id="549fb-141">연결 모니터 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="549fb-141">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="549fb-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="549fb-142">-ResourceId</span></span>
<span data-ttu-id="549fb-143">연결 모니터 끝점의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="549fb-143">Resource ID of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="549fb-144">-확인</span><span class="sxs-lookup"><span data-stu-id="549fb-144">-Confirm</span></span>
<span data-ttu-id="549fb-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="549fb-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="549fb-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="549fb-146">-WhatIf</span></span>
<span data-ttu-id="549fb-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="549fb-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="549fb-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="549fb-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="549fb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="549fb-149">CommonParameters</span></span>
<span data-ttu-id="549fb-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="549fb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="549fb-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="549fb-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="549fb-152">입력</span><span class="sxs-lookup"><span data-stu-id="549fb-152">INPUTS</span></span>

### <span data-ttu-id="549fb-153">않아야</span><span class="sxs-lookup"><span data-stu-id="549fb-153">None</span></span>

## <span data-ttu-id="549fb-154">출력</span><span class="sxs-lookup"><span data-stu-id="549fb-154">OUTPUTS</span></span>

### <span data-ttu-id="549fb-155">PSNetworkWatcherConnectionMonitorEndpointObject에 대 한.</span><span class="sxs-lookup"><span data-stu-id="549fb-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="549fb-156">상속자</span><span class="sxs-lookup"><span data-stu-id="549fb-156">NOTES</span></span>

## <span data-ttu-id="549fb-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="549fb-157">RELATED LINKS</span></span>

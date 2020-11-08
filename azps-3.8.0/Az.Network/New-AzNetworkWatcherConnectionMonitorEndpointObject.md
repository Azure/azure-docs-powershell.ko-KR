---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 58e26de74abb46234f6985c3973b5bbe494bd0ad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034491"
---
# <span data-ttu-id="c83c3-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="c83c3-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="c83c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c83c3-102">SYNOPSIS</span></span>
<span data-ttu-id="c83c3-103">연결 모니터 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c83c3-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="c83c3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c83c3-104">SYNTAX</span></span>

### <span data-ttu-id="c83c3-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c83c3-105">SetByResourceId</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] -ResourceId <String>
 [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c83c3-106">SetByAddress</span><span class="sxs-lookup"><span data-stu-id="c83c3-106">SetByAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] [-Address <String>] [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c83c3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c83c3-107">DESCRIPTION</span></span>
<span data-ttu-id="c83c3-108">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet은 연결 모니터 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c83c3-108">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="c83c3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c83c3-109">EXAMPLES</span></span>

### <span data-ttu-id="c83c3-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c83c3-110">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name "workspaceEndpoint" -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

<span data-ttu-id="c83c3-111">이름: workspaceEndpoint ResourceId:/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address: {"Type": "Include", "Items": [{"Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="c83c3-111">Name       : workspaceEndpoint ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Filter     : { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="c83c3-112">변수</span><span class="sxs-lookup"><span data-stu-id="c83c3-112">PARAMETERS</span></span>

### <span data-ttu-id="c83c3-113">-주소</span><span class="sxs-lookup"><span data-stu-id="c83c3-113">-Address</span></span>
<span data-ttu-id="c83c3-114">연결 모니터 끝점 (IP 또는 도메인 이름)의 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="c83c3-114">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c83c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c83c3-115">-DefaultProfile</span></span>
<span data-ttu-id="c83c3-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c83c3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c83c3-117">-FilterItem</span><span class="sxs-lookup"><span data-stu-id="c83c3-117">-FilterItem</span></span>
<span data-ttu-id="c83c3-118">필터의 항목 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="c83c3-118">List of items in the filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c83c3-119">-FilterType</span><span class="sxs-lookup"><span data-stu-id="c83c3-119">-FilterType</span></span>
<span data-ttu-id="c83c3-120">끝점 필터의 동작입니다.</span><span class="sxs-lookup"><span data-stu-id="c83c3-120">The behavior of the endpoint filter.</span></span> <span data-ttu-id="c83c3-121">현재는 ' Include '만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c83c3-121">Currently only 'Include' is supported.</span></span>

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

### <span data-ttu-id="c83c3-122">-이름</span><span class="sxs-lookup"><span data-stu-id="c83c3-122">-Name</span></span>
<span data-ttu-id="c83c3-123">연결 모니터 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c83c3-123">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="c83c3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c83c3-124">-ResourceId</span></span>
<span data-ttu-id="c83c3-125">연결 모니터 끝점의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c83c3-125">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c83c3-126">-확인</span><span class="sxs-lookup"><span data-stu-id="c83c3-126">-Confirm</span></span>
<span data-ttu-id="c83c3-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c83c3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c83c3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c83c3-128">-WhatIf</span></span>
<span data-ttu-id="c83c3-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c83c3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c83c3-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c83c3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c83c3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c83c3-131">CommonParameters</span></span>
<span data-ttu-id="c83c3-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c83c3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c83c3-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c83c3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c83c3-134">입력</span><span class="sxs-lookup"><span data-stu-id="c83c3-134">INPUTS</span></span>

### <span data-ttu-id="c83c3-135">않아야</span><span class="sxs-lookup"><span data-stu-id="c83c3-135">None</span></span>

## <span data-ttu-id="c83c3-136">출력</span><span class="sxs-lookup"><span data-stu-id="c83c3-136">OUTPUTS</span></span>

### <span data-ttu-id="c83c3-137">PSNetworkWatcherConnectionMonitorEndpointObject에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c83c3-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="c83c3-138">상속자</span><span class="sxs-lookup"><span data-stu-id="c83c3-138">NOTES</span></span>

## <span data-ttu-id="c83c3-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c83c3-139">RELATED LINKS</span></span>

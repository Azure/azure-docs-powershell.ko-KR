---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointfilteritemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
ms.openlocfilehash: c06052ee28d849c5d07a941366efd15cbfeefe25
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034492"
---
# <span data-ttu-id="e88fc-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span><span class="sxs-lookup"><span data-stu-id="e88fc-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span></span>

## <span data-ttu-id="e88fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e88fc-102">SYNOPSIS</span></span>
<span data-ttu-id="e88fc-103">연결 모니터 끝점 필터 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e88fc-103">Creates a connection monitor endpoint filter item.</span></span>

## <span data-ttu-id="e88fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e88fc-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e88fc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e88fc-105">DESCRIPTION</span></span>
<span data-ttu-id="e88fc-106">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject cmdlet은 끝점 필터 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e88fc-106">The New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject cmdlet creates endpoint filter item.</span></span>

## <span data-ttu-id="e88fc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e88fc-107">EXAMPLES</span></span>

### <span data-ttu-id="e88fc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e88fc-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "10.0.0.1"
```

<span data-ttu-id="e88fc-109">유형: AgentAddress 주소: 10.0.0.1</span><span class="sxs-lookup"><span data-stu-id="e88fc-109">Type    : AgentAddress Address : 10.0.0.1</span></span>

## <span data-ttu-id="e88fc-110">변수</span><span class="sxs-lookup"><span data-stu-id="e88fc-110">PARAMETERS</span></span>

### <span data-ttu-id="e88fc-111">-주소</span><span class="sxs-lookup"><span data-stu-id="e88fc-111">-Address</span></span>
<span data-ttu-id="e88fc-112">필터 항목의 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="e88fc-112">The address of the filter item.</span></span>

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

### <span data-ttu-id="e88fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88fc-113">-DefaultProfile</span></span>
<span data-ttu-id="e88fc-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e88fc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e88fc-115">-Type</span><span class="sxs-lookup"><span data-stu-id="e88fc-115">-Type</span></span>
<span data-ttu-id="e88fc-116">필터에 포함 된 항목의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e88fc-116">The type of item included in the filter.</span></span> <span data-ttu-id="e88fc-117">현재 ' AgentAddress '만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e88fc-117">Currently only 'AgentAddress' is supported.</span></span>

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

### <span data-ttu-id="e88fc-118">-확인</span><span class="sxs-lookup"><span data-stu-id="e88fc-118">-Confirm</span></span>
<span data-ttu-id="e88fc-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e88fc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e88fc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e88fc-120">-WhatIf</span></span>
<span data-ttu-id="e88fc-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e88fc-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e88fc-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e88fc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e88fc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88fc-123">CommonParameters</span></span>
<span data-ttu-id="e88fc-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e88fc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88fc-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e88fc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88fc-126">입력</span><span class="sxs-lookup"><span data-stu-id="e88fc-126">INPUTS</span></span>

### <span data-ttu-id="e88fc-127">않아야</span><span class="sxs-lookup"><span data-stu-id="e88fc-127">None</span></span>

## <span data-ttu-id="e88fc-128">출력</span><span class="sxs-lookup"><span data-stu-id="e88fc-128">OUTPUTS</span></span>

### <span data-ttu-id="e88fc-129">Microsoft. 네트워크. PSConnectionMonitorEndpointFilterItem</span><span class="sxs-lookup"><span data-stu-id="e88fc-129">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorEndpointFilterItem</span></span>

## <span data-ttu-id="e88fc-130">상속자</span><span class="sxs-lookup"><span data-stu-id="e88fc-130">NOTES</span></span>

## <span data-ttu-id="e88fc-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e88fc-131">RELATED LINKS</span></span>

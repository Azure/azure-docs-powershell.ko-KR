---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: c0ca9e257c0686aa0f4589ef4166fec150f41967
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334490"
---
# <span data-ttu-id="3dff6-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="3dff6-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="3dff6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dff6-102">SYNOPSIS</span></span>
<span data-ttu-id="3dff6-103">연결 모니터 엔드포인트 범위 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3dff6-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="3dff6-104">구문</span><span class="sxs-lookup"><span data-stu-id="3dff6-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dff6-105">설명</span><span class="sxs-lookup"><span data-stu-id="3dff6-105">DESCRIPTION</span></span>
<span data-ttu-id="3dff6-106">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet은 엔드포인트 범위 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3dff6-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="3dff6-107">예제</span><span class="sxs-lookup"><span data-stu-id="3dff6-107">EXAMPLES</span></span>

### <span data-ttu-id="3dff6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3dff6-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="3dff6-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dff6-109">PARAMETERS</span></span>

### <span data-ttu-id="3dff6-110">-Address</span><span class="sxs-lookup"><span data-stu-id="3dff6-110">-Address</span></span>
<span data-ttu-id="3dff6-111">범위 항목의 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="3dff6-111">The address of the scope item.</span></span>

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

### <span data-ttu-id="3dff6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dff6-112">-DefaultProfile</span></span>
<span data-ttu-id="3dff6-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3dff6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dff6-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dff6-114">-Confirm</span></span>
<span data-ttu-id="3dff6-115">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dff6-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dff6-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dff6-116">-WhatIf</span></span>
<span data-ttu-id="3dff6-117">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3dff6-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dff6-118">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3dff6-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dff6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dff6-119">CommonParameters</span></span>
<span data-ttu-id="3dff6-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3dff6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dff6-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3dff6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dff6-122">입력</span><span class="sxs-lookup"><span data-stu-id="3dff6-122">INPUTS</span></span>

### <span data-ttu-id="3dff6-123">없음</span><span class="sxs-lookup"><span data-stu-id="3dff6-123">None</span></span>

## <span data-ttu-id="3dff6-124">출력</span><span class="sxs-lookup"><span data-stu-id="3dff6-124">OUTPUTS</span></span>

### <span data-ttu-id="3dff6-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="3dff6-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="3dff6-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3dff6-126">NOTES</span></span>

## <span data-ttu-id="3dff6-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3dff6-127">RELATED LINKS</span></span>

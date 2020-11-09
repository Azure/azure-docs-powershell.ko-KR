---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: c0ca9e257c0686aa0f4589ef4166fec150f41967
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309212"
---
# <span data-ttu-id="2dce8-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="2dce8-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="2dce8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dce8-102">SYNOPSIS</span></span>
<span data-ttu-id="2dce8-103">연결 모니터 끝점 범위 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2dce8-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="2dce8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2dce8-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dce8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2dce8-105">DESCRIPTION</span></span>
<span data-ttu-id="2dce8-106">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet은 끝점 범위 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2dce8-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="2dce8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2dce8-107">EXAMPLES</span></span>

### <span data-ttu-id="2dce8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2dce8-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="2dce8-109">변수</span><span class="sxs-lookup"><span data-stu-id="2dce8-109">PARAMETERS</span></span>

### <span data-ttu-id="2dce8-110">-주소</span><span class="sxs-lookup"><span data-stu-id="2dce8-110">-Address</span></span>
<span data-ttu-id="2dce8-111">범위 항목의 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="2dce8-111">The address of the scope item.</span></span>

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

### <span data-ttu-id="2dce8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dce8-112">-DefaultProfile</span></span>
<span data-ttu-id="2dce8-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2dce8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dce8-114">-확인</span><span class="sxs-lookup"><span data-stu-id="2dce8-114">-Confirm</span></span>
<span data-ttu-id="2dce8-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dce8-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dce8-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dce8-116">-WhatIf</span></span>
<span data-ttu-id="2dce8-117">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2dce8-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dce8-118">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2dce8-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dce8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dce8-119">CommonParameters</span></span>
<span data-ttu-id="2dce8-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2dce8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dce8-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2dce8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dce8-122">입력</span><span class="sxs-lookup"><span data-stu-id="2dce8-122">INPUTS</span></span>

### <span data-ttu-id="2dce8-123">않아야</span><span class="sxs-lookup"><span data-stu-id="2dce8-123">None</span></span>

## <span data-ttu-id="2dce8-124">출력</span><span class="sxs-lookup"><span data-stu-id="2dce8-124">OUTPUTS</span></span>

### <span data-ttu-id="2dce8-125">PSNetworkWatcherConnectionMonitorEndpointScopeItem에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2dce8-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="2dce8-126">상속자</span><span class="sxs-lookup"><span data-stu-id="2dce8-126">NOTES</span></span>

## <span data-ttu-id="2dce8-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2dce8-127">RELATED LINKS</span></span>

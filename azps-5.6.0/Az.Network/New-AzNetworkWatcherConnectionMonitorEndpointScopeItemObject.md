---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: 298586f11bba29ce44e78bc3c19d4d9fc6be21f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958523"
---
# <span data-ttu-id="6262e-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="6262e-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="6262e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6262e-102">SYNOPSIS</span></span>
<span data-ttu-id="6262e-103">연결 모니터 엔드포인트 범위 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6262e-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="6262e-104">구문</span><span class="sxs-lookup"><span data-stu-id="6262e-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6262e-105">설명</span><span class="sxs-lookup"><span data-stu-id="6262e-105">DESCRIPTION</span></span>
<span data-ttu-id="6262e-106">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet은 엔드포인트 범위 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6262e-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="6262e-107">예제</span><span class="sxs-lookup"><span data-stu-id="6262e-107">EXAMPLES</span></span>

### <span data-ttu-id="6262e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6262e-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="6262e-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6262e-109">PARAMETERS</span></span>

### <span data-ttu-id="6262e-110">-address</span><span class="sxs-lookup"><span data-stu-id="6262e-110">-Address</span></span>
<span data-ttu-id="6262e-111">범위 항목의 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="6262e-111">The address of the scope item.</span></span>

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

### <span data-ttu-id="6262e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6262e-112">-DefaultProfile</span></span>
<span data-ttu-id="6262e-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6262e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6262e-114">-확인</span><span class="sxs-lookup"><span data-stu-id="6262e-114">-Confirm</span></span>
<span data-ttu-id="6262e-115">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6262e-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6262e-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6262e-116">-WhatIf</span></span>
<span data-ttu-id="6262e-117">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6262e-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6262e-118">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6262e-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6262e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6262e-119">CommonParameters</span></span>
<span data-ttu-id="6262e-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6262e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6262e-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6262e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6262e-122">입력</span><span class="sxs-lookup"><span data-stu-id="6262e-122">INPUTS</span></span>

### <span data-ttu-id="6262e-123">없음</span><span class="sxs-lookup"><span data-stu-id="6262e-123">None</span></span>

## <span data-ttu-id="6262e-124">출력</span><span class="sxs-lookup"><span data-stu-id="6262e-124">OUTPUTS</span></span>

### <span data-ttu-id="6262e-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="6262e-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="6262e-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6262e-126">NOTES</span></span>

## <span data-ttu-id="6262e-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6262e-127">RELATED LINKS</span></span>

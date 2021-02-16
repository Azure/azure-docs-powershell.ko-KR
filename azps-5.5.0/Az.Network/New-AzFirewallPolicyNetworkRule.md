---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206709"
---
# <span data-ttu-id="62c94-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="62c94-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="62c94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62c94-102">SYNOPSIS</span></span>
<span data-ttu-id="62c94-103">새 Azure Firewall 정책 네트워크 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="62c94-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="62c94-104">구문</span><span class="sxs-lookup"><span data-stu-id="62c94-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62c94-105">설명</span><span class="sxs-lookup"><span data-stu-id="62c94-105">DESCRIPTION</span></span>
<span data-ttu-id="62c94-106">**New-AzFirewallPolicyNetworkRule** cmdlet은 Azure Firewall 정책에 대한 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62c94-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="62c94-107">예제</span><span class="sxs-lookup"><span data-stu-id="62c94-107">EXAMPLES</span></span>

### <span data-ttu-id="62c94-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="62c94-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="62c94-109">이 예제에서는 원본 주소, 프로토콜, 대상 주소 및 대상 포트를 사용하여 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62c94-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="62c94-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62c94-110">PARAMETERS</span></span>

### <span data-ttu-id="62c94-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c94-111">-DefaultProfile</span></span>
<span data-ttu-id="62c94-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62c94-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c94-113">-Description</span><span class="sxs-lookup"><span data-stu-id="62c94-113">-Description</span></span>
<span data-ttu-id="62c94-114">규칙에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="62c94-114">The description of the rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c94-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="62c94-115">-DestinationAddress</span></span>
<span data-ttu-id="62c94-116">규칙의 대상 주소</span><span class="sxs-lookup"><span data-stu-id="62c94-116">The destination addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c94-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="62c94-117">-DestinationFqdn</span></span>
<span data-ttu-id="62c94-118">규칙의 대상 FQDN</span><span class="sxs-lookup"><span data-stu-id="62c94-118">The destination FQDN of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c94-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="62c94-119">-DestinationIpGroup</span></span>
<span data-ttu-id="62c94-120">규칙의 대상 ipgroups</span><span class="sxs-lookup"><span data-stu-id="62c94-120">The destination ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c94-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="62c94-121">-DestinationPort</span></span>
<span data-ttu-id="62c94-122">규칙의 대상 포트</span><span class="sxs-lookup"><span data-stu-id="62c94-122">The destination ports of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c94-123">-Name</span><span class="sxs-lookup"><span data-stu-id="62c94-123">-Name</span></span>
<span data-ttu-id="62c94-124">네트워크 규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="62c94-124">The name of the Network Rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c94-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="62c94-125">-Protocol</span></span>
<span data-ttu-id="62c94-126">규칙의 프로토콜</span><span class="sxs-lookup"><span data-stu-id="62c94-126">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP, ICMP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c94-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="62c94-127">-SourceAddress</span></span>
<span data-ttu-id="62c94-128">규칙의 원본 주소</span><span class="sxs-lookup"><span data-stu-id="62c94-128">The source addresses of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c94-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="62c94-129">-SourceIpGroup</span></span>
<span data-ttu-id="62c94-130">규칙의 원본 ipgroups</span><span class="sxs-lookup"><span data-stu-id="62c94-130">The source ipgroups of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c94-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62c94-131">-Confirm</span></span>
<span data-ttu-id="62c94-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="62c94-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c94-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62c94-133">-WhatIf</span></span>
<span data-ttu-id="62c94-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="62c94-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62c94-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62c94-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c94-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c94-136">CommonParameters</span></span>
<span data-ttu-id="62c94-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="62c94-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c94-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="62c94-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c94-139">입력</span><span class="sxs-lookup"><span data-stu-id="62c94-139">INPUTS</span></span>

### <span data-ttu-id="62c94-140">없음</span><span class="sxs-lookup"><span data-stu-id="62c94-140">None</span></span>

## <span data-ttu-id="62c94-141">출력</span><span class="sxs-lookup"><span data-stu-id="62c94-141">OUTPUTS</span></span>

### <span data-ttu-id="62c94-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="62c94-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="62c94-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="62c94-143">NOTES</span></span>

## <span data-ttu-id="62c94-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62c94-144">RELATED LINKS</span></span>

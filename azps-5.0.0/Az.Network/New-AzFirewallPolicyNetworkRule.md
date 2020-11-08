---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: 1cd87ecefdb2216e7fb77ffcaaf487fa13a5a565
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218319"
---
# <span data-ttu-id="165d9-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="165d9-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="165d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="165d9-102">SYNOPSIS</span></span>
<span data-ttu-id="165d9-103">새 Azure 방화벽 정책 네트워크 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="165d9-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="165d9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="165d9-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 [-SourceIpGroup <String[]>] -DestinationAddress <String[]> [-DestinationIpGroup <String[]>]
 -DestinationPort <String[]> [-DestinationFqdn <String[]>] -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="165d9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="165d9-105">DESCRIPTION</span></span>
<span data-ttu-id="165d9-106">**AzFirewallPolicyNetworkRule** Cmdlet은 Azure 방화벽 정책에 대 한 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="165d9-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="165d9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="165d9-107">EXAMPLES</span></span>

### <span data-ttu-id="165d9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="165d9-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="165d9-109">이 예제에서는 원본 주소, 프로토콜, 대상 주소 및 대상 포트를 사용 하 여 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="165d9-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="165d9-110">변수</span><span class="sxs-lookup"><span data-stu-id="165d9-110">PARAMETERS</span></span>

### <span data-ttu-id="165d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="165d9-111">-DefaultProfile</span></span>
<span data-ttu-id="165d9-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="165d9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="165d9-113">-설명</span><span class="sxs-lookup"><span data-stu-id="165d9-113">-Description</span></span>
<span data-ttu-id="165d9-114">규칙에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="165d9-114">The description of the rule</span></span>

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

### <span data-ttu-id="165d9-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="165d9-115">-DestinationAddress</span></span>
<span data-ttu-id="165d9-116">규칙의 대상 주소</span><span class="sxs-lookup"><span data-stu-id="165d9-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="165d9-117">-DestinationFqdn</span><span class="sxs-lookup"><span data-stu-id="165d9-117">-DestinationFqdn</span></span>
<span data-ttu-id="165d9-118">규칙의 대상 FQDN</span><span class="sxs-lookup"><span data-stu-id="165d9-118">The destination FQDN of the rule</span></span>

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

### <span data-ttu-id="165d9-119">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="165d9-119">-DestinationIpGroup</span></span>
<span data-ttu-id="165d9-120">규칙의 대상 ipgroups</span><span class="sxs-lookup"><span data-stu-id="165d9-120">The destination ipgroups of the rule</span></span>

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

### <span data-ttu-id="165d9-121">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="165d9-121">-DestinationPort</span></span>
<span data-ttu-id="165d9-122">규칙의 대상 포트</span><span class="sxs-lookup"><span data-stu-id="165d9-122">The destination ports of the rule</span></span>

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

### <span data-ttu-id="165d9-123">-이름</span><span class="sxs-lookup"><span data-stu-id="165d9-123">-Name</span></span>
<span data-ttu-id="165d9-124">네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="165d9-124">The name of the Network Rule</span></span>

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

### <span data-ttu-id="165d9-125">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="165d9-125">-Protocol</span></span>
<span data-ttu-id="165d9-126">규칙의 프로토콜</span><span class="sxs-lookup"><span data-stu-id="165d9-126">The protocols of the rule</span></span>

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

### <span data-ttu-id="165d9-127">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="165d9-127">-SourceAddress</span></span>
<span data-ttu-id="165d9-128">규칙의 원본 주소</span><span class="sxs-lookup"><span data-stu-id="165d9-128">The source addresses of the rule</span></span>

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

### <span data-ttu-id="165d9-129">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="165d9-129">-SourceIpGroup</span></span>
<span data-ttu-id="165d9-130">규칙의 원본 ipgroups</span><span class="sxs-lookup"><span data-stu-id="165d9-130">The source ipgroups of the rule</span></span>

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

### <span data-ttu-id="165d9-131">-확인</span><span class="sxs-lookup"><span data-stu-id="165d9-131">-Confirm</span></span>
<span data-ttu-id="165d9-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="165d9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="165d9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="165d9-133">-WhatIf</span></span>
<span data-ttu-id="165d9-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="165d9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="165d9-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="165d9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="165d9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="165d9-136">CommonParameters</span></span>
<span data-ttu-id="165d9-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="165d9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="165d9-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="165d9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="165d9-139">입력</span><span class="sxs-lookup"><span data-stu-id="165d9-139">INPUTS</span></span>

### <span data-ttu-id="165d9-140">않아야</span><span class="sxs-lookup"><span data-stu-id="165d9-140">None</span></span>

## <span data-ttu-id="165d9-141">출력</span><span class="sxs-lookup"><span data-stu-id="165d9-141">OUTPUTS</span></span>

### <span data-ttu-id="165d9-142">PSAzureFirewallNetworkRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="165d9-142">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="165d9-143">상속자</span><span class="sxs-lookup"><span data-stu-id="165d9-143">NOTES</span></span>

## <span data-ttu-id="165d9-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="165d9-144">RELATED LINKS</span></span>

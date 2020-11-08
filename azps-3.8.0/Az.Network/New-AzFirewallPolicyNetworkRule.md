---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNetworkRule.md
ms.openlocfilehash: b4cbc404139cd56e75f03c5cb19cb9b761576e39
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041817"
---
# <span data-ttu-id="82c4e-101">New-AzFirewallPolicyNetworkRule</span><span class="sxs-lookup"><span data-stu-id="82c4e-101">New-AzFirewallPolicyNetworkRule</span></span>

## <span data-ttu-id="82c4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82c4e-102">SYNOPSIS</span></span>
<span data-ttu-id="82c4e-103">새 Azure 방화벽 정책 네트워크 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="82c4e-103">Create a new Azure Firewall Policy Network Rule</span></span>

## <span data-ttu-id="82c4e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="82c4e-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNetworkRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocols <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82c4e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="82c4e-105">DESCRIPTION</span></span>
<span data-ttu-id="82c4e-106">**AzFirewallPolicyNetworkRule** Cmdlet은 Azure 방화벽 정책에 대 한 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82c4e-106">The **New-AzFirewallPolicyNetworkRule** cmdlet creates a Network rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="82c4e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="82c4e-107">EXAMPLES</span></span>

### <span data-ttu-id="82c4e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="82c4e-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNetworkRule -Name NRC1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress * -DestinationPort *
```

<span data-ttu-id="82c4e-109">이 예제에서는 원본 주소, 프로토콜, 대상 주소 및 대상 포트를 사용 하 여 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82c4e-109">This example creates an network rule with the source address, protocol , destination address and destination port</span></span>

## <span data-ttu-id="82c4e-110">변수</span><span class="sxs-lookup"><span data-stu-id="82c4e-110">PARAMETERS</span></span>

### <span data-ttu-id="82c4e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c4e-111">-DefaultProfile</span></span>
<span data-ttu-id="82c4e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82c4e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82c4e-113">-설명</span><span class="sxs-lookup"><span data-stu-id="82c4e-113">-Description</span></span>
<span data-ttu-id="82c4e-114">규칙에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="82c4e-114">The description of the rule</span></span>

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

### <span data-ttu-id="82c4e-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="82c4e-115">-DestinationAddress</span></span>
<span data-ttu-id="82c4e-116">규칙의 대상 주소</span><span class="sxs-lookup"><span data-stu-id="82c4e-116">The destination addresses of the rule</span></span>

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

### <span data-ttu-id="82c4e-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="82c4e-117">-DestinationPort</span></span>
<span data-ttu-id="82c4e-118">규칙의 대상 포트</span><span class="sxs-lookup"><span data-stu-id="82c4e-118">The destination ports of the rule</span></span>

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

### <span data-ttu-id="82c4e-119">-이름</span><span class="sxs-lookup"><span data-stu-id="82c4e-119">-Name</span></span>
<span data-ttu-id="82c4e-120">네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82c4e-120">The name of the Network Rule</span></span>

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

### <span data-ttu-id="82c4e-121">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="82c4e-121">-Protocols</span></span>
<span data-ttu-id="82c4e-122">규칙의 프로토콜</span><span class="sxs-lookup"><span data-stu-id="82c4e-122">The protocols of the rule</span></span>

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

### <span data-ttu-id="82c4e-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="82c4e-123">-SourceAddress</span></span>
<span data-ttu-id="82c4e-124">규칙의 원본 주소</span><span class="sxs-lookup"><span data-stu-id="82c4e-124">The source addresses of the rule</span></span>

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

### <span data-ttu-id="82c4e-125">-확인</span><span class="sxs-lookup"><span data-stu-id="82c4e-125">-Confirm</span></span>
<span data-ttu-id="82c4e-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c4e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82c4e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82c4e-127">-WhatIf</span></span>
<span data-ttu-id="82c4e-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="82c4e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82c4e-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82c4e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82c4e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c4e-130">CommonParameters</span></span>
<span data-ttu-id="82c4e-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="82c4e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c4e-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="82c4e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c4e-133">입력</span><span class="sxs-lookup"><span data-stu-id="82c4e-133">INPUTS</span></span>

### <span data-ttu-id="82c4e-134">않아야</span><span class="sxs-lookup"><span data-stu-id="82c4e-134">None</span></span>

## <span data-ttu-id="82c4e-135">출력</span><span class="sxs-lookup"><span data-stu-id="82c4e-135">OUTPUTS</span></span>

### <span data-ttu-id="82c4e-136">PSAzureFirewallNetworkRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="82c4e-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule</span></span>

## <span data-ttu-id="82c4e-137">상속자</span><span class="sxs-lookup"><span data-stu-id="82c4e-137">NOTES</span></span>

## <span data-ttu-id="82c4e-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82c4e-138">RELATED LINKS</span></span>

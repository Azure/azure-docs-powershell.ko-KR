---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicynatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRule.md
ms.openlocfilehash: 2ba006beef1c698c12086ef65efca0213920092c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987793"
---
# <span data-ttu-id="f626d-101">New-AzFirewallPolicyNatRule</span><span class="sxs-lookup"><span data-stu-id="f626d-101">New-AzFirewallPolicyNatRule</span></span>

## <span data-ttu-id="f626d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f626d-102">SYNOPSIS</span></span>
<span data-ttu-id="f626d-103">새 Azure 방화벽 정책 NAT 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="f626d-103">Create a new Azure Firewall Policy NAT Rule</span></span>

## <span data-ttu-id="f626d-104">구문</span><span class="sxs-lookup"><span data-stu-id="f626d-104">SYNTAX</span></span>

### <span data-ttu-id="f626d-105">SourceAddressAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="f626d-105">SourceAddressAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f626d-106">SourceAddressAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="f626d-106">SourceAddressAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f626d-107">SourceIpGroupAndTranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="f626d-107">SourceIpGroupAndTranslatedAddress</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f626d-108">SourceIpGroupAndTranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="f626d-108">SourceIpGroupAndTranslatedFqdn</span></span>
```
New-AzFirewallPolicyNatRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedFqdn <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f626d-109">설명</span><span class="sxs-lookup"><span data-stu-id="f626d-109">DESCRIPTION</span></span>
<span data-ttu-id="f626d-110">**New-AzFirewallPolicyNatRule** cmdlet은 Azure 방화벽 정책에 대한 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f626d-110">The **New-AzFirewallPolicyNatRule** cmdlet creates a NAT rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="f626d-111">예제</span><span class="sxs-lookup"><span data-stu-id="f626d-111">EXAMPLES</span></span>

### <span data-ttu-id="f626d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="f626d-112">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="f626d-113">이 예제에서는 원본 주소, 프로토콜, 대상 주소, 대상 포트, 번역된 주소 및 번역된 포트를 사용하여 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f626d-113">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated address, and translated port.</span></span>

### <span data-ttu-id="f626d-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="f626d-114">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRule -Name NatRule1 -Protocol "TCP" -SourceAddress "192.168.0.0/16" -DestinationAddress 10.20.30.40 -DestinationPort 1000 -TranslatedFqdn "internalhttp.server.net" -TranslatedPort "100"
```

<span data-ttu-id="f626d-115">이 예제에서는 원본 주소, 프로토콜, 대상 주소, 대상 포트, 번역된 fqdn 및 번역된 포트를 사용하여 NAT 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f626d-115">This example creates a NAT rule with the source address, protocol, destination address, destination port, translated fqdn, and translated port.</span></span>

## <span data-ttu-id="f626d-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f626d-116">PARAMETERS</span></span>

### <span data-ttu-id="f626d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f626d-117">-DefaultProfile</span></span>
<span data-ttu-id="f626d-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f626d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f626d-119">-Description</span><span class="sxs-lookup"><span data-stu-id="f626d-119">-Description</span></span>
<span data-ttu-id="f626d-120">규칙에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="f626d-120">The description of the rule</span></span>

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

### <span data-ttu-id="f626d-121">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="f626d-121">-DestinationAddress</span></span>
<span data-ttu-id="f626d-122">규칙의 대상 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="f626d-122">The destination addresses of the rule.</span></span> <span data-ttu-id="f626d-123">방화벽의 공용 IP가 됐습니다.</span><span class="sxs-lookup"><span data-stu-id="f626d-123">This has to be Public IP of the Firewall.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f626d-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="f626d-124">-DestinationPort</span></span>
<span data-ttu-id="f626d-125">규칙의 대상 포트</span><span class="sxs-lookup"><span data-stu-id="f626d-125">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f626d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f626d-126">-Name</span></span>
<span data-ttu-id="f626d-127">NAT 규칙 컬렉션의 이름</span><span class="sxs-lookup"><span data-stu-id="f626d-127">The name of the NAT Rule Collection</span></span>

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

### <span data-ttu-id="f626d-128">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f626d-128">-Protocol</span></span>
<span data-ttu-id="f626d-129">규칙의 프로토콜</span><span class="sxs-lookup"><span data-stu-id="f626d-129">The protocols of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f626d-130">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="f626d-130">-SourceAddress</span></span>
<span data-ttu-id="f626d-131">규칙의 원본 주소</span><span class="sxs-lookup"><span data-stu-id="f626d-131">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTranslatedAddress, SourceAddressAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f626d-132">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="f626d-132">-SourceIpGroup</span></span>
<span data-ttu-id="f626d-133">규칙의 원본 ipgroups</span><span class="sxs-lookup"><span data-stu-id="f626d-133">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTranslatedAddress, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f626d-134">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="f626d-134">-TranslatedAddress</span></span>
<span data-ttu-id="f626d-135">이 NAT 규칙에 대한 번역된 주소</span><span class="sxs-lookup"><span data-stu-id="f626d-135">The translated address for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedAddress, SourceIpGroupAndTranslatedAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f626d-136">-TranslatedFqdn</span><span class="sxs-lookup"><span data-stu-id="f626d-136">-TranslatedFqdn</span></span>
<span data-ttu-id="f626d-137">이 NAT 규칙에 대한 번역된 FQDN</span><span class="sxs-lookup"><span data-stu-id="f626d-137">The translated FQDN for this NAT rule</span></span>

```yaml
Type: System.String
Parameter Sets: SourceAddressAndTranslatedFqdn, SourceIpGroupAndTranslatedFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f626d-138">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="f626d-138">-TranslatedPort</span></span>
<span data-ttu-id="f626d-139">이 NAT 규칙에 대한 번역된 포트</span><span class="sxs-lookup"><span data-stu-id="f626d-139">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="f626d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f626d-140">CommonParameters</span></span>
<span data-ttu-id="f626d-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f626d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f626d-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f626d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f626d-143">입력</span><span class="sxs-lookup"><span data-stu-id="f626d-143">INPUTS</span></span>

### <span data-ttu-id="f626d-144">없음</span><span class="sxs-lookup"><span data-stu-id="f626d-144">None</span></span>

## <span data-ttu-id="f626d-145">출력</span><span class="sxs-lookup"><span data-stu-id="f626d-145">OUTPUTS</span></span>

### <span data-ttu-id="f626d-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="f626d-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="f626d-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f626d-147">NOTES</span></span>

## <span data-ttu-id="f626d-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f626d-148">RELATED LINKS</span></span>

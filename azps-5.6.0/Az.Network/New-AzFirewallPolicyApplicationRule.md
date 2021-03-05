---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 0c7e29b0c9b59842e885cf8763da63c2d65cfff2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001115"
---
# <span data-ttu-id="b2bfc-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="b2bfc-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="b2bfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2bfc-102">SYNOPSIS</span></span>
<span data-ttu-id="b2bfc-103">새 Azure 방화벽 정책 애플리케이션 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="b2bfc-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="b2bfc-104">구문</span><span class="sxs-lookup"><span data-stu-id="b2bfc-104">SYNTAX</span></span>

### <span data-ttu-id="b2bfc-105">SourceAddressAndTargetFqdn(기본값)</span><span class="sxs-lookup"><span data-stu-id="b2bfc-105">SourceAddressAndTargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2bfc-106">SourceAddressAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="b2bfc-106">SourceAddressAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2bfc-107">SourceAddressAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="b2bfc-107">SourceAddressAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2bfc-108">SourceAddressAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="b2bfc-108">SourceAddressAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2bfc-109">SourceIpGroupAndTargetUrl</span><span class="sxs-lookup"><span data-stu-id="b2bfc-109">SourceIpGroupAndTargetUrl</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetUrl <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2bfc-110">SourceIpGroupAndTargetFqdn</span><span class="sxs-lookup"><span data-stu-id="b2bfc-110">SourceIpGroupAndTargetFqdn</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2bfc-111">SourceIpGroupAndFqdnTag</span><span class="sxs-lookup"><span data-stu-id="b2bfc-111">SourceIpGroupAndFqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2bfc-112">SourceIpGroupAndWebCategory</span><span class="sxs-lookup"><span data-stu-id="b2bfc-112">SourceIpGroupAndWebCategory</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] -SourceIpGroup <String[]>
 -WebCategory <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2bfc-113">설명</span><span class="sxs-lookup"><span data-stu-id="b2bfc-113">DESCRIPTION</span></span>
<span data-ttu-id="b2bfc-114">**New-AzFirewallPolicyApplicationRule** cmdlet은 Azure 방화벽 정책에 대한 애플리케이션 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2bfc-114">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="b2bfc-115">예제</span><span class="sxs-lookup"><span data-stu-id="b2bfc-115">EXAMPLES</span></span>

### <span data-ttu-id="b2bfc-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="b2bfc-116">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="b2bfc-117">이 예제에서는 원본 주소, 프로토콜 및 대상 fqdns를 사용하여 애플리케이션 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2bfc-117">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

### <span data-ttu-id="b2bfc-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="b2bfc-118">Example 2</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -WebCategory "DatingAndPersonals", "Tasteless"
```

<span data-ttu-id="b2bfc-119">이 예제에서는 원본 주소, 프로토콜 및 웹 범주를 사용하여 애플리케이션 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2bfc-119">This example creates an application rule with the source address, protocol and web categories.</span></span>

## <span data-ttu-id="b2bfc-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b2bfc-120">PARAMETERS</span></span>

### <span data-ttu-id="b2bfc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2bfc-121">-DefaultProfile</span></span>
<span data-ttu-id="b2bfc-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2bfc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2bfc-123">-Description</span><span class="sxs-lookup"><span data-stu-id="b2bfc-123">-Description</span></span>
<span data-ttu-id="b2bfc-124">규칙에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="b2bfc-124">The description of the rule</span></span>

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

### <span data-ttu-id="b2bfc-125">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="b2bfc-125">-FqdnTag</span></span>
<span data-ttu-id="b2bfc-126">규칙의 FQDN 태그</span><span class="sxs-lookup"><span data-stu-id="b2bfc-126">The FQDN Tags of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndFqdnTag, SourceIpGroupAndFqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2bfc-127">-Name</span><span class="sxs-lookup"><span data-stu-id="b2bfc-127">-Name</span></span>
<span data-ttu-id="b2bfc-128">애플리케이션 규칙의 이름</span><span class="sxs-lookup"><span data-stu-id="b2bfc-128">The name of the Application Rule</span></span>

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

### <span data-ttu-id="b2bfc-129">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b2bfc-129">-Protocol</span></span>
<span data-ttu-id="b2bfc-130">규칙의 프로토콜</span><span class="sxs-lookup"><span data-stu-id="b2bfc-130">The protocols of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndWebCategory, SourceIpGroupAndTargetFqdn, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2bfc-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="b2bfc-131">-SourceAddress</span></span>
<span data-ttu-id="b2bfc-132">규칙의 원본 주소</span><span class="sxs-lookup"><span data-stu-id="b2bfc-132">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceAddressAndFqdnTag, SourceAddressAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2bfc-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="b2bfc-133">-SourceIpGroup</span></span>
<span data-ttu-id="b2bfc-134">규칙의 원본 ipgroups</span><span class="sxs-lookup"><span data-stu-id="b2bfc-134">The source ipgroups of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceIpGroupAndTargetFqdn, SourceIpGroupAndFqdnTag, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2bfc-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="b2bfc-135">-TargetFqdn</span></span>
<span data-ttu-id="b2bfc-136">규칙의 대상 FQDNS</span><span class="sxs-lookup"><span data-stu-id="b2bfc-136">The target FQDNs of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetFqdn, SourceIpGroupAndTargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2bfc-137">-WebCategory</span><span class="sxs-lookup"><span data-stu-id="b2bfc-137">-WebCategory</span></span>
<span data-ttu-id="b2bfc-138">규칙의 웹 범주</span><span class="sxs-lookup"><span data-stu-id="b2bfc-138">The Web Categories of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndWebCategory, SourceIpGroupAndWebCategory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2bfc-139">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="b2bfc-139">-TargetUrl</span></span>
<span data-ttu-id="b2bfc-140">규칙의 대상 URL</span><span class="sxs-lookup"><span data-stu-id="b2bfc-140">The Target Url of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: SourceAddressAndTargetUrl, SourceIpGroupAndTargetUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2bfc-141">-TerminateTLS</span><span class="sxs-lookup"><span data-stu-id="b2bfc-141">-TerminateTLS</span></span>
<span data-ttu-id="b2bfc-142">TLS 종료를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b2bfc-142">Indicates terminating TLS</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2bfc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2bfc-143">CommonParameters</span></span>
<span data-ttu-id="b2bfc-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b2bfc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2bfc-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2bfc-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2bfc-146">입력</span><span class="sxs-lookup"><span data-stu-id="b2bfc-146">INPUTS</span></span>

### <span data-ttu-id="b2bfc-147">없음</span><span class="sxs-lookup"><span data-stu-id="b2bfc-147">None</span></span>

## <span data-ttu-id="b2bfc-148">출력</span><span class="sxs-lookup"><span data-stu-id="b2bfc-148">OUTPUTS</span></span>

### <span data-ttu-id="b2bfc-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="b2bfc-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="b2bfc-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b2bfc-150">NOTES</span></span>

## <span data-ttu-id="b2bfc-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2bfc-151">RELATED LINKS</span></span>

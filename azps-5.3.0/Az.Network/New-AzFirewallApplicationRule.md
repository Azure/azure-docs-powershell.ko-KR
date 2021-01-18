---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: d5c3a560f0afcfb28224cf4681af78d6bd5249ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492633"
---
# <span data-ttu-id="53543-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="53543-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="53543-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53543-102">SYNOPSIS</span></span>
<span data-ttu-id="53543-103">방화벽 애플리케이션 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53543-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="53543-104">구문</span><span class="sxs-lookup"><span data-stu-id="53543-104">SYNTAX</span></span>

### <span data-ttu-id="53543-105">TargetFqdn(기본값)</span><span class="sxs-lookup"><span data-stu-id="53543-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -TargetFqdn <String[]> -Protocol <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53543-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="53543-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 [-SourceIpGroup <String[]>] -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53543-107">설명</span><span class="sxs-lookup"><span data-stu-id="53543-107">DESCRIPTION</span></span>
<span data-ttu-id="53543-108">**New-AzFirewallApplicationRule** cmdlet은 Azure Firewall에 대한 애플리케이션 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53543-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="53543-109">예제</span><span class="sxs-lookup"><span data-stu-id="53543-109">EXAMPLES</span></span>

### <span data-ttu-id="53543-110">예제 1: 10.0.0.0에서 모든 HTTPS 트래픽을 허용하는 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="53543-110">Example 1: Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```powershell
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="53543-111">이 예제에서는 10.0.0.0에서 포트 443의 모든 HTTPS 트래픽을 허용하는 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53543-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="53543-112">예제 2: 10.0.0.0/24 서브넷에 WindowsUpdate를 허용하는 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="53543-112">Example 2: Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```powershell
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="53543-113">이 예제에서는 10.0.0.0/24 도메인에 대한 Windows 업데이트에 대한 트래픽을 허용하는 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53543-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="53543-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53543-114">PARAMETERS</span></span>

### <span data-ttu-id="53543-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53543-115">-DefaultProfile</span></span>
<span data-ttu-id="53543-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53543-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53543-117">-Description</span><span class="sxs-lookup"><span data-stu-id="53543-117">-Description</span></span>
<span data-ttu-id="53543-118">이 규칙에 대한 선택적 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53543-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="53543-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="53543-119">-FqdnTag</span></span>
<span data-ttu-id="53543-120">이 규칙에 대한 FQDN 태그 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53543-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="53543-121">[Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet을 사용하여 사용 가능한 태그를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="53543-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53543-122">-Name</span><span class="sxs-lookup"><span data-stu-id="53543-122">-Name</span></span>
<span data-ttu-id="53543-123">이 애플리케이션 규칙의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53543-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="53543-124">이름은 규칙 컬렉션 내에서 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="53543-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="53543-125">-Protocol</span><span class="sxs-lookup"><span data-stu-id="53543-125">-Protocol</span></span>
<span data-ttu-id="53543-126">이 규칙에 따라 필터링할 트래픽 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53543-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="53543-127">형식은 <protocol type> : <port> .</span><span class="sxs-lookup"><span data-stu-id="53543-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="53543-128">예를 들어 "http:80" 또는 "https:443"입니다.</span><span class="sxs-lookup"><span data-stu-id="53543-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="53543-129">TargetFqdn을 사용할 때 프로토콜은 필수이지만 FqdnTag와 함께 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="53543-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="53543-130">지원되는 프로토콜은 HTTP 및 HTTPS입니다.</span><span class="sxs-lookup"><span data-stu-id="53543-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53543-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="53543-131">-SourceAddress</span></span>
<span data-ttu-id="53543-132">규칙의 원본 주소</span><span class="sxs-lookup"><span data-stu-id="53543-132">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53543-133">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="53543-133">-SourceIpGroup</span></span>
<span data-ttu-id="53543-134">규칙의 원본 ipgroup</span><span class="sxs-lookup"><span data-stu-id="53543-134">The source ipgroup of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53543-135">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="53543-135">-TargetFqdn</span></span>
<span data-ttu-id="53543-136">이 규칙으로 필터링된 도메인 이름 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53543-136">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="53543-137">목록에서 FQDN의 첫 번째 문자로만 허용되는 추가 문자 *''입니다. 이 경우, 이 문자는 모든 수의 문자와 일치합니다. (예:*'msn.com'는 msn.com 모든 하위 msn.com 일치합니다.)</span><span class="sxs-lookup"><span data-stu-id="53543-137">The asterisk character, '*', is accepted only as the first character of an FQDN in the list. When used, the asterisk matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53543-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53543-138">-Confirm</span></span>
<span data-ttu-id="53543-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="53543-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53543-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53543-140">-WhatIf</span></span>
<span data-ttu-id="53543-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="53543-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53543-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53543-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53543-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53543-143">CommonParameters</span></span>
<span data-ttu-id="53543-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="53543-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53543-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="53543-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53543-146">입력</span><span class="sxs-lookup"><span data-stu-id="53543-146">INPUTS</span></span>

### <span data-ttu-id="53543-147">없음</span><span class="sxs-lookup"><span data-stu-id="53543-147">None</span></span>

## <span data-ttu-id="53543-148">출력</span><span class="sxs-lookup"><span data-stu-id="53543-148">OUTPUTS</span></span>

### <span data-ttu-id="53543-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="53543-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="53543-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="53543-150">NOTES</span></span>

## <span data-ttu-id="53543-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53543-151">RELATED LINKS</span></span>

[<span data-ttu-id="53543-152">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="53543-152">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="53543-153">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="53543-153">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="53543-154">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="53543-154">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="53543-155">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="53543-155">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)

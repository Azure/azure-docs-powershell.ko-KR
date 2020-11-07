---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRule.md
ms.openlocfilehash: 6aad78a873b1eb24f1534c9b8c0b38d1567ee2ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700344"
---
# <span data-ttu-id="e4e4c-101">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="e4e4c-101">New-AzFirewallApplicationRule</span></span>

## <span data-ttu-id="e4e4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e4c-103">방화벽 응용 프로그램 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-103">Creates a Firewall Application Rule.</span></span>

## <span data-ttu-id="e4e4c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e4e4c-104">SYNTAX</span></span>

### <span data-ttu-id="e4e4c-105">TargetFqdn (기본값)</span><span class="sxs-lookup"><span data-stu-id="e4e4c-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4e4c-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="e4e4c-106">FqdnTag</span></span>
```
New-AzFirewallApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4e4c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e4e4c-107">DESCRIPTION</span></span>
<span data-ttu-id="e4e4c-108">**AzFirewallApplicationRule** Cmdlet은 Azure 방화벽에 대 한 응용 프로그램 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-108">The **New-AzFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="e4e4c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e4e4c-109">EXAMPLES</span></span>

### <span data-ttu-id="e4e4c-110">1:10.0.0.0의 모든 HTTPS 트래픽을 허용 하는 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-110">1:  Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```
New-AzFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="e4e4c-111">이 예제는 10.0.0.0에서 포트 443의 모든 HTTPS 트래픽을 허용 하는 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="e4e4c-112">2:10.0.0.0/24 서브넷에 대 한 Windows을 허용 하는 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-112">2:  Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```
New-AzFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="e4e4c-113">이 예제에서는 10.0.0.0/24 도메인에 대 한 Windows 업데이트에 대 한 트래픽을 허용 하는 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="e4e4c-114">변수</span><span class="sxs-lookup"><span data-stu-id="e4e4c-114">PARAMETERS</span></span>

### <span data-ttu-id="e4e4c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4e4c-115">-DefaultProfile</span></span>
<span data-ttu-id="e4e4c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4e4c-117">-설명</span><span class="sxs-lookup"><span data-stu-id="e4e4c-117">-Description</span></span>
<span data-ttu-id="e4e4c-118">이 규칙에 대 한 설명을 선택적으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="e4e4c-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="e4e4c-119">-FqdnTag</span></span>
<span data-ttu-id="e4e4c-120">이 규칙에 대 한 FQDN 태그 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="e4e4c-121">[AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet을 사용 하 여 사용 가능한 태그를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-121">The available tags can be retrieved using [Get-AzFirewallFqdnTag](./Get-AzFirewallFqdnTag.md) cmdlet.</span></span>

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

### <span data-ttu-id="e4e4c-122">-이름</span><span class="sxs-lookup"><span data-stu-id="e4e4c-122">-Name</span></span>
<span data-ttu-id="e4e4c-123">이 응용 프로그램 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="e4e4c-124">이름은 규칙 컬렉션 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="e4e4c-125">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="e4e4c-125">-Protocol</span></span>
<span data-ttu-id="e4e4c-126">이 규칙에 따라 필터링 할 트래픽 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="e4e4c-127">형식은 <protocol type> 다음과 같습니다. <port></span><span class="sxs-lookup"><span data-stu-id="e4e4c-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="e4e4c-128">예를 들어 "http: 80" 또는 "https: 443"입니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="e4e4c-129">프로토콜은 TargetFqdn을 사용 하지만 FqdnTag와 함께 사용할 수 없는 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="e4e4c-130">지원 되는 프로토콜은 HTTP 및 HTTPS입니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-130">The supported protocols are HTTP and HTTPS.</span></span>

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

### <span data-ttu-id="e4e4c-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="e4e4c-131">-SourceAddress</span></span>
<span data-ttu-id="e4e4c-132">규칙의 원본 주소</span><span class="sxs-lookup"><span data-stu-id="e4e4c-132">The source addresses of the rule</span></span>

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

### <span data-ttu-id="e4e4c-133">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="e4e4c-133">-TargetFqdn</span></span>
<span data-ttu-id="e4e4c-134">이 규칙에 따라 필터링 된 도메인 이름 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-134">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="e4e4c-135">별표 문자 ' '은 (는) *목록에 있는 FQDN의 첫 문자로만 허용 됩니다. 사용 되는 경우 별표는 임의 개수의 문자와 일치 합니다. (예: '* msn.com '는 msn.com와 모든 하위 도메인)</span><span class="sxs-lookup"><span data-stu-id="e4e4c-135">The asterik character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterik matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

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

### <span data-ttu-id="e4e4c-136">-확인</span><span class="sxs-lookup"><span data-stu-id="e4e4c-136">-Confirm</span></span>
<span data-ttu-id="e4e4c-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4e4c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4e4c-138">-WhatIf</span></span>
<span data-ttu-id="e4e4c-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4e4c-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4e4c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e4c-141">CommonParameters</span></span>
<span data-ttu-id="e4e4c-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e4c-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4e4c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e4c-144">입력</span><span class="sxs-lookup"><span data-stu-id="e4e4c-144">INPUTS</span></span>

### <span data-ttu-id="e4e4c-145">않아야</span><span class="sxs-lookup"><span data-stu-id="e4e4c-145">None</span></span>

## <span data-ttu-id="e4e4c-146">출력</span><span class="sxs-lookup"><span data-stu-id="e4e4c-146">OUTPUTS</span></span>

### <span data-ttu-id="e4e4c-147">PSAzureFirewallApplicationRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule</span></span>

## <span data-ttu-id="e4e4c-148">상속자</span><span class="sxs-lookup"><span data-stu-id="e4e4c-148">NOTES</span></span>

## <span data-ttu-id="e4e4c-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4e4c-149">RELATED LINKS</span></span>

[<span data-ttu-id="e4e4c-150">새로운 AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e4e4c-150">New-AzFirewallApplicationRuleCollection</span></span>](./New-AzFirewallApplicationRuleCollection.md)

[<span data-ttu-id="e4e4c-151">새로운 AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e4e4c-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="e4e4c-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e4e4c-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="e4e4c-153">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="e4e4c-153">Get-AzFirewallFqdnTag</span></span>](./Get-AzFirewallFqdnTag.md)

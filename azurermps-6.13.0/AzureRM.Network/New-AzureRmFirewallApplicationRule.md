---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRule.md
ms.openlocfilehash: 8a59f09184c7042b12abbd549398ca4690ace235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711334"
---
# <span data-ttu-id="09353-101">New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="09353-101">New-AzureRmFirewallApplicationRule</span></span>

## <span data-ttu-id="09353-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09353-102">SYNOPSIS</span></span>
<span data-ttu-id="09353-103">방화벽 응용 프로그램 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="09353-103">Creates a Firewall Application Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09353-104">구문과</span><span class="sxs-lookup"><span data-stu-id="09353-104">SYNTAX</span></span>

### <span data-ttu-id="09353-105">TargetFqdn (기본값)</span><span class="sxs-lookup"><span data-stu-id="09353-105">TargetFqdn (Default)</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -TargetFqdn <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09353-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="09353-106">FqdnTag</span></span>
```
New-AzureRmFirewallApplicationRule -Name <String> [-Description <String>]
 [-SourceAddress <System.Collections.Generic.List`1[System.String]>]
 -FqdnTag <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09353-107">설명은</span><span class="sxs-lookup"><span data-stu-id="09353-107">DESCRIPTION</span></span>
<span data-ttu-id="09353-108">**AzureRmFirewallApplicationRule** Cmdlet은 Azure 방화벽에 대 한 응용 프로그램 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="09353-108">The **New-AzureRmFirewallApplicationRule** cmdlet creates an application rule for Azure Firewall.</span></span>

## <span data-ttu-id="09353-109">예제의</span><span class="sxs-lookup"><span data-stu-id="09353-109">EXAMPLES</span></span>

### <span data-ttu-id="09353-110">1:10.0.0.0의 모든 HTTPS 트래픽을 허용 하는 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="09353-110">1:  Create a rule to allow all HTTPS traffic from 10.0.0.0</span></span>
```
New-AzureRmFirewallApplicationRule -Name "https-rule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
```

<span data-ttu-id="09353-111">이 예제는 10.0.0.0에서 포트 443의 모든 HTTPS 트래픽을 허용 하는 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="09353-111">This example creates a rule which will allow all HTTPS traffic on port 443 from 10.0.0.0.</span></span>

### <span data-ttu-id="09353-112">2:10.0.0.0/24 서브넷에 대 한 Windows을 허용 하는 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="09353-112">2:  Create a rule to allow WindowsUpdate for 10.0.0.0/24 subnet</span></span>
```
New-AzureRmFirewallApplicationRule -Name "windows-update-rule" -FqdnTag WindowsUpdate -SourceAddress "10.0.0.0/24"
```

<span data-ttu-id="09353-113">이 예제에서는 10.0.0.0/24 도메인에 대 한 Windows 업데이트에 대 한 트래픽을 허용 하는 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="09353-113">This example creates a rule which will allow traffic for Windows Updates for 10.0.0.0/24 domain.</span></span>

## <span data-ttu-id="09353-114">변수</span><span class="sxs-lookup"><span data-stu-id="09353-114">PARAMETERS</span></span>

### <span data-ttu-id="09353-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09353-115">-DefaultProfile</span></span>
<span data-ttu-id="09353-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09353-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09353-117">-설명</span><span class="sxs-lookup"><span data-stu-id="09353-117">-Description</span></span>
<span data-ttu-id="09353-118">이 규칙에 대 한 설명을 선택적으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09353-118">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="09353-119">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="09353-119">-FqdnTag</span></span>
<span data-ttu-id="09353-120">이 규칙에 대 한 FQDN 태그 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09353-120">Specifies a list of FQDN Tags for this rule.</span></span> <span data-ttu-id="09353-121">[AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) cmdlet을 사용 하 여 사용 가능한 태그를 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09353-121">The available tags can be retrieved using [Get-AzureRmFirewallFqdnTag](./Get-AzureRmFirewallFqdnTag.md) cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09353-122">-이름</span><span class="sxs-lookup"><span data-stu-id="09353-122">-Name</span></span>
<span data-ttu-id="09353-123">이 응용 프로그램 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09353-123">Specifies the name of this application rule.</span></span> <span data-ttu-id="09353-124">이름은 규칙 컬렉션 내에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="09353-124">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="09353-125">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="09353-125">-Protocol</span></span>
<span data-ttu-id="09353-126">이 규칙에 따라 필터링 할 트래픽 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09353-126">Specifies the type of traffic to be filtered by this rule.</span></span> <span data-ttu-id="09353-127">형식은 <protocol type> 다음과 같습니다. <port></span><span class="sxs-lookup"><span data-stu-id="09353-127">The format is <protocol type>:<port>.</span></span> <span data-ttu-id="09353-128">예를 들어 "http: 80" 또는 "https: 443"입니다.</span><span class="sxs-lookup"><span data-stu-id="09353-128">For example, "http:80" or "https:443".</span></span>
<span data-ttu-id="09353-129">프로토콜은 TargetFqdn을 사용 하지만 FqdnTag와 함께 사용할 수 없는 경우 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="09353-129">Protocol is mandatory when TargetFqdn is used, but it cannot be used with FqdnTag.</span></span> <span data-ttu-id="09353-130">지원 되는 프로토콜은 HTTP 및 HTTPS입니다.</span><span class="sxs-lookup"><span data-stu-id="09353-130">The supported protocols are HTTP and HTTPS.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09353-131">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="09353-131">-SourceAddress</span></span>
<span data-ttu-id="09353-132">규칙의 원본 주소</span><span class="sxs-lookup"><span data-stu-id="09353-132">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09353-133">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="09353-133">-TargetFqdn</span></span>
<span data-ttu-id="09353-134">이 규칙에 따라 필터링 된 도메인 이름 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09353-134">Specifies a list of domain names filtered by this rule.</span></span>
<span data-ttu-id="09353-135">별표 문자 ' '은 (는) *목록에 있는 FQDN의 첫 문자로만 허용 됩니다. 사용 되는 경우 별표는 임의 개수의 문자와 일치 합니다. (예: '* msn.com '는 msn.com와 모든 하위 도메인)</span><span class="sxs-lookup"><span data-stu-id="09353-135">The asterik character, ' *', is accepted only as the first character of an FQDN in the list. When used, the asterik matches any number of characters. (e.g. '* msn.com' will match msn.com and all its subdomains)</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09353-136">-확인</span><span class="sxs-lookup"><span data-stu-id="09353-136">-Confirm</span></span>
<span data-ttu-id="09353-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="09353-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09353-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09353-138">-WhatIf</span></span>
<span data-ttu-id="09353-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="09353-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09353-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="09353-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09353-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09353-141">CommonParameters</span></span>
<span data-ttu-id="09353-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="09353-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09353-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09353-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09353-144">입력</span><span class="sxs-lookup"><span data-stu-id="09353-144">INPUTS</span></span>

### <span data-ttu-id="09353-145">않아야</span><span class="sxs-lookup"><span data-stu-id="09353-145">None</span></span>
<span data-ttu-id="09353-146">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="09353-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="09353-147">출력</span><span class="sxs-lookup"><span data-stu-id="09353-147">OUTPUTS</span></span>

### <span data-ttu-id="09353-148">PSFirewallApplicationRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="09353-148">Microsoft.Azure.Commands.Network.Models.PSFirewallApplicationRule</span></span>

## <span data-ttu-id="09353-149">상속자</span><span class="sxs-lookup"><span data-stu-id="09353-149">NOTES</span></span>

## <span data-ttu-id="09353-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09353-150">RELATED LINKS</span></span>

[<span data-ttu-id="09353-151">새로운 AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="09353-151">New-AzureRmFirewallApplicationRuleCollection</span></span>](./New-AzureRmFirewallApplicationRuleCollection.md)

[<span data-ttu-id="09353-152">새로운 AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="09353-152">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="09353-153">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="09353-153">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="09353-154">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="09353-154">Get-AzureRmFirewallFqdnTag</span></span>](./Get-AzureRmFirewallFqdnTag.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyapplicationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyApplicationRule.md
ms.openlocfilehash: 1b9fd10e11cb283f880979e7e4a5d703521c9a87
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877257"
---
# <span data-ttu-id="f9f96-101">New-AzFirewallPolicyApplicationRule</span><span class="sxs-lookup"><span data-stu-id="f9f96-101">New-AzFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="f9f96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9f96-102">SYNOPSIS</span></span>
<span data-ttu-id="f9f96-103">새 Azure 방화벽 정책 응용 프로그램 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="f9f96-103">Create a new Azure Firewall Policy Application Rule</span></span>

## <span data-ttu-id="f9f96-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f9f96-104">SYNTAX</span></span>

### <span data-ttu-id="f9f96-105">TargetFqdn (기본값)</span><span class="sxs-lookup"><span data-stu-id="f9f96-105">TargetFqdn (Default)</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -TargetFqdn <String[]> -Protocol <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9f96-106">FqdnTag</span><span class="sxs-lookup"><span data-stu-id="f9f96-106">FqdnTag</span></span>
```
New-AzFirewallPolicyApplicationRule -Name <String> [-Description <String>] [-SourceAddress <String[]>]
 -FqdnTag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9f96-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f9f96-107">DESCRIPTION</span></span>
<span data-ttu-id="f9f96-108">**AzFirewallPolicyApplicationRule** Cmdlet은 Azure 방화벽 정책에 대 한 응용 프로그램 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f9f96-108">The **New-AzFirewallPolicyApplicationRule** cmdlet creates an Application Rule for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="f9f96-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f9f96-109">EXAMPLES</span></span>

### <span data-ttu-id="f9f96-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f9f96-110">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyApplicationRule -Name AR1 -SourceAddress "192.168.0.0/16" -Protocol "http:80","https:443" -TargetFqdn "*.ro", "*.com"
```

<span data-ttu-id="f9f96-111">이 예제에서는 원본 주소, 프로토콜 및 대상 fqdn을 사용 하 여 응용 프로그램 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f9f96-111">This example creates an application rule with the source address, protocol and the target fqdns.</span></span>

## <span data-ttu-id="f9f96-112">변수</span><span class="sxs-lookup"><span data-stu-id="f9f96-112">PARAMETERS</span></span>

### <span data-ttu-id="f9f96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9f96-113">-DefaultProfile</span></span>
<span data-ttu-id="f9f96-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f96-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9f96-115">-설명</span><span class="sxs-lookup"><span data-stu-id="f9f96-115">-Description</span></span>
<span data-ttu-id="f9f96-116">규칙에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="f9f96-116">The description of the rule</span></span>

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

### <span data-ttu-id="f9f96-117">-FqdnTag</span><span class="sxs-lookup"><span data-stu-id="f9f96-117">-FqdnTag</span></span>
<span data-ttu-id="f9f96-118">규칙의 FQDN 태그</span><span class="sxs-lookup"><span data-stu-id="f9f96-118">The FQDN Tags of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: FqdnTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f96-119">-이름</span><span class="sxs-lookup"><span data-stu-id="f9f96-119">-Name</span></span>
<span data-ttu-id="f9f96-120">응용 프로그램 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f96-120">The name of the Application Rule</span></span>

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

### <span data-ttu-id="f9f96-121">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="f9f96-121">-Protocol</span></span>
<span data-ttu-id="f9f96-122">규칙의 프로토콜</span><span class="sxs-lookup"><span data-stu-id="f9f96-122">The protocols of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f96-123">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="f9f96-123">-SourceAddress</span></span>
<span data-ttu-id="f9f96-124">규칙의 원본 주소</span><span class="sxs-lookup"><span data-stu-id="f9f96-124">The source addresses of the rule</span></span>

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

### <span data-ttu-id="f9f96-125">-TargetFqdn</span><span class="sxs-lookup"><span data-stu-id="f9f96-125">-TargetFqdn</span></span>
<span data-ttu-id="f9f96-126">규칙의 대상 Fqdn</span><span class="sxs-lookup"><span data-stu-id="f9f96-126">The target FQDNs of the rule</span></span>

```yaml
Type: String[]
Parameter Sets: TargetFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9f96-127">-확인</span><span class="sxs-lookup"><span data-stu-id="f9f96-127">-Confirm</span></span>
<span data-ttu-id="f9f96-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f96-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9f96-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9f96-129">-WhatIf</span></span>
<span data-ttu-id="f9f96-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f9f96-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9f96-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f96-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9f96-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9f96-132">CommonParameters</span></span>
<span data-ttu-id="f9f96-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f96-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9f96-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f9f96-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9f96-135">입력</span><span class="sxs-lookup"><span data-stu-id="f9f96-135">INPUTS</span></span>

### <span data-ttu-id="f9f96-136">않아야</span><span class="sxs-lookup"><span data-stu-id="f9f96-136">None</span></span>

## <span data-ttu-id="f9f96-137">출력</span><span class="sxs-lookup"><span data-stu-id="f9f96-137">OUTPUTS</span></span>

### <span data-ttu-id="f9f96-138">PSAzureFirewallPolicyApplicationRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f9f96-138">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyApplicationRule</span></span>

## <span data-ttu-id="f9f96-139">상속자</span><span class="sxs-lookup"><span data-stu-id="f9f96-139">NOTES</span></span>

## <span data-ttu-id="f9f96-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9f96-140">RELATED LINKS</span></span>

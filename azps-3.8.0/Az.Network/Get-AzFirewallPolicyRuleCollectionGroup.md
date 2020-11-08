---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8ce5369605f419821994c771dc9200e138e5ad7a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043344"
---
# <span data-ttu-id="2de8f-101">Get-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="2de8f-101">Get-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="2de8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2de8f-102">SYNOPSIS</span></span>
<span data-ttu-id="2de8f-103">Azure 방화벽 정책 규칙 컬렉션 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2de8f-103">Gets a Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="2de8f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2de8f-104">SYNTAX</span></span>

### <span data-ttu-id="2de8f-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2de8f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2de8f-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2de8f-106">GetByInputObjectParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -AzureFirewallPolicy <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2de8f-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2de8f-107">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2de8f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2de8f-108">DESCRIPTION</span></span>
<span data-ttu-id="2de8f-109">**AzFirewallPolicyRuleCollectionGroup** Cmdlet은 방화벽 정책에서 언급 한 RuleCollectionGroup를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2de8f-109">The **Get-AzFirewallPolicyRuleCollectionGroup** cmdlet gets the RuleCollectionGroup mentioned from a Firewall Policy</span></span>

## <span data-ttu-id="2de8f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2de8f-110">EXAMPLES</span></span>

### <span data-ttu-id="2de8f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2de8f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicyRuleCollectionGroup -Name rg1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="2de8f-112">이 예제에서는 방화벽 정책의 규칙 collectionGroup을 가져옵니다 $fp</span><span class="sxs-lookup"><span data-stu-id="2de8f-112">This example get the rule collectionGroup in the firewall policy $fp</span></span>

## <span data-ttu-id="2de8f-113">변수</span><span class="sxs-lookup"><span data-stu-id="2de8f-113">PARAMETERS</span></span>

### <span data-ttu-id="2de8f-114">-AzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="2de8f-114">-AzureFirewallPolicy</span></span>
<span data-ttu-id="2de8f-115">방화벽 정책.</span><span class="sxs-lookup"><span data-stu-id="2de8f-115">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de8f-116">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="2de8f-116">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="2de8f-117">방화벽 정책 이름</span><span class="sxs-lookup"><span data-stu-id="2de8f-117">The Firewall policy name</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de8f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de8f-118">-DefaultProfile</span></span>
<span data-ttu-id="2de8f-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2de8f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2de8f-120">-이름</span><span class="sxs-lookup"><span data-stu-id="2de8f-120">-Name</span></span>
<span data-ttu-id="2de8f-121">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2de8f-121">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de8f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de8f-122">-ResourceGroupName</span></span>
<span data-ttu-id="2de8f-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2de8f-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de8f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2de8f-124">-ResourceId</span></span>
<span data-ttu-id="2de8f-125">리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="2de8f-125">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de8f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de8f-126">CommonParameters</span></span>
<span data-ttu-id="2de8f-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2de8f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de8f-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2de8f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de8f-129">입력</span><span class="sxs-lookup"><span data-stu-id="2de8f-129">INPUTS</span></span>

### <span data-ttu-id="2de8f-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2de8f-130">System.String</span></span>

### <span data-ttu-id="2de8f-131">PSAzureFirewallPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2de8f-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="2de8f-132">출력</span><span class="sxs-lookup"><span data-stu-id="2de8f-132">OUTPUTS</span></span>

### <span data-ttu-id="2de8f-133">Microsoft. \* PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="2de8f-133">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="2de8f-134">1.12.0.0 ' 1 [[Microsoft Azure.]. 모델에 대 한 PSAzureFirewall, Microsoft Azure. PowerShell. t e t-네트워크, 버전 =, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2de8f-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2de8f-135">상속자</span><span class="sxs-lookup"><span data-stu-id="2de8f-135">NOTES</span></span>

## <span data-ttu-id="2de8f-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2de8f-136">RELATED LINKS</span></span>

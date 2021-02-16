---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193865"
---
# <span data-ttu-id="0ebce-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="0ebce-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="0ebce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ebce-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebce-103">Azure Firewall 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0ebce-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="0ebce-104">구문</span><span class="sxs-lookup"><span data-stu-id="0ebce-104">SYNTAX</span></span>

### <span data-ttu-id="0ebce-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0ebce-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ebce-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ebce-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ebce-107">설명</span><span class="sxs-lookup"><span data-stu-id="0ebce-107">DESCRIPTION</span></span>
<span data-ttu-id="0ebce-108">**Get-AzFirewallPolicy** cmdlet은 리소스 그룹에서 하나 이상의 방화벽을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0ebce-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="0ebce-109">예제</span><span class="sxs-lookup"><span data-stu-id="0ebce-109">EXAMPLES</span></span>

### <span data-ttu-id="0ebce-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0ebce-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="0ebce-111">이 예제에서는 리소스 그룹 "TestRg"에서 "firewallPolicy"라는 방화벽 정책을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ebce-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="0ebce-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ebce-112">PARAMETERS</span></span>

### <span data-ttu-id="0ebce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ebce-113">-DefaultProfile</span></span>
<span data-ttu-id="0ebce-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ebce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ebce-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0ebce-115">-Name</span></span>
<span data-ttu-id="0ebce-116">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ebce-116">The resource name.</span></span>

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

### <span data-ttu-id="0ebce-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ebce-117">-ResourceGroupName</span></span>
<span data-ttu-id="0ebce-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ebce-118">The resource group name.</span></span>

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

### <span data-ttu-id="0ebce-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ebce-119">-ResourceId</span></span>
<span data-ttu-id="0ebce-120">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0ebce-120">The resource Id.</span></span>

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

### <span data-ttu-id="0ebce-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebce-121">CommonParameters</span></span>
<span data-ttu-id="0ebce-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0ebce-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ebce-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0ebce-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebce-124">입력</span><span class="sxs-lookup"><span data-stu-id="0ebce-124">INPUTS</span></span>

### <span data-ttu-id="0ebce-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0ebce-125">System.String</span></span>

## <span data-ttu-id="0ebce-126">출력</span><span class="sxs-lookup"><span data-stu-id="0ebce-126">OUTPUTS</span></span>

### <span data-ttu-id="0ebce-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="0ebce-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="0ebce-128">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="0ebce-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0ebce-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0ebce-129">NOTES</span></span>

## <span data-ttu-id="0ebce-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ebce-130">RELATED LINKS</span></span>

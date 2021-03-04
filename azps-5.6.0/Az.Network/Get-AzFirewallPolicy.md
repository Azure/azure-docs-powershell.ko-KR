---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: 056a70f6c085f3c0a936f9e144708c7258a3d5c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956928"
---
# <span data-ttu-id="54160-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="54160-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="54160-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54160-102">SYNOPSIS</span></span>
<span data-ttu-id="54160-103">Azure 방화벽 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="54160-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="54160-104">구문</span><span class="sxs-lookup"><span data-stu-id="54160-104">SYNTAX</span></span>

### <span data-ttu-id="54160-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="54160-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54160-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54160-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54160-107">설명</span><span class="sxs-lookup"><span data-stu-id="54160-107">DESCRIPTION</span></span>
<span data-ttu-id="54160-108">**Get-AzFirewallPolicy** cmdlet은 리소스 그룹에서 하나 이상의 방화벽을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="54160-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="54160-109">예제</span><span class="sxs-lookup"><span data-stu-id="54160-109">EXAMPLES</span></span>

### <span data-ttu-id="54160-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="54160-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="54160-111">이 예제에서는 리소스 그룹 "TestRg"에서 "firewallPolicy"라는 방화벽 정책을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="54160-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="54160-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="54160-112">PARAMETERS</span></span>

### <span data-ttu-id="54160-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54160-113">-DefaultProfile</span></span>
<span data-ttu-id="54160-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54160-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54160-115">-Name</span><span class="sxs-lookup"><span data-stu-id="54160-115">-Name</span></span>
<span data-ttu-id="54160-116">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54160-116">The resource name.</span></span>

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

### <span data-ttu-id="54160-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54160-117">-ResourceGroupName</span></span>
<span data-ttu-id="54160-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54160-118">The resource group name.</span></span>

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

### <span data-ttu-id="54160-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54160-119">-ResourceId</span></span>
<span data-ttu-id="54160-120">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="54160-120">The resource Id.</span></span>

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

### <span data-ttu-id="54160-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54160-121">CommonParameters</span></span>
<span data-ttu-id="54160-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="54160-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54160-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54160-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54160-124">입력</span><span class="sxs-lookup"><span data-stu-id="54160-124">INPUTS</span></span>

### <span data-ttu-id="54160-125">System.String</span><span class="sxs-lookup"><span data-stu-id="54160-125">System.String</span></span>

## <span data-ttu-id="54160-126">출력</span><span class="sxs-lookup"><span data-stu-id="54160-126">OUTPUTS</span></span>

### <span data-ttu-id="54160-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="54160-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="54160-128">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="54160-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="54160-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="54160-129">NOTES</span></span>

## <span data-ttu-id="54160-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54160-130">RELATED LINKS</span></span>

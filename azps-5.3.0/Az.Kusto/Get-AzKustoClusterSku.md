---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 42fed776d1f77211c7967dd6313d0ddd1e04b65a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490223"
---
# <span data-ttu-id="d3085-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="d3085-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="d3085-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3085-102">SYNOPSIS</span></span>
<span data-ttu-id="d3085-103">Kusto 리소스 공급자에 대한 적격 S KU를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="d3085-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="d3085-104">구문</span><span class="sxs-lookup"><span data-stu-id="d3085-104">SYNTAX</span></span>

### <span data-ttu-id="d3085-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="d3085-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d3085-106">List1</span><span class="sxs-lookup"><span data-stu-id="d3085-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d3085-107">설명</span><span class="sxs-lookup"><span data-stu-id="d3085-107">DESCRIPTION</span></span>
<span data-ttu-id="d3085-108">Kusto 리소스 공급자에 대한 적격 S KU를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="d3085-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="d3085-109">예제</span><span class="sxs-lookup"><span data-stu-id="d3085-109">EXAMPLES</span></span>

### <span data-ttu-id="d3085-110">예제 1: 적격 SKUS 나열</span><span class="sxs-lookup"><span data-stu-id="d3085-110">Example 1: Lists eligible SKUs</span></span>
```powershell
PS C:\> Get-AzKustoClusterSku

Location             Name                        ResourceType Tier
--------             ----                        ------------ ----
{eastus2}            D13_v2                      clusters     Standard
{eastus2}            D14_v2                      clusters     Standard
{eastus2}            L8                          clusters     Standard
{eastus2}            L16                         clusters     Standard
{eastus2}            D11_v2                      clusters     Standard
{eastus2}            D12_v2                      clusters     Standard
{eastus2}            L4                          clusters     Standard
{eastus2}            Standard_D13_v2             clusters     Standard
{eastus2}            Standard_D14_v2             clusters     Standard
{eastus2}            Standard_L8s                clusters     Standard
{eastus2}            Standard_L16s               clusters     Standard
{eastus2}            Standard_D11_v2             clusters     Standard
{eastus2}            Standard_D12_v2             clusters     Standard
{eastus2}            Standard_L4s                clusters     Standard
{eastus2}            Standard_DS13_v2+1TB_PS     clusters     Standard
{eastus2}            Standard_DS13_v2+2TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+3TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+4TB_PS     clusters     Standard
{eastus2}            Dev(No SLA)_Standard_D11_v2 clusters     Basic
{westcentralus}      D13_v2                      clusters     Standard
{westcentralus}      D14_v2                      clusters     Standard
{westcentralus}      D11_v2                      clusters     Standard
{westcentralus}      D12_v2                      clusters     Standard
{westcentralus}      Standard_D13_v2             clusters     Standard
{westcentralus}      Standard_D14_v2             clusters     Standard
{westcentralus}      Standard_D11_v2             clusters     Standard
{westcentralus}      Standard_D12_v2             clusters     Standard
{westcentralus}      Standard_DS13_v2+1TB_PS     clusters     Standard
{westcentralus}      Standard_DS13_v2+2TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+3TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+4TB_PS     clusters     Standard
...
```

<span data-ttu-id="d3085-111">위의 명령은 적격 SKUS를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="d3085-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="d3085-112">예제 2: 특정 클러스터에 대한 적격 SKUS 나열</span><span class="sxs-lookup"><span data-stu-id="d3085-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
```powershell
PS C:\>  Get-AzKustoClusterSku -ResourceGroupName testrg -ClusterName testnewkustocluster

ResourceType
------------
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
...
```

<span data-ttu-id="d3085-113">위의 명령은 특정 클러스터에 대해 적격 SKUS를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="d3085-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="d3085-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3085-114">PARAMETERS</span></span>

### <span data-ttu-id="d3085-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="d3085-115">-ClusterName</span></span>
<span data-ttu-id="d3085-116">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3085-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3085-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3085-117">-DefaultProfile</span></span>
<span data-ttu-id="d3085-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3085-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3085-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3085-119">-ResourceGroupName</span></span>
<span data-ttu-id="d3085-120">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3085-120">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3085-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3085-121">-SubscriptionId</span></span>
<span data-ttu-id="d3085-122">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d3085-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d3085-123">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="d3085-123">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3085-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3085-124">CommonParameters</span></span>
<span data-ttu-id="d3085-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d3085-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3085-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d3085-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3085-127">입력</span><span class="sxs-lookup"><span data-stu-id="d3085-127">INPUTS</span></span>

## <span data-ttu-id="d3085-128">출력</span><span class="sxs-lookup"><span data-stu-id="d3085-128">OUTPUTS</span></span>

### <span data-ttu-id="d3085-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAzureResourceSku</span><span class="sxs-lookup"><span data-stu-id="d3085-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAzureResourceSku</span></span>

### <span data-ttu-id="d3085-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ISkuDescription</span><span class="sxs-lookup"><span data-stu-id="d3085-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ISkuDescription</span></span>

## <span data-ttu-id="d3085-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d3085-131">NOTES</span></span>

<span data-ttu-id="d3085-132">별칭</span><span class="sxs-lookup"><span data-stu-id="d3085-132">ALIASES</span></span>

## <span data-ttu-id="d3085-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3085-133">RELATED LINKS</span></span>


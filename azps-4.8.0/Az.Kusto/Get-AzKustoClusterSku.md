---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 88b3104512b1cad4cddf98f521b44c6b638c05b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056684"
---
# <span data-ttu-id="4ca04-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="4ca04-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="4ca04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ca04-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca04-103">Kusto 리소스 공급자에 대 한 적격 Sku 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca04-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="4ca04-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ca04-104">SYNTAX</span></span>

### <span data-ttu-id="4ca04-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4ca04-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4ca04-106">List1</span><span class="sxs-lookup"><span data-stu-id="4ca04-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4ca04-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4ca04-107">DESCRIPTION</span></span>
<span data-ttu-id="4ca04-108">Kusto 리소스 공급자에 대 한 적격 Sku 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca04-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="4ca04-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4ca04-109">EXAMPLES</span></span>

### <span data-ttu-id="4ca04-110">예제 1: 적격 Sku 목록 표시</span><span class="sxs-lookup"><span data-stu-id="4ca04-110">Example 1: Lists eligible SKUs</span></span>
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

<span data-ttu-id="4ca04-111">위의 명령에 적격 Sku가 나열 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ca04-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="4ca04-112">예제 2: 특정 클러스터에 대 한 적격 Sku 목록</span><span class="sxs-lookup"><span data-stu-id="4ca04-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
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

<span data-ttu-id="4ca04-113">위의 명령은 특정 클러스터에 대 한 적격 Sku 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca04-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="4ca04-114">변수</span><span class="sxs-lookup"><span data-stu-id="4ca04-114">PARAMETERS</span></span>

### <span data-ttu-id="4ca04-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4ca04-115">-ClusterName</span></span>
<span data-ttu-id="4ca04-116">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ca04-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="4ca04-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca04-117">-DefaultProfile</span></span>
<span data-ttu-id="4ca04-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ca04-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ca04-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ca04-119">-ResourceGroupName</span></span>
<span data-ttu-id="4ca04-120">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ca04-120">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="4ca04-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ca04-121">-SubscriptionId</span></span>
<span data-ttu-id="4ca04-122">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4ca04-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4ca04-123">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca04-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4ca04-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca04-124">CommonParameters</span></span>
<span data-ttu-id="4ca04-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ca04-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca04-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4ca04-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca04-127">입력</span><span class="sxs-lookup"><span data-stu-id="4ca04-127">INPUTS</span></span>

## <span data-ttu-id="4ca04-128">출력</span><span class="sxs-lookup"><span data-stu-id="4ca04-128">OUTPUTS</span></span>

### <span data-ttu-id="4ca04-129">Microsoft. Api20200614. IAzureResourceSku에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4ca04-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAzureResourceSku</span></span>

### <span data-ttu-id="4ca04-130">Microsoft. Api20200614. ISkuDescription에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4ca04-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ISkuDescription</span></span>

## <span data-ttu-id="4ca04-131">상속자</span><span class="sxs-lookup"><span data-stu-id="4ca04-131">NOTES</span></span>

<span data-ttu-id="4ca04-132">별칭과</span><span class="sxs-lookup"><span data-stu-id="4ca04-132">ALIASES</span></span>

## <span data-ttu-id="4ca04-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ca04-133">RELATED LINKS</span></span>


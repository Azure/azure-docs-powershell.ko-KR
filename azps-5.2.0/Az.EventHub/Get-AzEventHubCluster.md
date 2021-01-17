---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
ms.openlocfilehash: 4e2657d6a4af26b96a2e7a97a56b735838610005
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323595"
---
# <span data-ttu-id="01a22-101">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="01a22-101">Get-AzEventHubCluster</span></span>

## <span data-ttu-id="01a22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01a22-102">SYNOPSIS</span></span>
<span data-ttu-id="01a22-103">단일 이벤트 허브 클러스터의 세부 정보를 얻거나 이벤트 허브 클러스터 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="01a22-103">Gets the details of a single Event Hub Cluster , or gets a list of Event Hub Clusters.</span></span>

## <span data-ttu-id="01a22-104">구문</span><span class="sxs-lookup"><span data-stu-id="01a22-104">SYNTAX</span></span>

```
Get-AzEventHubCluster [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01a22-105">설명</span><span class="sxs-lookup"><span data-stu-id="01a22-105">DESCRIPTION</span></span>
<span data-ttu-id="01a22-106">이 Get-AzEventHubCluster cmdlet은 이벤트 허브 클러스터의 세부 정보 또는 주어진 리소스 그룹의 모든 Event Hub 클러스터 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="01a22-106">The Get-AzEventHubCluster cmdlet returns either the details of an Event Hub Cluster, or a list of all Event Hub Clusters in given resource group.</span></span>
<span data-ttu-id="01a22-107">클러스터 이름이 제공된 경우 단일 클러스터의 세부 정보가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="01a22-107">If the cluster name is provided, the details of a single cluster are returned.</span></span>
<span data-ttu-id="01a22-108">클러스터 이름이 제공되지 않으면 지정된 리소스 그룹의 모든 클러스터 목록이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="01a22-108">If an cluster name is not provided, a list of all clusters in the specified resource group is returned.</span></span>

## <span data-ttu-id="01a22-109">예제</span><span class="sxs-lookup"><span data-stu-id="01a22-109">EXAMPLES</span></span>

### <span data-ttu-id="01a22-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="01a22-110">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557

Id        : /subscriptions/326100e2-f69d-4268-8503-075374f62b6e/resourceGroups/RSG-Cluster27651/providers/Microsoft.Eve
            ntHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/10/2020 23:02:48
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag2, Tag4], [ClusterTag1, Tag3]}

```

<span data-ttu-id="01a22-111">리소스 그룹 'RSG-Cluster27651'에서 'Eventhub-Cluster-5557' 클러스터의tials를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="01a22-111">Returns the detials of cluster 'Eventhub-Cluster-5557' from the resource group 'RSG-Cluster27651'</span></span>

## <span data-ttu-id="01a22-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01a22-112">PARAMETERS</span></span>

### <span data-ttu-id="01a22-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a22-113">-DefaultProfile</span></span>
<span data-ttu-id="01a22-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01a22-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01a22-115">-Name</span><span class="sxs-lookup"><span data-stu-id="01a22-115">-Name</span></span>
<span data-ttu-id="01a22-116">클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="01a22-116">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a22-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01a22-117">-ResourceGroupName</span></span>
<span data-ttu-id="01a22-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="01a22-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a22-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01a22-119">CommonParameters</span></span>
<span data-ttu-id="01a22-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="01a22-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01a22-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="01a22-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01a22-122">입력</span><span class="sxs-lookup"><span data-stu-id="01a22-122">INPUTS</span></span>

### <span data-ttu-id="01a22-123">System.String</span><span class="sxs-lookup"><span data-stu-id="01a22-123">System.String</span></span>

## <span data-ttu-id="01a22-124">출력</span><span class="sxs-lookup"><span data-stu-id="01a22-124">OUTPUTS</span></span>

### <span data-ttu-id="01a22-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="01a22-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="01a22-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="01a22-126">NOTES</span></span>

## <span data-ttu-id="01a22-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01a22-127">RELATED LINKS</span></span>

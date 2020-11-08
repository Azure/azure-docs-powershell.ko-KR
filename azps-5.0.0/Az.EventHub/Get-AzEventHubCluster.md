---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
ms.openlocfilehash: 4e2657d6a4af26b96a2e7a97a56b735838610005
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218698"
---
# <span data-ttu-id="b2539-101">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="b2539-101">Get-AzEventHubCluster</span></span>

## <span data-ttu-id="b2539-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2539-102">SYNOPSIS</span></span>
<span data-ttu-id="b2539-103">단일 이벤트 허브 클러스터의 세부 정보를 가져오거나 이벤트 허브 클러스터의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2539-103">Gets the details of a single Event Hub Cluster , or gets a list of Event Hub Clusters.</span></span>

## <span data-ttu-id="b2539-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b2539-104">SYNTAX</span></span>

```
Get-AzEventHubCluster [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2539-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b2539-105">DESCRIPTION</span></span>
<span data-ttu-id="b2539-106">Get-AzEventHubCluster cmdlet은 이벤트 허브 클러스터의 세부 정보 또는 주어진 리소스 그룹에 있는 모든 이벤트 허브 클러스터의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2539-106">The Get-AzEventHubCluster cmdlet returns either the details of an Event Hub Cluster, or a list of all Event Hub Clusters in given resource group.</span></span>
<span data-ttu-id="b2539-107">클러스터 이름을 제공 하는 경우 단일 클러스터에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2539-107">If the cluster name is provided, the details of a single cluster are returned.</span></span>
<span data-ttu-id="b2539-108">클러스터 이름을 제공 하지 않으면 지정 된 리소스 그룹에 있는 모든 클러스터의 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2539-108">If an cluster name is not provided, a list of all clusters in the specified resource group is returned.</span></span>

## <span data-ttu-id="b2539-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b2539-109">EXAMPLES</span></span>

### <span data-ttu-id="b2539-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b2539-110">Example 1</span></span>
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

<span data-ttu-id="b2539-111">리소스 그룹 ' RSG-Cluster27651 '에서 ' Eventhub-Cluster-5557 ' 클러스터의 detials를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2539-111">Returns the detials of cluster 'Eventhub-Cluster-5557' from the resource group 'RSG-Cluster27651'</span></span>

## <span data-ttu-id="b2539-112">변수</span><span class="sxs-lookup"><span data-stu-id="b2539-112">PARAMETERS</span></span>

### <span data-ttu-id="b2539-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2539-113">-DefaultProfile</span></span>
<span data-ttu-id="b2539-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2539-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2539-115">-이름</span><span class="sxs-lookup"><span data-stu-id="b2539-115">-Name</span></span>
<span data-ttu-id="b2539-116">클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="b2539-116">Cluster Name</span></span>

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

### <span data-ttu-id="b2539-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2539-117">-ResourceGroupName</span></span>
<span data-ttu-id="b2539-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b2539-118">Resource Group Name</span></span>

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

### <span data-ttu-id="b2539-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2539-119">CommonParameters</span></span>
<span data-ttu-id="b2539-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2539-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2539-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b2539-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2539-122">입력</span><span class="sxs-lookup"><span data-stu-id="b2539-122">INPUTS</span></span>

### <span data-ttu-id="b2539-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b2539-123">System.String</span></span>

## <span data-ttu-id="b2539-124">출력</span><span class="sxs-lookup"><span data-stu-id="b2539-124">OUTPUTS</span></span>

### <span data-ttu-id="b2539-125">PSEventHubAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="b2539-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="b2539-126">상속자</span><span class="sxs-lookup"><span data-stu-id="b2539-126">NOTES</span></span>

## <span data-ttu-id="b2539-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2539-127">RELATED LINKS</span></span>

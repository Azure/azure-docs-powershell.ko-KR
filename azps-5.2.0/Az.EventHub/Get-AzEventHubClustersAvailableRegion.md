---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 712e9274eabe27bbe5f4a8acce704926e1e895fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344594"
---
# <span data-ttu-id="80c86-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="80c86-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="80c86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80c86-102">SYNOPSIS</span></span>
<span data-ttu-id="80c86-103">단일 Eventhub 클러스터 또는 주어진 리소스 그룹의 클러스터 목록을 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="80c86-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="80c86-104">구문</span><span class="sxs-lookup"><span data-stu-id="80c86-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80c86-105">설명</span><span class="sxs-lookup"><span data-stu-id="80c86-105">DESCRIPTION</span></span>
<span data-ttu-id="80c86-106">전용 Get-AzEventHubClustersAvailableRegion 사용할 수 있는 지역의 Get-AzEventHubClustersAvailableRegion cmdlet 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="80c86-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="80c86-107">예제</span><span class="sxs-lookup"><span data-stu-id="80c86-107">EXAMPLES</span></span>

### <span data-ttu-id="80c86-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="80c86-108">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubClustersAvailableRegion

Location
--------
northcentralus
westeurope
uksouth
westcentralus
australiasoutheast
ukwest
brazilsouth
centralus
australiaeast
eastus
southcentralus
japaneast
northeurope
eastus2
southeastasia
eastasia
westus
westus2
```

<span data-ttu-id="80c86-109">지역 목록이 반환되는 위치</span><span class="sxs-lookup"><span data-stu-id="80c86-109">List of regions is returned where</span></span>

## <span data-ttu-id="80c86-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80c86-110">PARAMETERS</span></span>

### <span data-ttu-id="80c86-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c86-111">-DefaultProfile</span></span>
<span data-ttu-id="80c86-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80c86-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80c86-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c86-113">CommonParameters</span></span>
<span data-ttu-id="80c86-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="80c86-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c86-115">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="80c86-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c86-116">입력</span><span class="sxs-lookup"><span data-stu-id="80c86-116">INPUTS</span></span>

### <span data-ttu-id="80c86-117">없음</span><span class="sxs-lookup"><span data-stu-id="80c86-117">None</span></span>

## <span data-ttu-id="80c86-118">출력</span><span class="sxs-lookup"><span data-stu-id="80c86-118">OUTPUTS</span></span>

### <span data-ttu-id="80c86-119">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="80c86-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="80c86-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="80c86-120">NOTES</span></span>

## <span data-ttu-id="80c86-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80c86-121">RELATED LINKS</span></span>

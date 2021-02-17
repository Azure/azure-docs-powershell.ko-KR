---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 712e9274eabe27bbe5f4a8acce704926e1e895fe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196340"
---
# <span data-ttu-id="21e4a-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="21e4a-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="21e4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="21e4a-103">단일 Eventhub 클러스터 또는 주어진 리소스 그룹의 클러스터 목록을 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="21e4a-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="21e4a-104">구문</span><span class="sxs-lookup"><span data-stu-id="21e4a-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21e4a-105">설명</span><span class="sxs-lookup"><span data-stu-id="21e4a-105">DESCRIPTION</span></span>
<span data-ttu-id="21e4a-106">전용 Get-AzEventHubClustersAvailableRegion 사용할 수 있는 지역의 Get-AzEventHubClustersAvailableRegion cmdlet 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="21e4a-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="21e4a-107">예제</span><span class="sxs-lookup"><span data-stu-id="21e4a-107">EXAMPLES</span></span>

### <span data-ttu-id="21e4a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="21e4a-108">Example 1</span></span>
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

<span data-ttu-id="21e4a-109">지역 목록이 반환되는 위치</span><span class="sxs-lookup"><span data-stu-id="21e4a-109">List of regions is returned where</span></span>

## <span data-ttu-id="21e4a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21e4a-110">PARAMETERS</span></span>

### <span data-ttu-id="21e4a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21e4a-111">-DefaultProfile</span></span>
<span data-ttu-id="21e4a-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21e4a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21e4a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21e4a-113">CommonParameters</span></span>
<span data-ttu-id="21e4a-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="21e4a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21e4a-115">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="21e4a-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21e4a-116">입력</span><span class="sxs-lookup"><span data-stu-id="21e4a-116">INPUTS</span></span>

### <span data-ttu-id="21e4a-117">없음</span><span class="sxs-lookup"><span data-stu-id="21e4a-117">None</span></span>

## <span data-ttu-id="21e4a-118">출력</span><span class="sxs-lookup"><span data-stu-id="21e4a-118">OUTPUTS</span></span>

### <span data-ttu-id="21e4a-119">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="21e4a-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="21e4a-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="21e4a-120">NOTES</span></span>

## <span data-ttu-id="21e4a-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21e4a-121">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubclustersavailableregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubClustersAvailableRegion.md
ms.openlocfilehash: 712e9274eabe27bbe5f4a8acce704926e1e895fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214534"
---
# <span data-ttu-id="b0f0c-101">Get-AzEventHubClustersAvailableRegion</span><span class="sxs-lookup"><span data-stu-id="b0f0c-101">Get-AzEventHubClustersAvailableRegion</span></span>

## <span data-ttu-id="b0f0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="b0f0c-103">단일 Eventhub 클러스터 또는 지정 된 리소스 그룹의 클러스터 목록에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0f0c-103">Gets the details of single Eventhub cluster or the list of clusters in the given Resource Group</span></span>

## <span data-ttu-id="b0f0c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0f0c-104">SYNTAX</span></span>

```
Get-AzEventHubClustersAvailableRegion [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0f0c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b0f0c-105">DESCRIPTION</span></span>
<span data-ttu-id="b0f0c-106">전용을 만들 수 있는 지역의 Get-AzEventHubClustersAvailableRegion cmdlet 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b0f0c-106">The Get-AzEventHubClustersAvailableRegion cmdlet list of regions where dedicated are available to create.</span></span>

## <span data-ttu-id="b0f0c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b0f0c-107">EXAMPLES</span></span>

### <span data-ttu-id="b0f0c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b0f0c-108">Example 1</span></span>
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

<span data-ttu-id="b0f0c-109">지역 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0f0c-109">List of regions is returned where</span></span>

## <span data-ttu-id="b0f0c-110">변수</span><span class="sxs-lookup"><span data-stu-id="b0f0c-110">PARAMETERS</span></span>

### <span data-ttu-id="b0f0c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0f0c-111">-DefaultProfile</span></span>
<span data-ttu-id="b0f0c-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0f0c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0f0c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0f0c-113">CommonParameters</span></span>
<span data-ttu-id="b0f0c-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0f0c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0f0c-115">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0f0c-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0f0c-116">입력</span><span class="sxs-lookup"><span data-stu-id="b0f0c-116">INPUTS</span></span>

### <span data-ttu-id="b0f0c-117">않아야</span><span class="sxs-lookup"><span data-stu-id="b0f0c-117">None</span></span>

## <span data-ttu-id="b0f0c-118">출력</span><span class="sxs-lookup"><span data-stu-id="b0f0c-118">OUTPUTS</span></span>

### <span data-ttu-id="b0f0c-119">System.webserver. t e 1 [[Microsoft Azure. 1.5.0.0, PSEventHubsAvailableCluster, Microsoft Azure. PowerShell. h 2, 버전 =, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b0f0c-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubsAvailableCluster, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b0f0c-120">상속자</span><span class="sxs-lookup"><span data-stu-id="b0f0c-120">NOTES</span></span>

## <span data-ttu-id="b0f0c-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0f0c-121">RELATED LINKS</span></span>

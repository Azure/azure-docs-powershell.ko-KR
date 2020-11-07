---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearchresults
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
ms.openlocfilehash: 9b885193a3e00b9bfe062de4b47feedae36e545f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702363"
---
# <span data-ttu-id="9fa57-101">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="9fa57-101">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>

## <span data-ttu-id="9fa57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fa57-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa57-103">쿼리 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa57-103">Returns the results from a query.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fa57-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9fa57-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fa57-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9fa57-105">DESCRIPTION</span></span>
<span data-ttu-id="9fa57-106">**AzureRmOperationalInsightsSavedSearchResults** cmdlet은 검색 ID로 지정 된 쿼리의 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa57-106">The **Get-AzureRmOperationalInsightsSavedSearchResults** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="9fa57-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9fa57-107">EXAMPLES</span></span>

### <span data-ttu-id="9fa57-108">예제 1: 저장 된 검색에 대 한 모든 검색 결과 가져오기</span><span class="sxs-lookup"><span data-stu-id="9fa57-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzureRmOperationalInsightSavedSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="9fa57-109">이 명령은 저장 된 검색에 대 한 모든 검색 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9fa57-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="9fa57-110">변수</span><span class="sxs-lookup"><span data-stu-id="9fa57-110">PARAMETERS</span></span>

### <span data-ttu-id="9fa57-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa57-111">-DefaultProfile</span></span>
<span data-ttu-id="9fa57-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9fa57-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa57-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fa57-113">-ResourceGroupName</span></span>
<span data-ttu-id="9fa57-114">작업 영역을 포함 하는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa57-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa57-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="9fa57-115">-SavedSearchId</span></span>
<span data-ttu-id="9fa57-116">저장 된 검색 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa57-116">Specifies a saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa57-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9fa57-117">-WorkspaceName</span></span>
<span data-ttu-id="9fa57-118">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa57-118">Specifies a workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa57-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa57-119">CommonParameters</span></span>
<span data-ttu-id="9fa57-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa57-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa57-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fa57-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa57-122">입력</span><span class="sxs-lookup"><span data-stu-id="9fa57-122">INPUTS</span></span>

### <span data-ttu-id="9fa57-123">않아야</span><span class="sxs-lookup"><span data-stu-id="9fa57-123">None</span></span>
<span data-ttu-id="9fa57-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9fa57-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9fa57-125">출력</span><span class="sxs-lookup"><span data-stu-id="9fa57-125">OUTPUTS</span></span>

### <span data-ttu-id="9fa57-126">OperationalInsights. PSSearchGetSearchResultsResponse/.</span><span class="sxs-lookup"><span data-stu-id="9fa57-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="9fa57-127">상속자</span><span class="sxs-lookup"><span data-stu-id="9fa57-127">NOTES</span></span>

## <span data-ttu-id="9fa57-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9fa57-128">RELATED LINKS</span></span>

[<span data-ttu-id="9fa57-129">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9fa57-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)



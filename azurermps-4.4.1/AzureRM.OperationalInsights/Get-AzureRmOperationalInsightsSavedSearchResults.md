---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: AA3EF369-C724-4D32-A56E-503CBE191320
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearchResults.md
ms.openlocfilehash: 88adac87543c0a51542cc0f79f2f1eb10ca8184b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533927"
---
# <span data-ttu-id="faaf0-101">Get-AzureRmOperationalInsightsSavedSearchResults</span><span class="sxs-lookup"><span data-stu-id="faaf0-101">Get-AzureRmOperationalInsightsSavedSearchResults</span></span>

## <span data-ttu-id="faaf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faaf0-102">SYNOPSIS</span></span>
<span data-ttu-id="faaf0-103">쿼리 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="faaf0-103">Returns the results from a query.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faaf0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="faaf0-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearchResults [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faaf0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="faaf0-105">DESCRIPTION</span></span>
<span data-ttu-id="faaf0-106">**AzureRmOperationalInsightsSavedSearchResults** cmdlet은 검색 ID로 지정 된 쿼리의 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="faaf0-106">The **Get-AzureRmOperationalInsightsSavedSearchResults** cmdlet returns the results from the query specified by the search ID.</span></span>

## <span data-ttu-id="faaf0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="faaf0-107">EXAMPLES</span></span>

### <span data-ttu-id="faaf0-108">예제 1: 저장 된 검색에 대 한 모든 검색 결과 가져오기</span><span class="sxs-lookup"><span data-stu-id="faaf0-108">Example 1: Get all of the search results for a saved search</span></span>
```
PS C:\>Get-AzureRmOperationalInsightSavedSearchResults -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="faaf0-109">이 명령은 저장 된 검색에 대 한 모든 검색 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="faaf0-109">This command gets all of the search results for a saved search.</span></span>

## <span data-ttu-id="faaf0-110">변수</span><span class="sxs-lookup"><span data-stu-id="faaf0-110">PARAMETERS</span></span>

### <span data-ttu-id="faaf0-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faaf0-111">-ResourceGroupName</span></span>
<span data-ttu-id="faaf0-112">작업 영역을 포함 하는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="faaf0-112">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="faaf0-113">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="faaf0-113">-SavedSearchId</span></span>
<span data-ttu-id="faaf0-114">저장 된 검색 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="faaf0-114">Specifies a saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faaf0-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="faaf0-115">-WorkspaceName</span></span>
<span data-ttu-id="faaf0-116">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="faaf0-116">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="faaf0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faaf0-117">-DefaultProfile</span></span>
<span data-ttu-id="faaf0-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="faaf0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faaf0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faaf0-119">CommonParameters</span></span>
<span data-ttu-id="faaf0-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="faaf0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faaf0-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faaf0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faaf0-122">입력</span><span class="sxs-lookup"><span data-stu-id="faaf0-122">INPUTS</span></span>

## <span data-ttu-id="faaf0-123">출력</span><span class="sxs-lookup"><span data-stu-id="faaf0-123">OUTPUTS</span></span>

### <span data-ttu-id="faaf0-124">OperationalInsights. PSSearchGetSearchResultsResponse/.</span><span class="sxs-lookup"><span data-stu-id="faaf0-124">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSearchResultsResponse</span></span>

## <span data-ttu-id="faaf0-125">상속자</span><span class="sxs-lookup"><span data-stu-id="faaf0-125">NOTES</span></span>

## <span data-ttu-id="faaf0-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="faaf0-126">RELATED LINKS</span></span>

[<span data-ttu-id="faaf0-127">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="faaf0-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


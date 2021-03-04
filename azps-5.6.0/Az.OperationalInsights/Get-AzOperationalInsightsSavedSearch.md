---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: fe0d1e13b276f3282feaef2cf4eb5a9c687bb3b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958096"
---
# <span data-ttu-id="38150-101">Get-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="38150-101">Get-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="38150-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38150-102">SYNOPSIS</span></span>
<span data-ttu-id="38150-103">지정된 작업 영역의 저장된 모든 검색을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="38150-103">Returns all of the saved searches for a specified workspace.</span></span>

## <span data-ttu-id="38150-104">구문</span><span class="sxs-lookup"><span data-stu-id="38150-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38150-105">설명</span><span class="sxs-lookup"><span data-stu-id="38150-105">DESCRIPTION</span></span>
<span data-ttu-id="38150-106">**Get-AzOperationalInsightsSavedSearch** cmdlet은 저장된 검색 ID를 지정하지 않는 경우 지정된 리소스 그룹 내에서 지정된 작업 영역의 저장된 모든 검색을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="38150-106">The **Get-AzOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="38150-107">저장된 검색 ID를 지정하는 경우 해당 ID에 해당하는 저장된 검색이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="38150-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="38150-108">예제</span><span class="sxs-lookup"><span data-stu-id="38150-108">EXAMPLES</span></span>

### <span data-ttu-id="38150-109">예제 1: 작업 영역의 모든 저장된 검색을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="38150-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="38150-110">이 명령은 작업 영역과 연결된 모든 저장된 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="38150-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="38150-111">예제 2: ID로 특정 저장된 검색을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="38150-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="38150-112">이 명령은 해당 ID로 저장된 특정 검색을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="38150-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="38150-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="38150-113">PARAMETERS</span></span>

### <span data-ttu-id="38150-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38150-114">-DefaultProfile</span></span>
<span data-ttu-id="38150-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="38150-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38150-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38150-116">-ResourceGroupName</span></span>
<span data-ttu-id="38150-117">작업 영역이 포함된 Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38150-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="38150-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="38150-118">-SavedSearchId</span></span>
<span data-ttu-id="38150-119">저장된 검색 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38150-119">Specifies a saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38150-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="38150-120">-WorkspaceName</span></span>
<span data-ttu-id="38150-121">작업 영역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="38150-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="38150-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38150-122">CommonParameters</span></span>
<span data-ttu-id="38150-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="38150-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38150-124">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="38150-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38150-125">입력</span><span class="sxs-lookup"><span data-stu-id="38150-125">INPUTS</span></span>

### <span data-ttu-id="38150-126">System.String</span><span class="sxs-lookup"><span data-stu-id="38150-126">System.String</span></span>

## <span data-ttu-id="38150-127">출력</span><span class="sxs-lookup"><span data-stu-id="38150-127">OUTPUTS</span></span>

### <span data-ttu-id="38150-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="38150-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="38150-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span><span class="sxs-lookup"><span data-stu-id="38150-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="38150-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="38150-130">NOTES</span></span>

## <span data-ttu-id="38150-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38150-131">RELATED LINKS</span></span>

[<span data-ttu-id="38150-132">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="38150-132">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)



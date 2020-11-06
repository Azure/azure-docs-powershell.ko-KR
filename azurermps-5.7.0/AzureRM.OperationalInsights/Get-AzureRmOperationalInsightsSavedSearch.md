---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: FB2C47AD-E103-409E-A23B-BC316FA32E8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: 7022c7b2fcc9fb0f11ded4034a0c78c4faa65237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528890"
---
# <span data-ttu-id="b1cea-101">Get-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="b1cea-101">Get-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="b1cea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1cea-102">SYNOPSIS</span></span>
<span data-ttu-id="b1cea-103">지정 된 작업 영역에 대해 저장 된 모든 검색을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cea-103">Returns all of the saved searches for a specified workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1cea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1cea-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-SavedSearchId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1cea-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b1cea-105">DESCRIPTION</span></span>
<span data-ttu-id="b1cea-106">**AzureRmOperationalInsightsSavedSearch** cmdlet은 저장 된 검색 ID를 지정 하지 않은 경우 지정 된 리소스 그룹 내의 지정 된 작업 영역에 대 한 저장 검색을 모두 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cea-106">The **Get-AzureRmOperationalInsightsSavedSearch** cmdlet returns all of the saved searches for a specified workspace within the resource group specified if you do not specify a saved search ID.</span></span>
<span data-ttu-id="b1cea-107">저장 된 검색 ID를 지정 하면 해당 ID에 해당 하는 저장 된 검색이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1cea-107">If you do specify a saved search ID, then the saved search corresponding to that ID is returned.</span></span>

## <span data-ttu-id="b1cea-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b1cea-108">EXAMPLES</span></span>

### <span data-ttu-id="b1cea-109">예제 1: 작업 영역에 대해 저장 된 모든 검색 가져오기</span><span class="sxs-lookup"><span data-stu-id="b1cea-109">Example 1: Get all saved searches for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="b1cea-110">이 명령은 작업 영역과 연결 된 저장 된 모든 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1cea-110">This command gets all of the saved resources associated with a workspace.</span></span>

### <span data-ttu-id="b1cea-111">예제 2: ID를 기준으로 저장 된 특정 검색 가져오기</span><span class="sxs-lookup"><span data-stu-id="b1cea-111">Example 2: Get a specific saved search by ID</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId"
```

<span data-ttu-id="b1cea-112">이 명령은 해당 ID로 저장 된 특정 검색을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1cea-112">This command gets a specific saved search by its ID.</span></span>

## <span data-ttu-id="b1cea-113">변수</span><span class="sxs-lookup"><span data-stu-id="b1cea-113">PARAMETERS</span></span>

### <span data-ttu-id="b1cea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1cea-114">-DefaultProfile</span></span>
<span data-ttu-id="b1cea-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b1cea-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1cea-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1cea-116">-ResourceGroupName</span></span>
<span data-ttu-id="b1cea-117">작업 영역을 포함 하는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cea-117">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="b1cea-118">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="b1cea-118">-SavedSearchId</span></span>
<span data-ttu-id="b1cea-119">저장 된 검색 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cea-119">Specifies a saved search ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1cea-120">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b1cea-120">-WorkspaceName</span></span>
<span data-ttu-id="b1cea-121">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cea-121">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="b1cea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1cea-122">CommonParameters</span></span>
<span data-ttu-id="b1cea-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1cea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1cea-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1cea-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1cea-125">입력</span><span class="sxs-lookup"><span data-stu-id="b1cea-125">INPUTS</span></span>

### <span data-ttu-id="b1cea-126">않아야</span><span class="sxs-lookup"><span data-stu-id="b1cea-126">None</span></span>
<span data-ttu-id="b1cea-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1cea-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b1cea-128">출력</span><span class="sxs-lookup"><span data-stu-id="b1cea-128">OUTPUTS</span></span>

### <span data-ttu-id="b1cea-129">OperationalInsights. PSSearchListSavedSearchResponse/.</span><span class="sxs-lookup"><span data-stu-id="b1cea-129">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse</span></span>

### <span data-ttu-id="b1cea-130">OperationalInsights. PSSearchGetSavedSearchResponse/.</span><span class="sxs-lookup"><span data-stu-id="b1cea-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSavedSearchResponse</span></span>

## <span data-ttu-id="b1cea-131">상속자</span><span class="sxs-lookup"><span data-stu-id="b1cea-131">NOTES</span></span>

## <span data-ttu-id="b1cea-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1cea-132">RELATED LINKS</span></span>

[<span data-ttu-id="b1cea-133">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b1cea-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)



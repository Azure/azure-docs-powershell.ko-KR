---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: fdfe52151346bbf173226213c9450484d49fe040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527980"
---
# <span data-ttu-id="2b582-101">Set-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="2b582-101">Set-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="2b582-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b582-102">SYNOPSIS</span></span>
<span data-ttu-id="2b582-103">이미 존재 하는 저장 된 검색을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b582-103">Updates a saved search that already exists.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b582-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b582-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b582-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2b582-105">DESCRIPTION</span></span>
<span data-ttu-id="2b582-106">**Set-AzureRmOperationalInsightsSavedSearch** cmdlet은 이미 존재 하는 저장 된 검색을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b582-106">The **Set-AzureRmOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="2b582-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2b582-107">EXAMPLES</span></span>

### <span data-ttu-id="2b582-108">예제 1: 업데이트 된 속성을 사용 하 여 저장 된 검색 설정</span><span class="sxs-lookup"><span data-stu-id="2b582-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="2b582-109">이 명령은 업데이트 된 속성을 사용 하 여 저장 한 검색을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b582-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="2b582-110">변수</span><span class="sxs-lookup"><span data-stu-id="2b582-110">PARAMETERS</span></span>

### <span data-ttu-id="2b582-111">-범주</span><span class="sxs-lookup"><span data-stu-id="2b582-111">-Category</span></span>
<span data-ttu-id="2b582-112">범주 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b582-112">Specifies the category name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b582-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b582-113">-DefaultProfile</span></span>
<span data-ttu-id="2b582-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2b582-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b582-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2b582-115">-DisplayName</span></span>
<span data-ttu-id="2b582-116">표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b582-116">Specifies the display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b582-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="2b582-117">-ETag</span></span>
<span data-ttu-id="2b582-118">ETag 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b582-118">Specifies the ETag name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b582-119">-쿼리</span><span class="sxs-lookup"><span data-stu-id="2b582-119">-Query</span></span>
<span data-ttu-id="2b582-120">쿼리 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b582-120">Specifies the query name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b582-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b582-121">-ResourceGroupName</span></span>
<span data-ttu-id="2b582-122">리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b582-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="2b582-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="2b582-123">-SavedSearchId</span></span>
<span data-ttu-id="2b582-124">저장 된 검색 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b582-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="2b582-125">태그</span><span class="sxs-lookup"><span data-stu-id="2b582-125">-Tag</span></span>
<span data-ttu-id="2b582-126">저장 된 검색 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="2b582-126">The saved search tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b582-127">-버전</span><span class="sxs-lookup"><span data-stu-id="2b582-127">-Version</span></span>
```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b582-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2b582-128">-WorkspaceName</span></span>
<span data-ttu-id="2b582-129">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b582-129">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="2b582-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b582-130">CommonParameters</span></span>
<span data-ttu-id="2b582-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b582-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b582-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b582-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b582-133">입력</span><span class="sxs-lookup"><span data-stu-id="2b582-133">INPUTS</span></span>

### <span data-ttu-id="2b582-134">않아야</span><span class="sxs-lookup"><span data-stu-id="2b582-134">None</span></span>
<span data-ttu-id="2b582-135">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b582-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b582-136">출력</span><span class="sxs-lookup"><span data-stu-id="2b582-136">OUTPUTS</span></span>

## <span data-ttu-id="2b582-137">상속자</span><span class="sxs-lookup"><span data-stu-id="2b582-137">NOTES</span></span>

## <span data-ttu-id="2b582-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b582-138">RELATED LINKS</span></span>

[<span data-ttu-id="2b582-139">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2b582-139">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 25d973d6a568695fbca7371b229cf9bb18fcd5cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989716"
---
# <span data-ttu-id="aeca4-101">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="aeca4-101">Set-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="aeca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeca4-102">SYNOPSIS</span></span>
<span data-ttu-id="aeca4-103">이미 있는 저장된 검색을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="aeca4-103">Updates a saved search that already exists.</span></span>

## <span data-ttu-id="aeca4-104">구문</span><span class="sxs-lookup"><span data-stu-id="aeca4-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aeca4-105">설명</span><span class="sxs-lookup"><span data-stu-id="aeca4-105">DESCRIPTION</span></span>
<span data-ttu-id="aeca4-106">**Set-AzOperationalInsightsSavedSearch** cmdlet은 이미 있는 저장된 검색을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="aeca4-106">The **Set-AzOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="aeca4-107">예제</span><span class="sxs-lookup"><span data-stu-id="aeca4-107">EXAMPLES</span></span>

### <span data-ttu-id="aeca4-108">예제 1: 업데이트된 속성으로 저장된 검색 설정</span><span class="sxs-lookup"><span data-stu-id="aeca4-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="aeca4-109">이 명령은 업데이트된 속성으로 저장된 검색을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="aeca4-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="aeca4-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aeca4-110">PARAMETERS</span></span>

### <span data-ttu-id="aeca4-111">-Category</span><span class="sxs-lookup"><span data-stu-id="aeca4-111">-Category</span></span>
<span data-ttu-id="aeca4-112">범주 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aeca4-112">Specifies the category name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeca4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeca4-113">-DefaultProfile</span></span>
<span data-ttu-id="aeca4-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="aeca4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aeca4-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="aeca4-115">-DisplayName</span></span>
<span data-ttu-id="aeca4-116">표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aeca4-116">Specifies the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeca4-117">-ETag</span><span class="sxs-lookup"><span data-stu-id="aeca4-117">-ETag</span></span>
<span data-ttu-id="aeca4-118">ETag 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aeca4-118">Specifies the ETag name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeca4-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="aeca4-119">-FunctionAlias</span></span>
<span data-ttu-id="aeca4-120">쿼리가 함수 역할을 하는 경우 함수 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="aeca4-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeca4-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="aeca4-121">-FunctionParameter</span></span>
<span data-ttu-id="aeca4-122">쿼리가 함수 역할을 하는 경우 선택적 함수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="aeca4-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="aeca4-123">값은 'param-name1:type1 = default_value1, param-name2:type2 = default_value2.</span><span class="sxs-lookup"><span data-stu-id="aeca4-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="aeca4-124">자세한 예제 및 적절한 구문은 를 https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="aeca4-124">For more examples and proper syntax please refer to https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeca4-125">-쿼리</span><span class="sxs-lookup"><span data-stu-id="aeca4-125">-Query</span></span>
<span data-ttu-id="aeca4-126">쿼리 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aeca4-126">Specifies the query name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeca4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeca4-127">-ResourceGroupName</span></span>
<span data-ttu-id="aeca4-128">리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aeca4-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="aeca4-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="aeca4-129">-SavedSearchId</span></span>
<span data-ttu-id="aeca4-130">저장된 검색 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aeca4-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="aeca4-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="aeca4-131">-Tag</span></span>
<span data-ttu-id="aeca4-132">저장된 검색 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="aeca4-132">The saved search tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeca4-133">-Version</span><span class="sxs-lookup"><span data-stu-id="aeca4-133">-Version</span></span>
```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeca4-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aeca4-134">-WorkspaceName</span></span>
<span data-ttu-id="aeca4-135">작업 영역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aeca4-135">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="aeca4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeca4-136">CommonParameters</span></span>
<span data-ttu-id="aeca4-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aeca4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeca4-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aeca4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeca4-139">입력</span><span class="sxs-lookup"><span data-stu-id="aeca4-139">INPUTS</span></span>

### <span data-ttu-id="aeca4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="aeca4-140">System.String</span></span>

### <span data-ttu-id="aeca4-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="aeca4-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="aeca4-142">System.Int64</span><span class="sxs-lookup"><span data-stu-id="aeca4-142">System.Int64</span></span>

## <span data-ttu-id="aeca4-143">출력</span><span class="sxs-lookup"><span data-stu-id="aeca4-143">OUTPUTS</span></span>

### <span data-ttu-id="aeca4-144">System.Net.HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="aeca4-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="aeca4-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aeca4-145">NOTES</span></span>

## <span data-ttu-id="aeca4-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aeca4-146">RELATED LINKS</span></span>

[<span data-ttu-id="aeca4-147">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="aeca4-147">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)



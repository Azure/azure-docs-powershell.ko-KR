---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: cba56fd21263d4accba296cd7aab181f18b09200
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989907"
---
# <span data-ttu-id="b00ad-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="b00ad-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="b00ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b00ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b00ad-103">지정된 매개 변수를 사용하여 새 저장된 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="b00ad-104">구문</span><span class="sxs-lookup"><span data-stu-id="b00ad-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b00ad-105">설명</span><span class="sxs-lookup"><span data-stu-id="b00ad-105">DESCRIPTION</span></span>
<span data-ttu-id="b00ad-106">**New-AzOperationalInsightsSavedSearch** cmdlet은 작업 영역의 지정된 매개 변수를 사용하여 새 저장된 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="b00ad-107">예제</span><span class="sxs-lookup"><span data-stu-id="b00ad-107">EXAMPLES</span></span>

### <span data-ttu-id="b00ad-108">예제 1: 새 저장된 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="b00ad-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="b00ad-109">이 명령은 새 저장된 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="b00ad-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b00ad-110">PARAMETERS</span></span>

### <span data-ttu-id="b00ad-111">-Category</span><span class="sxs-lookup"><span data-stu-id="b00ad-111">-Category</span></span>
<span data-ttu-id="b00ad-112">범주 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="b00ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b00ad-113">-DefaultProfile</span></span>
<span data-ttu-id="b00ad-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b00ad-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b00ad-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b00ad-115">-DisplayName</span></span>
<span data-ttu-id="b00ad-116">저장된 검색 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="b00ad-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b00ad-117">-Force</span></span>
<span data-ttu-id="b00ad-118">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00ad-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="b00ad-119">-FunctionAlias</span></span>
<span data-ttu-id="b00ad-120">쿼리가 함수 역할을 하는 경우 함수 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-120">The function alias if query serves as a function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00ad-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="b00ad-121">-FunctionParameter</span></span>
<span data-ttu-id="b00ad-122">쿼리가 함수 역할을 하는 경우 선택적 함수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="b00ad-123">값은 'param-name1:type1 = default_value1, param-name2:type2 = default_value2.</span><span class="sxs-lookup"><span data-stu-id="b00ad-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="b00ad-124">자세한 예제 및 적절한 구문은 를 https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-124">For more examples and proper syntax please refer to https://docs.microsoft.com/azure/kusto/query/functions/user-defined-functions.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FunctionParameters

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00ad-125">-쿼리</span><span class="sxs-lookup"><span data-stu-id="b00ad-125">-Query</span></span>
<span data-ttu-id="b00ad-126">저장된 검색에 대한 쿼리 식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-126">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="b00ad-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b00ad-127">-ResourceGroupName</span></span>
<span data-ttu-id="b00ad-128">리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="b00ad-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="b00ad-129">-SavedSearchId</span></span>
<span data-ttu-id="b00ad-130">저장된 검색 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="b00ad-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="b00ad-131">-Tag</span></span>
<span data-ttu-id="b00ad-132">저장된 검색 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-132">The saved search tags.</span></span>

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

### <span data-ttu-id="b00ad-133">-Version</span><span class="sxs-lookup"><span data-stu-id="b00ad-133">-Version</span></span>
<span data-ttu-id="b00ad-134">버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-134">Specifies the version.</span></span>

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

### <span data-ttu-id="b00ad-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b00ad-135">-WorkspaceName</span></span>
<span data-ttu-id="b00ad-136">작업 영역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-136">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="b00ad-137">-확인</span><span class="sxs-lookup"><span data-stu-id="b00ad-137">-Confirm</span></span>
<span data-ttu-id="b00ad-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00ad-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b00ad-139">-WhatIf</span></span>
<span data-ttu-id="b00ad-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b00ad-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00ad-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b00ad-142">CommonParameters</span></span>
<span data-ttu-id="b00ad-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b00ad-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b00ad-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b00ad-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b00ad-145">입력</span><span class="sxs-lookup"><span data-stu-id="b00ad-145">INPUTS</span></span>

### <span data-ttu-id="b00ad-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b00ad-146">System.String</span></span>

### <span data-ttu-id="b00ad-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b00ad-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b00ad-148">System.Int64</span><span class="sxs-lookup"><span data-stu-id="b00ad-148">System.Int64</span></span>

## <span data-ttu-id="b00ad-149">출력</span><span class="sxs-lookup"><span data-stu-id="b00ad-149">OUTPUTS</span></span>

### <span data-ttu-id="b00ad-150">System.Net.HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="b00ad-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="b00ad-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b00ad-151">NOTES</span></span>

## <span data-ttu-id="b00ad-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b00ad-152">RELATED LINKS</span></span>

[<span data-ttu-id="b00ad-153">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b00ad-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)



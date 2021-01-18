---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 3426b93ec9551ba6218634fa87adeff09b5872af
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492510"
---
# <span data-ttu-id="4485f-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="4485f-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="4485f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4485f-102">SYNOPSIS</span></span>
<span data-ttu-id="4485f-103">지정된 매개 변수를 사용하여 저장된 새 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="4485f-104">구문</span><span class="sxs-lookup"><span data-stu-id="4485f-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4485f-105">설명</span><span class="sxs-lookup"><span data-stu-id="4485f-105">DESCRIPTION</span></span>
<span data-ttu-id="4485f-106">**New-AzOperationalInsightsSavedSearch** cmdlet은 작업 영역의 지정된 매개 변수를 사용하여 저장된 새 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="4485f-107">예제</span><span class="sxs-lookup"><span data-stu-id="4485f-107">EXAMPLES</span></span>

### <span data-ttu-id="4485f-108">예제 1: 저장된 새 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="4485f-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="4485f-109">이 명령은 저장된 새 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="4485f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4485f-110">PARAMETERS</span></span>

### <span data-ttu-id="4485f-111">-Category</span><span class="sxs-lookup"><span data-stu-id="4485f-111">-Category</span></span>
<span data-ttu-id="4485f-112">범주 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="4485f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4485f-113">-DefaultProfile</span></span>
<span data-ttu-id="4485f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4485f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4485f-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4485f-115">-DisplayName</span></span>
<span data-ttu-id="4485f-116">저장된 검색 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="4485f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4485f-117">-Force</span></span>
<span data-ttu-id="4485f-118">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4485f-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="4485f-119">-FunctionAlias</span></span>
<span data-ttu-id="4485f-120">쿼리가 함수 역할을 하는 경우 함수 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="4485f-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="4485f-121">-FunctionParameter</span></span>
<span data-ttu-id="4485f-122">쿼리가 함수 역할을 하는 경우 선택적 함수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="4485f-123">값은 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'입니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="4485f-124">더 많은 예제 및 적절한 구문은 다음을 https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="4485f-125">-Query</span><span class="sxs-lookup"><span data-stu-id="4485f-125">-Query</span></span>
<span data-ttu-id="4485f-126">저장된 검색에 대한 쿼리 식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-126">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="4485f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4485f-127">-ResourceGroupName</span></span>
<span data-ttu-id="4485f-128">리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="4485f-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="4485f-129">-SavedSearchId</span></span>
<span data-ttu-id="4485f-130">저장된 검색 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="4485f-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="4485f-131">-Tag</span></span>
<span data-ttu-id="4485f-132">저장된 검색 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-132">The saved search tags.</span></span>

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

### <span data-ttu-id="4485f-133">-Version</span><span class="sxs-lookup"><span data-stu-id="4485f-133">-Version</span></span>
<span data-ttu-id="4485f-134">버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-134">Specifies the version.</span></span>

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

### <span data-ttu-id="4485f-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4485f-135">-WorkspaceName</span></span>
<span data-ttu-id="4485f-136">작업 영역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-136">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="4485f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4485f-137">-Confirm</span></span>
<span data-ttu-id="4485f-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4485f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4485f-139">-WhatIf</span></span>
<span data-ttu-id="4485f-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4485f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4485f-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4485f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4485f-142">CommonParameters</span></span>
<span data-ttu-id="4485f-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4485f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4485f-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4485f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4485f-145">입력</span><span class="sxs-lookup"><span data-stu-id="4485f-145">INPUTS</span></span>

### <span data-ttu-id="4485f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="4485f-146">System.String</span></span>

### <span data-ttu-id="4485f-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4485f-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4485f-148">System.Int64</span><span class="sxs-lookup"><span data-stu-id="4485f-148">System.Int64</span></span>

## <span data-ttu-id="4485f-149">출력</span><span class="sxs-lookup"><span data-stu-id="4485f-149">OUTPUTS</span></span>

### <span data-ttu-id="4485f-150">System.Net.HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="4485f-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="4485f-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4485f-151">NOTES</span></span>

## <span data-ttu-id="4485f-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4485f-152">RELATED LINKS</span></span>

[<span data-ttu-id="4485f-153">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4485f-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 3426b93ec9551ba6218634fa87adeff09b5872af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216038"
---
# <span data-ttu-id="99b17-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="99b17-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="99b17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99b17-102">SYNOPSIS</span></span>
<span data-ttu-id="99b17-103">지정 된 매개 변수를 사용 하 여 새 저장 된 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="99b17-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99b17-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [[-FunctionAlias] <String>] [[-FunctionParameter] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99b17-105">설명은</span><span class="sxs-lookup"><span data-stu-id="99b17-105">DESCRIPTION</span></span>
<span data-ttu-id="99b17-106">**AzOperationalInsightsSavedSearch** cmdlet은 작업 영역에 대해 지정 된 매개 변수를 사용 하 여 새 저장 된 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="99b17-107">예제의</span><span class="sxs-lookup"><span data-stu-id="99b17-107">EXAMPLES</span></span>

### <span data-ttu-id="99b17-108">예제 1: 새 저장 된 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="99b17-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="99b17-109">이 명령은 저장 된 새 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="99b17-110">변수</span><span class="sxs-lookup"><span data-stu-id="99b17-110">PARAMETERS</span></span>

### <span data-ttu-id="99b17-111">-범주</span><span class="sxs-lookup"><span data-stu-id="99b17-111">-Category</span></span>
<span data-ttu-id="99b17-112">범주 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="99b17-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b17-113">-DefaultProfile</span></span>
<span data-ttu-id="99b17-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="99b17-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99b17-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="99b17-115">-DisplayName</span></span>
<span data-ttu-id="99b17-116">저장 된 검색 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="99b17-117">-Force</span><span class="sxs-lookup"><span data-stu-id="99b17-117">-Force</span></span>
<span data-ttu-id="99b17-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99b17-119">-FunctionAlias</span><span class="sxs-lookup"><span data-stu-id="99b17-119">-FunctionAlias</span></span>
<span data-ttu-id="99b17-120">If 쿼리가 함수의 역할을 하는 경우 함수 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-120">The function alias if query serves as a function.</span></span>

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

### <span data-ttu-id="99b17-121">-FunctionParameter</span><span class="sxs-lookup"><span data-stu-id="99b17-121">-FunctionParameter</span></span>
<span data-ttu-id="99b17-122">Query가 함수 역할을 하는 경우 선택적 함수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-122">The optional function parameters if query serves as a function.</span></span> <span data-ttu-id="99b17-123">값은 ' param-name1: type1 = default_value1, param-name2: type2 = default_value2 형식 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-123">Value should be in the following format: 'param-name1:type1 = default_value1, param-name2:type2 = default_value2'.</span></span> <span data-ttu-id="99b17-124">더 많은 예와 적절 한 구문을 참조 하세요 https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions .</span><span class="sxs-lookup"><span data-stu-id="99b17-124">For more examples and proper syntax please refer to https://docs.microsoft.com/en-us/azure/kusto/query/functions/user-defined-functions.</span></span>

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

### <span data-ttu-id="99b17-125">-쿼리</span><span class="sxs-lookup"><span data-stu-id="99b17-125">-Query</span></span>
<span data-ttu-id="99b17-126">저장 된 검색에 대 한 쿼리 식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-126">Specifies the query expression for the saved search.</span></span>

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

### <span data-ttu-id="99b17-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99b17-127">-ResourceGroupName</span></span>
<span data-ttu-id="99b17-128">리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-128">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="99b17-129">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="99b17-129">-SavedSearchId</span></span>
<span data-ttu-id="99b17-130">저장 된 검색 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-130">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="99b17-131">태그</span><span class="sxs-lookup"><span data-stu-id="99b17-131">-Tag</span></span>
<span data-ttu-id="99b17-132">저장 된 검색 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-132">The saved search tags.</span></span>

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

### <span data-ttu-id="99b17-133">-버전</span><span class="sxs-lookup"><span data-stu-id="99b17-133">-Version</span></span>
<span data-ttu-id="99b17-134">버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-134">Specifies the version.</span></span>

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

### <span data-ttu-id="99b17-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="99b17-135">-WorkspaceName</span></span>
<span data-ttu-id="99b17-136">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-136">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="99b17-137">-확인</span><span class="sxs-lookup"><span data-stu-id="99b17-137">-Confirm</span></span>
<span data-ttu-id="99b17-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99b17-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99b17-139">-WhatIf</span></span>
<span data-ttu-id="99b17-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99b17-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99b17-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b17-142">CommonParameters</span></span>
<span data-ttu-id="99b17-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99b17-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b17-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="99b17-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b17-145">입력</span><span class="sxs-lookup"><span data-stu-id="99b17-145">INPUTS</span></span>

### <span data-ttu-id="99b17-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="99b17-146">System.String</span></span>

### <span data-ttu-id="99b17-147">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="99b17-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="99b17-148">시스템 Int64</span><span class="sxs-lookup"><span data-stu-id="99b17-148">System.Int64</span></span>

## <span data-ttu-id="99b17-149">출력</span><span class="sxs-lookup"><span data-stu-id="99b17-149">OUTPUTS</span></span>

### <span data-ttu-id="99b17-150">System .Net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="99b17-150">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="99b17-151">상속자</span><span class="sxs-lookup"><span data-stu-id="99b17-151">NOTES</span></span>

## <span data-ttu-id="99b17-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99b17-152">RELATED LINKS</span></span>

[<span data-ttu-id="99b17-153">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="99b17-153">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)



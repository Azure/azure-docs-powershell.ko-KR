---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 5853447dfc91511782e99ebafae644e14b6649b3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93701922"
---
# <span data-ttu-id="e24ed-101">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="e24ed-101">New-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="e24ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e24ed-102">SYNOPSIS</span></span>
<span data-ttu-id="e24ed-103">지정 된 매개 변수를 사용 하 여 새 저장 된 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e24ed-103">Creates a new saved search with the specified parameters.</span></span>

## <span data-ttu-id="e24ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e24ed-104">SYNTAX</span></span>

```
New-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tag] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e24ed-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e24ed-105">DESCRIPTION</span></span>
<span data-ttu-id="e24ed-106">**AzOperationalInsightsSavedSearch** cmdlet은 작업 영역에 대해 지정 된 매개 변수를 사용 하 여 새 저장 된 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e24ed-106">The **New-AzOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="e24ed-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e24ed-107">EXAMPLES</span></span>

### <span data-ttu-id="e24ed-108">예제 1: 새 저장 된 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="e24ed-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="e24ed-109">이 명령은 저장 된 새 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e24ed-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="e24ed-110">변수</span><span class="sxs-lookup"><span data-stu-id="e24ed-110">PARAMETERS</span></span>

### <span data-ttu-id="e24ed-111">-범주</span><span class="sxs-lookup"><span data-stu-id="e24ed-111">-Category</span></span>
<span data-ttu-id="e24ed-112">범주 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e24ed-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="e24ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e24ed-113">-DefaultProfile</span></span>
<span data-ttu-id="e24ed-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e24ed-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e24ed-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e24ed-115">-DisplayName</span></span>
<span data-ttu-id="e24ed-116">저장 된 검색 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e24ed-116">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="e24ed-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e24ed-117">-Force</span></span>
<span data-ttu-id="e24ed-118">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e24ed-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e24ed-119">-쿼리</span><span class="sxs-lookup"><span data-stu-id="e24ed-119">-Query</span></span>
<span data-ttu-id="e24ed-120">쿼리 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e24ed-120">Specifies the query name.</span></span>

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

### <span data-ttu-id="e24ed-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e24ed-121">-ResourceGroupName</span></span>
<span data-ttu-id="e24ed-122">리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e24ed-122">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="e24ed-123">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="e24ed-123">-SavedSearchId</span></span>
<span data-ttu-id="e24ed-124">저장 된 검색 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e24ed-124">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="e24ed-125">태그</span><span class="sxs-lookup"><span data-stu-id="e24ed-125">-Tag</span></span>
<span data-ttu-id="e24ed-126">저장 된 검색 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="e24ed-126">The saved search tags.</span></span>

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

### <span data-ttu-id="e24ed-127">-버전</span><span class="sxs-lookup"><span data-stu-id="e24ed-127">-Version</span></span>
<span data-ttu-id="e24ed-128">버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e24ed-128">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e24ed-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e24ed-129">-WorkspaceName</span></span>
<span data-ttu-id="e24ed-130">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e24ed-130">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="e24ed-131">-확인</span><span class="sxs-lookup"><span data-stu-id="e24ed-131">-Confirm</span></span>
<span data-ttu-id="e24ed-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e24ed-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e24ed-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e24ed-133">-WhatIf</span></span>
<span data-ttu-id="e24ed-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e24ed-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e24ed-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e24ed-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e24ed-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e24ed-136">CommonParameters</span></span>
<span data-ttu-id="e24ed-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e24ed-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e24ed-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e24ed-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e24ed-139">입력</span><span class="sxs-lookup"><span data-stu-id="e24ed-139">INPUTS</span></span>

### <span data-ttu-id="e24ed-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e24ed-140">System.String</span></span>

### <span data-ttu-id="e24ed-141">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="e24ed-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e24ed-142">시스템 Int64</span><span class="sxs-lookup"><span data-stu-id="e24ed-142">System.Int64</span></span>

## <span data-ttu-id="e24ed-143">출력</span><span class="sxs-lookup"><span data-stu-id="e24ed-143">OUTPUTS</span></span>

### <span data-ttu-id="e24ed-144">System .Net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="e24ed-144">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="e24ed-145">상속자</span><span class="sxs-lookup"><span data-stu-id="e24ed-145">NOTES</span></span>

## <span data-ttu-id="e24ed-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e24ed-146">RELATED LINKS</span></span>

[<span data-ttu-id="e24ed-147">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e24ed-147">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)



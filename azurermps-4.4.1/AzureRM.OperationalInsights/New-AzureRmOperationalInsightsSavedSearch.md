---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: DFEB9EA3-574A-463B-8B70-46D76ABCA84D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: a233e41ed91a40e8fb16ccda7ed640f8ad5239ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529226"
---
# <span data-ttu-id="aba3b-101">New-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="aba3b-101">New-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="aba3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aba3b-102">SYNOPSIS</span></span>
<span data-ttu-id="aba3b-103">지정 된 매개 변수를 사용 하 여 새 저장 된 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aba3b-103">Creates a new saved search with the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aba3b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aba3b-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tags] <Hashtable>]
 [[-Version] <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aba3b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aba3b-105">DESCRIPTION</span></span>
<span data-ttu-id="aba3b-106">**AzureRmOperationalInsightsSavedSearch** cmdlet은 작업 영역에 대해 지정 된 매개 변수를 사용 하 여 새 저장 된 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aba3b-106">The **New-AzureRmOperationalInsightsSavedSearch** cmdlet creates a new saved search with the specified parameters for the workspace.</span></span>

## <span data-ttu-id="aba3b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="aba3b-107">EXAMPLES</span></span>

### <span data-ttu-id="aba3b-108">예제 1: 새 저장 된 검색 만들기</span><span class="sxs-lookup"><span data-stu-id="aba3b-108">Example 1: Create a new saved search</span></span>
```
PS C:\>New-AzureRmOperationalInsightSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "*" -Version $Version -Force
```

<span data-ttu-id="aba3b-109">이 명령은 저장 된 새 검색을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aba3b-109">This command creates a new saved search.</span></span>

## <span data-ttu-id="aba3b-110">변수</span><span class="sxs-lookup"><span data-stu-id="aba3b-110">PARAMETERS</span></span>

### <span data-ttu-id="aba3b-111">-범주</span><span class="sxs-lookup"><span data-stu-id="aba3b-111">-Category</span></span>
<span data-ttu-id="aba3b-112">범주 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aba3b-112">Specifies the category name.</span></span>

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

### <span data-ttu-id="aba3b-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="aba3b-113">-DisplayName</span></span>
<span data-ttu-id="aba3b-114">저장 된 검색 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aba3b-114">Specifies the saved search display name.</span></span>

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

### <span data-ttu-id="aba3b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="aba3b-115">-Force</span></span>
<span data-ttu-id="aba3b-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="aba3b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aba3b-117">-쿼리</span><span class="sxs-lookup"><span data-stu-id="aba3b-117">-Query</span></span>
<span data-ttu-id="aba3b-118">쿼리 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aba3b-118">Specifies the query name.</span></span>

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

### <span data-ttu-id="aba3b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aba3b-119">-ResourceGroupName</span></span>
<span data-ttu-id="aba3b-120">리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aba3b-120">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="aba3b-121">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="aba3b-121">-SavedSearchId</span></span>
<span data-ttu-id="aba3b-122">저장 된 검색 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aba3b-122">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="aba3b-123">태그</span><span class="sxs-lookup"><span data-stu-id="aba3b-123">-Tags</span></span>
<span data-ttu-id="aba3b-124">저장 된 검색에 대 한 리소스 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aba3b-124">Specifies the resource tags for the saved search.</span></span>

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

### <span data-ttu-id="aba3b-125">-버전</span><span class="sxs-lookup"><span data-stu-id="aba3b-125">-Version</span></span>
<span data-ttu-id="aba3b-126">버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aba3b-126">Specifies the version.</span></span>

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

### <span data-ttu-id="aba3b-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aba3b-127">-WorkspaceName</span></span>
<span data-ttu-id="aba3b-128">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aba3b-128">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="aba3b-129">-확인</span><span class="sxs-lookup"><span data-stu-id="aba3b-129">-Confirm</span></span>
<span data-ttu-id="aba3b-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aba3b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aba3b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aba3b-131">-WhatIf</span></span>
<span data-ttu-id="aba3b-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aba3b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aba3b-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aba3b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aba3b-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba3b-134">-DefaultProfile</span></span>
<span data-ttu-id="aba3b-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aba3b-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aba3b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba3b-136">CommonParameters</span></span>
<span data-ttu-id="aba3b-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aba3b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba3b-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aba3b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba3b-139">입력</span><span class="sxs-lookup"><span data-stu-id="aba3b-139">INPUTS</span></span>

## <span data-ttu-id="aba3b-140">출력</span><span class="sxs-lookup"><span data-stu-id="aba3b-140">OUTPUTS</span></span>

## <span data-ttu-id="aba3b-141">상속자</span><span class="sxs-lookup"><span data-stu-id="aba3b-141">NOTES</span></span>

## <span data-ttu-id="aba3b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aba3b-142">RELATED LINKS</span></span>

[<span data-ttu-id="aba3b-143">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="aba3b-143">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)



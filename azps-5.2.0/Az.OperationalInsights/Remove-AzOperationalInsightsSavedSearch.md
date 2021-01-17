---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: f9bf63a65642e62e7f0416f0f053ef62277fa9bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337593"
---
# <span data-ttu-id="f0786-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="f0786-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="f0786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0786-102">SYNOPSIS</span></span>
<span data-ttu-id="f0786-103">작업 영역의 저장된 검색을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f0786-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="f0786-104">구문</span><span class="sxs-lookup"><span data-stu-id="f0786-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0786-105">설명</span><span class="sxs-lookup"><span data-stu-id="f0786-105">DESCRIPTION</span></span>
<span data-ttu-id="f0786-106">**Remove-AzOperationalInsightsSavedSearch** cmdlet은 작업 영역의 저장된 검색을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f0786-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="f0786-107">예제</span><span class="sxs-lookup"><span data-stu-id="f0786-107">EXAMPLES</span></span>

### <span data-ttu-id="f0786-108">예제 1: 저장된 검색 제거</span><span class="sxs-lookup"><span data-stu-id="f0786-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="f0786-109">이 명령은 작업 영역의 저장된 검색을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f0786-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="f0786-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0786-110">PARAMETERS</span></span>

### <span data-ttu-id="f0786-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0786-111">-DefaultProfile</span></span>
<span data-ttu-id="f0786-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f0786-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0786-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0786-113">-ResourceGroupName</span></span>
<span data-ttu-id="f0786-114">작업 영역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0786-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="f0786-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="f0786-115">-SavedSearchId</span></span>
<span data-ttu-id="f0786-116">저장된 검색 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0786-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="f0786-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f0786-117">-WorkspaceName</span></span>
<span data-ttu-id="f0786-118">작업 영역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0786-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="f0786-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0786-119">-Confirm</span></span>
<span data-ttu-id="f0786-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0786-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0786-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0786-121">-WhatIf</span></span>
<span data-ttu-id="f0786-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f0786-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0786-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0786-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0786-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0786-124">CommonParameters</span></span>
<span data-ttu-id="f0786-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f0786-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0786-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f0786-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0786-127">입력</span><span class="sxs-lookup"><span data-stu-id="f0786-127">INPUTS</span></span>

### <span data-ttu-id="f0786-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f0786-128">System.String</span></span>

## <span data-ttu-id="f0786-129">출력</span><span class="sxs-lookup"><span data-stu-id="f0786-129">OUTPUTS</span></span>

### <span data-ttu-id="f0786-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="f0786-130">System.Void</span></span>

## <span data-ttu-id="f0786-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f0786-131">NOTES</span></span>

## <span data-ttu-id="f0786-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0786-132">RELATED LINKS</span></span>

[<span data-ttu-id="f0786-133">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f0786-133">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 404624f85dcf5647055ced9cd4ad55b373215c7d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93880261"
---
# <span data-ttu-id="3ddee-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="3ddee-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="3ddee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ddee-102">SYNOPSIS</span></span>
<span data-ttu-id="3ddee-103">작업 영역에서 저장 된 검색을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ddee-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="3ddee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ddee-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ddee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3ddee-105">DESCRIPTION</span></span>
<span data-ttu-id="3ddee-106">**Remove-AzOperationalInsightsSavedSearch** cmdlet은 작업 영역에서 저장 된 검색을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ddee-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="3ddee-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3ddee-107">EXAMPLES</span></span>

### <span data-ttu-id="3ddee-108">예제 1: 저장 된 검색 제거</span><span class="sxs-lookup"><span data-stu-id="3ddee-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="3ddee-109">이 명령은 작업 영역에서 저장 된 검색을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ddee-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="3ddee-110">변수</span><span class="sxs-lookup"><span data-stu-id="3ddee-110">PARAMETERS</span></span>

### <span data-ttu-id="3ddee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ddee-111">-DefaultProfile</span></span>
<span data-ttu-id="3ddee-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3ddee-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ddee-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ddee-113">-ResourceGroupName</span></span>
<span data-ttu-id="3ddee-114">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ddee-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="3ddee-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="3ddee-115">-SavedSearchId</span></span>
<span data-ttu-id="3ddee-116">저장 된 검색 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ddee-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="3ddee-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3ddee-117">-WorkspaceName</span></span>
<span data-ttu-id="3ddee-118">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ddee-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="3ddee-119">-확인</span><span class="sxs-lookup"><span data-stu-id="3ddee-119">-Confirm</span></span>
<span data-ttu-id="3ddee-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ddee-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ddee-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ddee-121">-WhatIf</span></span>
<span data-ttu-id="3ddee-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3ddee-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ddee-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ddee-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ddee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ddee-124">CommonParameters</span></span>
<span data-ttu-id="3ddee-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ddee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ddee-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ddee-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ddee-127">입력</span><span class="sxs-lookup"><span data-stu-id="3ddee-127">INPUTS</span></span>

### <span data-ttu-id="3ddee-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3ddee-128">System.String</span></span>

## <span data-ttu-id="3ddee-129">출력</span><span class="sxs-lookup"><span data-stu-id="3ddee-129">OUTPUTS</span></span>

### <span data-ttu-id="3ddee-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="3ddee-130">System.Void</span></span>

## <span data-ttu-id="3ddee-131">상속자</span><span class="sxs-lookup"><span data-stu-id="3ddee-131">NOTES</span></span>

## <span data-ttu-id="3ddee-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ddee-132">RELATED LINKS</span></span>

[<span data-ttu-id="3ddee-133">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3ddee-133">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)



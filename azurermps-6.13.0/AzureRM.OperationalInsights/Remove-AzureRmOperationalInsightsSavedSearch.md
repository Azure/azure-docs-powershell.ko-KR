---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: a438a84a25e100539f485b5d3a7012f03ee355a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531345"
---
# <span data-ttu-id="ad2e7-101">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="ad2e7-101">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="ad2e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad2e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ad2e7-103">작업 영역에서 저장 된 검색을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e7-103">Removes a saved search from the workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad2e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad2e7-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad2e7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ad2e7-105">DESCRIPTION</span></span>
<span data-ttu-id="ad2e7-106">**Remove-AzureRmOperationalInsightsSavedSearch** cmdlet은 작업 영역에서 저장 된 검색을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e7-106">The **Remove-AzureRmOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="ad2e7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ad2e7-107">EXAMPLES</span></span>

### <span data-ttu-id="ad2e7-108">예제 1: 저장 된 검색 제거</span><span class="sxs-lookup"><span data-stu-id="ad2e7-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="ad2e7-109">이 명령은 작업 영역에서 저장 된 검색을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e7-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="ad2e7-110">변수</span><span class="sxs-lookup"><span data-stu-id="ad2e7-110">PARAMETERS</span></span>

### <span data-ttu-id="ad2e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad2e7-111">-DefaultProfile</span></span>
<span data-ttu-id="ad2e7-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ad2e7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad2e7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad2e7-113">-ResourceGroupName</span></span>
<span data-ttu-id="ad2e7-114">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e7-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="ad2e7-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="ad2e7-115">-SavedSearchId</span></span>
<span data-ttu-id="ad2e7-116">저장 된 검색 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e7-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="ad2e7-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ad2e7-117">-WorkspaceName</span></span>
<span data-ttu-id="ad2e7-118">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e7-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="ad2e7-119">-확인</span><span class="sxs-lookup"><span data-stu-id="ad2e7-119">-Confirm</span></span>
<span data-ttu-id="ad2e7-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad2e7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad2e7-121">-WhatIf</span></span>
<span data-ttu-id="ad2e7-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad2e7-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad2e7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad2e7-124">CommonParameters</span></span>
<span data-ttu-id="ad2e7-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad2e7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad2e7-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad2e7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad2e7-127">입력</span><span class="sxs-lookup"><span data-stu-id="ad2e7-127">INPUTS</span></span>

### <span data-ttu-id="ad2e7-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ad2e7-128">System.String</span></span>

## <span data-ttu-id="ad2e7-129">출력</span><span class="sxs-lookup"><span data-stu-id="ad2e7-129">OUTPUTS</span></span>

### <span data-ttu-id="ad2e7-130">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="ad2e7-130">System.Void</span></span>

## <span data-ttu-id="ad2e7-131">상속자</span><span class="sxs-lookup"><span data-stu-id="ad2e7-131">NOTES</span></span>

## <span data-ttu-id="ad2e7-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad2e7-132">RELATED LINKS</span></span>

[<span data-ttu-id="ad2e7-133">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ad2e7-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 31c9728a95e5cfc52b283a8dddc0e24ffffe1630
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976352"
---
# <span data-ttu-id="c80fa-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="c80fa-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="c80fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c80fa-102">SYNOPSIS</span></span>
<span data-ttu-id="c80fa-103">책갈피를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c80fa-103">Create a Bookmark.</span></span>

## <span data-ttu-id="c80fa-104">구문</span><span class="sxs-lookup"><span data-stu-id="c80fa-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c80fa-105">설명</span><span class="sxs-lookup"><span data-stu-id="c80fa-105">DESCRIPTION</span></span>
<span data-ttu-id="c80fa-106">**New-AzSentinelBookmark** cmdlet은 지정된 작업 영역의 책갈피를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c80fa-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="c80fa-107">확인 매개  변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c80fa-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="c80fa-108">예제</span><span class="sxs-lookup"><span data-stu-id="c80fa-108">EXAMPLES</span></span>

### <span data-ttu-id="c80fa-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="c80fa-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="c80fa-110">이 예제에서는  지정된 작업 영역의 책갈피를 만든 다음, 해당 책갈피를 $Bookmark 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c80fa-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="c80fa-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c80fa-111">PARAMETERS</span></span>

### <span data-ttu-id="c80fa-112">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="c80fa-112">-BookmarkId</span></span>
<span data-ttu-id="c80fa-113">책갈피 ID,</span><span class="sxs-lookup"><span data-stu-id="c80fa-113">Bookmark Id,</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c80fa-114">-DefaultProfile</span></span>
<span data-ttu-id="c80fa-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c80fa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c80fa-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c80fa-116">-DisplayName</span></span>
<span data-ttu-id="c80fa-117">책갈피 규칙 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c80fa-117">Bookmark Rule Display Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80fa-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="c80fa-118">-IncidentInfo</span></span>
<span data-ttu-id="c80fa-119">책갈피 인시던트 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="c80fa-119">Bookmark Incident Info.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c80fa-120">-Label</span><span class="sxs-lookup"><span data-stu-id="c80fa-120">-Label</span></span>
<span data-ttu-id="c80fa-121">인시던트 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="c80fa-121">Incident Labels.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80fa-122">-Notes</span><span class="sxs-lookup"><span data-stu-id="c80fa-122">-Notes</span></span>
<span data-ttu-id="c80fa-123">책갈피 노트.</span><span class="sxs-lookup"><span data-stu-id="c80fa-123">Bookmark Notes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80fa-124">-쿼리</span><span class="sxs-lookup"><span data-stu-id="c80fa-124">-Query</span></span>
<span data-ttu-id="c80fa-125">책갈피 쿼리.</span><span class="sxs-lookup"><span data-stu-id="c80fa-125">Bookmark Query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80fa-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="c80fa-126">-QueryResult</span></span>
<span data-ttu-id="c80fa-127">책갈피 쿼리 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="c80fa-127">Bookmark Query Result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80fa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c80fa-128">-ResourceGroupName</span></span>
<span data-ttu-id="c80fa-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c80fa-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80fa-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c80fa-130">-WorkspaceName</span></span>
<span data-ttu-id="c80fa-131">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c80fa-131">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80fa-132">-확인</span><span class="sxs-lookup"><span data-stu-id="c80fa-132">-Confirm</span></span>
<span data-ttu-id="c80fa-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c80fa-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80fa-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c80fa-134">-WhatIf</span></span>
<span data-ttu-id="c80fa-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c80fa-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c80fa-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c80fa-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80fa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c80fa-137">CommonParameters</span></span>
<span data-ttu-id="c80fa-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c80fa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c80fa-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c80fa-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c80fa-140">입력</span><span class="sxs-lookup"><span data-stu-id="c80fa-140">INPUTS</span></span>

### <span data-ttu-id="c80fa-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="c80fa-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="c80fa-142">출력</span><span class="sxs-lookup"><span data-stu-id="c80fa-142">OUTPUTS</span></span>

### <span data-ttu-id="c80fa-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="c80fa-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="c80fa-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c80fa-144">NOTES</span></span>

## <span data-ttu-id="c80fa-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c80fa-145">RELATED LINKS</span></span>

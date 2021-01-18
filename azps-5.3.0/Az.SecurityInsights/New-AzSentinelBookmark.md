---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 3c30edd841eb2e773c5d813e798e63fc9858437d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494937"
---
# <span data-ttu-id="dda38-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="dda38-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="dda38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dda38-102">SYNOPSIS</span></span>
<span data-ttu-id="dda38-103">책갈피를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dda38-103">Create a Bookmark.</span></span>

## <span data-ttu-id="dda38-104">구문</span><span class="sxs-lookup"><span data-stu-id="dda38-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dda38-105">설명</span><span class="sxs-lookup"><span data-stu-id="dda38-105">DESCRIPTION</span></span>
<span data-ttu-id="dda38-106">**New-AzSentinelBookmark** cmdlet은 지정된 작업 영역의 책갈피를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dda38-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="dda38-107">*Confirm* 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dda38-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="dda38-108">예제</span><span class="sxs-lookup"><span data-stu-id="dda38-108">EXAMPLES</span></span>

### <span data-ttu-id="dda38-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="dda38-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="dda38-110">이 예제에서는  지정된 작업 영역의 책갈피를 만든 다음 책갈피 $Bookmark 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="dda38-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="dda38-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dda38-111">PARAMETERS</span></span>

### <span data-ttu-id="dda38-112">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="dda38-112">-BookmarkId</span></span>
<span data-ttu-id="dda38-113">책갈피 ID,</span><span class="sxs-lookup"><span data-stu-id="dda38-113">Bookmark Id,</span></span>

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

### <span data-ttu-id="dda38-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda38-114">-DefaultProfile</span></span>
<span data-ttu-id="dda38-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dda38-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dda38-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dda38-116">-DisplayName</span></span>
<span data-ttu-id="dda38-117">책갈피 규칙 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dda38-117">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="dda38-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="dda38-118">-IncidentInfo</span></span>
<span data-ttu-id="dda38-119">책갈피 인시던트 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="dda38-119">Bookmark Incident Info.</span></span>

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

### <span data-ttu-id="dda38-120">-Label</span><span class="sxs-lookup"><span data-stu-id="dda38-120">-Label</span></span>
<span data-ttu-id="dda38-121">인시던트 레이블.</span><span class="sxs-lookup"><span data-stu-id="dda38-121">Incident Labels.</span></span>

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

### <span data-ttu-id="dda38-122">-Notes</span><span class="sxs-lookup"><span data-stu-id="dda38-122">-Notes</span></span>
<span data-ttu-id="dda38-123">책갈피 노트.</span><span class="sxs-lookup"><span data-stu-id="dda38-123">Bookmark Notes.</span></span>

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

### <span data-ttu-id="dda38-124">-Query</span><span class="sxs-lookup"><span data-stu-id="dda38-124">-Query</span></span>
<span data-ttu-id="dda38-125">책갈피 쿼리.</span><span class="sxs-lookup"><span data-stu-id="dda38-125">Bookmark Query.</span></span>

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

### <span data-ttu-id="dda38-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="dda38-126">-QueryResult</span></span>
<span data-ttu-id="dda38-127">책갈피 쿼리 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="dda38-127">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="dda38-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dda38-128">-ResourceGroupName</span></span>
<span data-ttu-id="dda38-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dda38-129">Resource group name.</span></span>

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

### <span data-ttu-id="dda38-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dda38-130">-WorkspaceName</span></span>
<span data-ttu-id="dda38-131">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dda38-131">Workspace Name.</span></span>

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

### <span data-ttu-id="dda38-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dda38-132">-Confirm</span></span>
<span data-ttu-id="dda38-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dda38-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dda38-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dda38-134">-WhatIf</span></span>
<span data-ttu-id="dda38-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dda38-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dda38-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dda38-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dda38-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda38-137">CommonParameters</span></span>
<span data-ttu-id="dda38-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dda38-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda38-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dda38-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda38-140">입력</span><span class="sxs-lookup"><span data-stu-id="dda38-140">INPUTS</span></span>

### <span data-ttu-id="dda38-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="dda38-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="dda38-142">출력</span><span class="sxs-lookup"><span data-stu-id="dda38-142">OUTPUTS</span></span>

### <span data-ttu-id="dda38-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="dda38-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="dda38-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dda38-144">NOTES</span></span>

## <span data-ttu-id="dda38-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dda38-145">RELATED LINKS</span></span>

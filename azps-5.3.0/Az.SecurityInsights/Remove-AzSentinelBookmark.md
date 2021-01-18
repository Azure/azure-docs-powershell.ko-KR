---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
ms.openlocfilehash: 544c019fd52c0cb5723cbeafb5a82df072ac284e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494921"
---
# <span data-ttu-id="e8e59-101">Remove-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="e8e59-101">Remove-AzSentinelBookmark</span></span>

## <span data-ttu-id="e8e59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8e59-102">SYNOPSIS</span></span>
<span data-ttu-id="e8e59-103">책갈피를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e59-103">Delete a Bookmark.</span></span>

## <span data-ttu-id="e8e59-104">구문</span><span class="sxs-lookup"><span data-stu-id="e8e59-104">SYNTAX</span></span>

### <span data-ttu-id="e8e59-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="e8e59-105">BookmarkId.</span></span> <span data-ttu-id="e8e59-106">(기본값)</span><span class="sxs-lookup"><span data-stu-id="e8e59-106">(Default)</span></span>
```
Remove-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8e59-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e8e59-107">InputObject</span></span>
```
Remove-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8e59-108">설명</span><span class="sxs-lookup"><span data-stu-id="e8e59-108">DESCRIPTION</span></span>
<span data-ttu-id="e8e59-109">**Remove-AzSentinelBookmark** cmdlet은 지정된 작업 영역의 책갈피를 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e59-109">The **Remove-AzSentinelBookmark** cmdlet permanently deletes a Bookmark from a specified workspace.</span></span>
<span data-ttu-id="e8e59-110">파이프라인 연산자를 사용하여 **Bookmark** 개체를 전달하거나 필요한 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8e59-110">You can pass an **Bookmark** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="e8e59-111">Confirm 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8e59-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="e8e59-112">예제</span><span class="sxs-lookup"><span data-stu-id="e8e59-112">EXAMPLES</span></span>

### <span data-ttu-id="e8e59-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="e8e59-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="e8e59-114">이 명령은 작업 영역의 책갈피를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e59-114">This command removes the Bookmark from the workspace.</span></span>

## <span data-ttu-id="e8e59-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8e59-115">PARAMETERS</span></span>

### <span data-ttu-id="e8e59-116">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="e8e59-116">-BookmarkId</span></span>
<span data-ttu-id="e8e59-117">책갈피 ID,</span><span class="sxs-lookup"><span data-stu-id="e8e59-117">Bookmark Id,</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e59-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8e59-118">-DefaultProfile</span></span>
<span data-ttu-id="e8e59-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8e59-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8e59-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8e59-120">-InputObject</span></span>
<span data-ttu-id="e8e59-121">InputObject.</span><span class="sxs-lookup"><span data-stu-id="e8e59-121">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e59-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8e59-122">-PassThru</span></span>
<span data-ttu-id="e8e59-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="e8e59-123">PassThru</span></span>

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

### <span data-ttu-id="e8e59-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8e59-124">-ResourceGroupName</span></span>
<span data-ttu-id="e8e59-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8e59-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e59-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e8e59-126">-WorkspaceName</span></span>
<span data-ttu-id="e8e59-127">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e8e59-127">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e59-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8e59-128">-Confirm</span></span>
<span data-ttu-id="e8e59-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8e59-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8e59-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8e59-130">-WhatIf</span></span>
<span data-ttu-id="e8e59-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e8e59-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8e59-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8e59-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8e59-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8e59-133">CommonParameters</span></span>
<span data-ttu-id="e8e59-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e8e59-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8e59-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e8e59-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8e59-136">입력</span><span class="sxs-lookup"><span data-stu-id="e8e59-136">INPUTS</span></span>

### <span data-ttu-id="e8e59-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e8e59-137">System.String</span></span>
### <span data-ttu-id="e8e59-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="e8e59-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="e8e59-139">출력</span><span class="sxs-lookup"><span data-stu-id="e8e59-139">OUTPUTS</span></span>

### <span data-ttu-id="e8e59-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="e8e59-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="e8e59-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e8e59-141">NOTES</span></span>

## <span data-ttu-id="e8e59-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8e59-142">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
ms.openlocfilehash: ed75d128053a4b08fc7d63a4ef8b02254d868408
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978144"
---
# <span data-ttu-id="3e769-101">Remove-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="3e769-101">Remove-AzSentinelBookmark</span></span>

## <span data-ttu-id="3e769-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e769-102">SYNOPSIS</span></span>
<span data-ttu-id="3e769-103">책갈피를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3e769-103">Delete a Bookmark.</span></span>

## <span data-ttu-id="3e769-104">구문</span><span class="sxs-lookup"><span data-stu-id="3e769-104">SYNTAX</span></span>

### <span data-ttu-id="3e769-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="3e769-105">BookmarkId.</span></span> <span data-ttu-id="3e769-106">(기본값)</span><span class="sxs-lookup"><span data-stu-id="3e769-106">(Default)</span></span>
```
Remove-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e769-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="3e769-107">InputObject</span></span>
```
Remove-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e769-108">설명</span><span class="sxs-lookup"><span data-stu-id="3e769-108">DESCRIPTION</span></span>
<span data-ttu-id="3e769-109">**Remove-AzSentinelBookmark** cmdlet은 지정된 작업 영역의 책갈피를 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3e769-109">The **Remove-AzSentinelBookmark** cmdlet permanently deletes a Bookmark from a specified workspace.</span></span>
<span data-ttu-id="3e769-110">파이프라인 연산자를 사용하여 **Bookmark** 개체를 전달하거나 또는 필요한 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e769-110">You can pass an **Bookmark** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="3e769-111">확인 매개 변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e769-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="3e769-112">예제</span><span class="sxs-lookup"><span data-stu-id="3e769-112">EXAMPLES</span></span>

### <span data-ttu-id="3e769-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="3e769-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="3e769-114">이 명령은 작업 영역에서 책갈피를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3e769-114">This command removes the Bookmark from the workspace.</span></span>

## <span data-ttu-id="3e769-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3e769-115">PARAMETERS</span></span>

### <span data-ttu-id="3e769-116">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="3e769-116">-BookmarkId</span></span>
<span data-ttu-id="3e769-117">책갈피 ID,</span><span class="sxs-lookup"><span data-stu-id="3e769-117">Bookmark Id,</span></span>

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

### <span data-ttu-id="3e769-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e769-118">-DefaultProfile</span></span>
<span data-ttu-id="3e769-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e769-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e769-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e769-120">-InputObject</span></span>
<span data-ttu-id="3e769-121">InputObject.</span><span class="sxs-lookup"><span data-stu-id="3e769-121">InputObject.</span></span>

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

### <span data-ttu-id="3e769-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e769-122">-PassThru</span></span>
<span data-ttu-id="3e769-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="3e769-123">PassThru</span></span>

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

### <span data-ttu-id="3e769-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e769-124">-ResourceGroupName</span></span>
<span data-ttu-id="3e769-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e769-125">Resource group name.</span></span>

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

### <span data-ttu-id="3e769-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3e769-126">-WorkspaceName</span></span>
<span data-ttu-id="3e769-127">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e769-127">Workspace Name.</span></span>

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

### <span data-ttu-id="3e769-128">-확인</span><span class="sxs-lookup"><span data-stu-id="3e769-128">-Confirm</span></span>
<span data-ttu-id="3e769-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3e769-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e769-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e769-130">-WhatIf</span></span>
<span data-ttu-id="3e769-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3e769-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e769-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e769-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e769-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e769-133">CommonParameters</span></span>
<span data-ttu-id="3e769-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3e769-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e769-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e769-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e769-136">입력</span><span class="sxs-lookup"><span data-stu-id="3e769-136">INPUTS</span></span>

### <span data-ttu-id="3e769-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3e769-137">System.String</span></span>
### <span data-ttu-id="3e769-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="3e769-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="3e769-139">출력</span><span class="sxs-lookup"><span data-stu-id="3e769-139">OUTPUTS</span></span>

### <span data-ttu-id="3e769-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="3e769-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="3e769-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3e769-141">NOTES</span></span>

## <span data-ttu-id="3e769-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e769-142">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
ms.openlocfilehash: ebc0ffd78f653276e66b85d263db41803a48c356
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494913"
---
# <span data-ttu-id="bdcb9-101">Update-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="bdcb9-101">Update-AzSentinelBookmark</span></span>

## <span data-ttu-id="bdcb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdcb9-102">SYNOPSIS</span></span>
<span data-ttu-id="bdcb9-103">책갈피를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-103">Update a Bookmark.</span></span>

## <span data-ttu-id="bdcb9-104">구문</span><span class="sxs-lookup"><span data-stu-id="bdcb9-104">SYNTAX</span></span>

### <span data-ttu-id="bdcb9-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-105">BookmarkId.</span></span> <span data-ttu-id="bdcb9-106">(기본값)</span><span class="sxs-lookup"><span data-stu-id="bdcb9-106">(Default)</span></span>
```
Update-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DisplayName <String>] [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] [-Query <String>]
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdcb9-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="bdcb9-107">InputObject</span></span>
```
Update-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdcb9-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdcb9-108">ResourceId</span></span>
```
Update-AzSentinelBookmark -ResourceId <String> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdcb9-109">설명</span><span class="sxs-lookup"><span data-stu-id="bdcb9-109">DESCRIPTION</span></span>
<span data-ttu-id="bdcb9-110">**Update-AzSentinelBookmark** cmdlet은 지정된 작업 영역의 책갈피를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-110">The **Update-AzSentinelBookmark** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="bdcb9-111">**Bookmark** 개체를 매개 변수로 전달하거나 파이프라인 연산자를 사용하여 전달하거나 필요한 *BookmarkId* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-111">You can pass an **Bookmark** object as a parameter or by using the pipeline operator, or alternatively you can specify the required *BookmarkId* parameters.</span></span>
<span data-ttu-id="bdcb9-112">*Confirm* 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="bdcb9-113">예제</span><span class="sxs-lookup"><span data-stu-id="bdcb9-113">EXAMPLES</span></span>

### <span data-ttu-id="bdcb9-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="bdcb9-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId" -Notes "Found something interesting"
```

<span data-ttu-id="bdcb9-115">이 명령은 Notes 속성을 설정하여 책갈피를 *업데이트합니다.*</span><span class="sxs-lookup"><span data-stu-id="bdcb9-115">The command updates the Bookmark by setting the *Notes* property.</span></span>  <span data-ttu-id="bdcb9-116">다른 모든 propreties는 동일하게 유지.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-116">All other propreties stay the same.</span></span>

### <span data-ttu-id="bdcb9-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="bdcb9-117">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId"
PS C:\> $Bookmark | Set-AzSentinelBookmark -Notes "Found something interesting"
```

<span data-ttu-id="bdcb9-118">첫 번째 명령은 지정된 작업 영역의 *BookmarkId로* 책갈피를 읽은 다음 $Bookmark 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-118">The first command gets the Bookmark by *BookmarkId* from the specified workspace, and then stores it in the $Bookmark variable.</span></span>
<span data-ttu-id="bdcb9-119">두 번째 명령은 Notes 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-119">The second command updates the Notes property.</span></span>   <span data-ttu-id="bdcb9-120">다른 모든 propreties는 동일하게 유지.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-120">All other propreties stay the same.</span></span>

## <span data-ttu-id="bdcb9-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdcb9-121">PARAMETERS</span></span>

### <span data-ttu-id="bdcb9-122">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="bdcb9-122">-BookmarkId</span></span>
<span data-ttu-id="bdcb9-123">책갈피 ID,</span><span class="sxs-lookup"><span data-stu-id="bdcb9-123">Bookmark Id,</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId., ParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcb9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdcb9-124">-DefaultProfile</span></span>
<span data-ttu-id="bdcb9-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcb9-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bdcb9-126">-DisplayName</span></span>
<span data-ttu-id="bdcb9-127">책갈피 규칙 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-127">Bookmark Rule Display Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcb9-128">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="bdcb9-128">-IncidentInfo</span></span>
<span data-ttu-id="bdcb9-129">책갈피 인시던트 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-129">Bookmark Incident Info.</span></span>

```yaml
Type: PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdcb9-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdcb9-130">-InputObject</span></span>
<span data-ttu-id="bdcb9-131">InputObject.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-131">InputObject.</span></span>

```yaml
Type: PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdcb9-132">-Label</span><span class="sxs-lookup"><span data-stu-id="bdcb9-132">-Label</span></span>
<span data-ttu-id="bdcb9-133">인시던트 레이블.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-133">Incident Labels.</span></span>

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

### <span data-ttu-id="bdcb9-134">-Notes</span><span class="sxs-lookup"><span data-stu-id="bdcb9-134">-Notes</span></span>
<span data-ttu-id="bdcb9-135">책갈피 노트.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-135">Bookmark Notes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcb9-136">-Query</span><span class="sxs-lookup"><span data-stu-id="bdcb9-136">-Query</span></span>
<span data-ttu-id="bdcb9-137">책갈피 쿼리.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-137">Bookmark Query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcb9-138">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="bdcb9-138">-QueryResult</span></span>
<span data-ttu-id="bdcb9-139">책갈피 쿼리 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-139">Bookmark Query Result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcb9-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdcb9-140">-ResourceGroupName</span></span>
<span data-ttu-id="bdcb9-141">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-141">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcb9-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdcb9-142">-ResourceId</span></span>
<span data-ttu-id="bdcb9-143">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-143">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdcb9-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bdcb9-144">-WorkspaceName</span></span>
<span data-ttu-id="bdcb9-145">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-145">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcb9-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdcb9-146">-Confirm</span></span>
<span data-ttu-id="bdcb9-147">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcb9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdcb9-148">-WhatIf</span></span>
<span data-ttu-id="bdcb9-149">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bdcb9-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdcb9-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcb9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdcb9-151">CommonParameters</span></span>
<span data-ttu-id="bdcb9-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdcb9-153">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bdcb9-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdcb9-154">입력</span><span class="sxs-lookup"><span data-stu-id="bdcb9-154">INPUTS</span></span>

### <span data-ttu-id="bdcb9-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="bdcb9-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

### <span data-ttu-id="bdcb9-156">System.String</span><span class="sxs-lookup"><span data-stu-id="bdcb9-156">System.String</span></span>

### <span data-ttu-id="bdcb9-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="bdcb9-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>

## <span data-ttu-id="bdcb9-158">출력</span><span class="sxs-lookup"><span data-stu-id="bdcb9-158">OUTPUTS</span></span>

### <span data-ttu-id="bdcb9-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="bdcb9-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

## <span data-ttu-id="bdcb9-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bdcb9-160">NOTES</span></span>

## <span data-ttu-id="bdcb9-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bdcb9-161">RELATED LINKS</span></span>

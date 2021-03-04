---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
ms.openlocfilehash: eccb0ce5a9a92eae956c11273bf6397f20473e39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953003"
---
# <span data-ttu-id="54a7d-101">Update-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="54a7d-101">Update-AzSentinelBookmark</span></span>

## <span data-ttu-id="54a7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="54a7d-103">책갈피를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-103">Update a Bookmark.</span></span>

## <span data-ttu-id="54a7d-104">구문</span><span class="sxs-lookup"><span data-stu-id="54a7d-104">SYNTAX</span></span>

### <span data-ttu-id="54a7d-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="54a7d-105">BookmarkId.</span></span> <span data-ttu-id="54a7d-106">(기본값)</span><span class="sxs-lookup"><span data-stu-id="54a7d-106">(Default)</span></span>
```
Update-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DisplayName <String>] [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] [-Query <String>]
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54a7d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="54a7d-107">InputObject</span></span>
```
Update-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54a7d-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="54a7d-108">ResourceId</span></span>
```
Update-AzSentinelBookmark -ResourceId <String> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54a7d-109">설명</span><span class="sxs-lookup"><span data-stu-id="54a7d-109">DESCRIPTION</span></span>
<span data-ttu-id="54a7d-110">**Update-AzSentinelBookmark** cmdlet은 지정된 작업 영역의 책갈피를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-110">The **Update-AzSentinelBookmark** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="54a7d-111">Bookmark 개체를  매개 변수로 전달하거나 파이프라인 연산자를 사용하여 전달하거나 필요한 *BookmarkId* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-111">You can pass an **Bookmark** object as a parameter or by using the pipeline operator, or alternatively you can specify the required *BookmarkId* parameters.</span></span>
<span data-ttu-id="54a7d-112">확인 매개  변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="54a7d-113">예제</span><span class="sxs-lookup"><span data-stu-id="54a7d-113">EXAMPLES</span></span>

### <span data-ttu-id="54a7d-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="54a7d-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId" -Notes "Found something interesting"
```

<span data-ttu-id="54a7d-115">명령은 Notes 속성을 설정하여 *책갈피를 업데이트합니다.*</span><span class="sxs-lookup"><span data-stu-id="54a7d-115">The command updates the Bookmark by setting the *Notes* property.</span></span>  <span data-ttu-id="54a7d-116">다른 모든 프로리타이트는 동일하게 유지된다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-116">All other propreties stay the same.</span></span>

### <span data-ttu-id="54a7d-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="54a7d-117">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId"
PS C:\> $Bookmark | Set-AzSentinelBookmark -Notes "Found something interesting"
```

<span data-ttu-id="54a7d-118">첫 번째 명령은 지정된 작업 영역에서 *BookmarkId by BookmarkId를* 얻은 다음, 이 책갈피를 $Bookmark 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-118">The first command gets the Bookmark by *BookmarkId* from the specified workspace, and then stores it in the $Bookmark variable.</span></span>
<span data-ttu-id="54a7d-119">두 번째 명령은 Notes 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-119">The second command updates the Notes property.</span></span>   <span data-ttu-id="54a7d-120">다른 모든 프로리타이트는 동일하게 유지된다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-120">All other propreties stay the same.</span></span>

## <span data-ttu-id="54a7d-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="54a7d-121">PARAMETERS</span></span>

### <span data-ttu-id="54a7d-122">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="54a7d-122">-BookmarkId</span></span>
<span data-ttu-id="54a7d-123">책갈피 ID,</span><span class="sxs-lookup"><span data-stu-id="54a7d-123">Bookmark Id,</span></span>

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

### <span data-ttu-id="54a7d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54a7d-124">-DefaultProfile</span></span>
<span data-ttu-id="54a7d-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54a7d-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="54a7d-126">-DisplayName</span></span>
<span data-ttu-id="54a7d-127">책갈피 규칙 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-127">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="54a7d-128">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="54a7d-128">-IncidentInfo</span></span>
<span data-ttu-id="54a7d-129">책갈피 인시던트 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-129">Bookmark Incident Info.</span></span>

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

### <span data-ttu-id="54a7d-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54a7d-130">-InputObject</span></span>
<span data-ttu-id="54a7d-131">InputObject.</span><span class="sxs-lookup"><span data-stu-id="54a7d-131">InputObject.</span></span>

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

### <span data-ttu-id="54a7d-132">-Label</span><span class="sxs-lookup"><span data-stu-id="54a7d-132">-Label</span></span>
<span data-ttu-id="54a7d-133">인시던트 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-133">Incident Labels.</span></span>

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

### <span data-ttu-id="54a7d-134">-Notes</span><span class="sxs-lookup"><span data-stu-id="54a7d-134">-Notes</span></span>
<span data-ttu-id="54a7d-135">책갈피 노트.</span><span class="sxs-lookup"><span data-stu-id="54a7d-135">Bookmark Notes.</span></span>

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

### <span data-ttu-id="54a7d-136">-쿼리</span><span class="sxs-lookup"><span data-stu-id="54a7d-136">-Query</span></span>
<span data-ttu-id="54a7d-137">책갈피 쿼리.</span><span class="sxs-lookup"><span data-stu-id="54a7d-137">Bookmark Query.</span></span>

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

### <span data-ttu-id="54a7d-138">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="54a7d-138">-QueryResult</span></span>
<span data-ttu-id="54a7d-139">책갈피 쿼리 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-139">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="54a7d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54a7d-140">-ResourceGroupName</span></span>
<span data-ttu-id="54a7d-141">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-141">Resource group name.</span></span>

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

### <span data-ttu-id="54a7d-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54a7d-142">-ResourceId</span></span>
<span data-ttu-id="54a7d-143">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-143">Resource Id.</span></span>

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

### <span data-ttu-id="54a7d-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="54a7d-144">-WorkspaceName</span></span>
<span data-ttu-id="54a7d-145">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-145">Workspace Name.</span></span>

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

### <span data-ttu-id="54a7d-146">-확인</span><span class="sxs-lookup"><span data-stu-id="54a7d-146">-Confirm</span></span>
<span data-ttu-id="54a7d-147">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54a7d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54a7d-148">-WhatIf</span></span>
<span data-ttu-id="54a7d-149">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54a7d-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54a7d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a7d-151">CommonParameters</span></span>
<span data-ttu-id="54a7d-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="54a7d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a7d-153">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54a7d-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a7d-154">입력</span><span class="sxs-lookup"><span data-stu-id="54a7d-154">INPUTS</span></span>

### <span data-ttu-id="54a7d-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="54a7d-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

### <span data-ttu-id="54a7d-156">System.String</span><span class="sxs-lookup"><span data-stu-id="54a7d-156">System.String</span></span>

### <span data-ttu-id="54a7d-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="54a7d-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>

## <span data-ttu-id="54a7d-158">출력</span><span class="sxs-lookup"><span data-stu-id="54a7d-158">OUTPUTS</span></span>

### <span data-ttu-id="54a7d-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="54a7d-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

## <span data-ttu-id="54a7d-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="54a7d-160">NOTES</span></span>

## <span data-ttu-id="54a7d-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54a7d-161">RELATED LINKS</span></span>

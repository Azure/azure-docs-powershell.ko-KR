---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
ms.openlocfilehash: ebc0ffd78f653276e66b85d263db41803a48c356
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198713"
---
# <span data-ttu-id="9fda3-101">Update-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="9fda3-101">Update-AzSentinelBookmark</span></span>

## <span data-ttu-id="9fda3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fda3-102">SYNOPSIS</span></span>
<span data-ttu-id="9fda3-103">책갈피를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9fda3-103">Update a Bookmark.</span></span>

## <span data-ttu-id="9fda3-104">구문</span><span class="sxs-lookup"><span data-stu-id="9fda3-104">SYNTAX</span></span>

### <span data-ttu-id="9fda3-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="9fda3-105">BookmarkId.</span></span> <span data-ttu-id="9fda3-106">(기본값)</span><span class="sxs-lookup"><span data-stu-id="9fda3-106">(Default)</span></span>
```
Update-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DisplayName <String>] [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] [-Query <String>]
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fda3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9fda3-107">InputObject</span></span>
```
Update-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fda3-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fda3-108">ResourceId</span></span>
```
Update-AzSentinelBookmark -ResourceId <String> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fda3-109">설명</span><span class="sxs-lookup"><span data-stu-id="9fda3-109">DESCRIPTION</span></span>
<span data-ttu-id="9fda3-110">**Update-AzSentinelBookmark** cmdlet은 지정된 작업 영역의 책갈피를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9fda3-110">The **Update-AzSentinelBookmark** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="9fda3-111">**Bookmark** 개체를 매개 변수로 전달하거나 파이프라인 연산자를 사용하여 전달하거나 필요한 *BookmarkId* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9fda3-111">You can pass an **Bookmark** object as a parameter or by using the pipeline operator, or alternatively you can specify the required *BookmarkId* parameters.</span></span>
<span data-ttu-id="9fda3-112">*Confirm* 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9fda3-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="9fda3-113">예제</span><span class="sxs-lookup"><span data-stu-id="9fda3-113">EXAMPLES</span></span>

### <span data-ttu-id="9fda3-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="9fda3-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId" -Notes "Found something interesting"
```

<span data-ttu-id="9fda3-115">이 명령은 Notes 속성을 설정하여 책갈피를 *업데이트합니다.*</span><span class="sxs-lookup"><span data-stu-id="9fda3-115">The command updates the Bookmark by setting the *Notes* property.</span></span>  <span data-ttu-id="9fda3-116">다른 모든 제안은 동일하게 유지.</span><span class="sxs-lookup"><span data-stu-id="9fda3-116">All other propreties stay the same.</span></span>

### <span data-ttu-id="9fda3-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="9fda3-117">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId"
PS C:\> $Bookmark | Set-AzSentinelBookmark -Notes "Found something interesting"
```

<span data-ttu-id="9fda3-118">첫 번째 명령은 지정된 작업 영역의 *BookmarkId로* 책갈피를 읽은 다음 $Bookmark 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9fda3-118">The first command gets the Bookmark by *BookmarkId* from the specified workspace, and then stores it in the $Bookmark variable.</span></span>
<span data-ttu-id="9fda3-119">두 번째 명령은 Notes 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9fda3-119">The second command updates the Notes property.</span></span>   <span data-ttu-id="9fda3-120">다른 모든 제안은 동일하게 유지.</span><span class="sxs-lookup"><span data-stu-id="9fda3-120">All other propreties stay the same.</span></span>

## <span data-ttu-id="9fda3-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fda3-121">PARAMETERS</span></span>

### <span data-ttu-id="9fda3-122">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="9fda3-122">-BookmarkId</span></span>
<span data-ttu-id="9fda3-123">책갈피 ID</span><span class="sxs-lookup"><span data-stu-id="9fda3-123">Bookmark Id,</span></span>

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

### <span data-ttu-id="9fda3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fda3-124">-DefaultProfile</span></span>
<span data-ttu-id="9fda3-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9fda3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fda3-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9fda3-126">-DisplayName</span></span>
<span data-ttu-id="9fda3-127">책갈피 규칙 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9fda3-127">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="9fda3-128">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="9fda3-128">-IncidentInfo</span></span>
<span data-ttu-id="9fda3-129">책갈피 인시던트 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="9fda3-129">Bookmark Incident Info.</span></span>

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

### <span data-ttu-id="9fda3-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fda3-130">-InputObject</span></span>
<span data-ttu-id="9fda3-131">InputObject.</span><span class="sxs-lookup"><span data-stu-id="9fda3-131">InputObject.</span></span>

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

### <span data-ttu-id="9fda3-132">-Label</span><span class="sxs-lookup"><span data-stu-id="9fda3-132">-Label</span></span>
<span data-ttu-id="9fda3-133">인시던트 레이블.</span><span class="sxs-lookup"><span data-stu-id="9fda3-133">Incident Labels.</span></span>

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

### <span data-ttu-id="9fda3-134">-Notes</span><span class="sxs-lookup"><span data-stu-id="9fda3-134">-Notes</span></span>
<span data-ttu-id="9fda3-135">책갈피 노트.</span><span class="sxs-lookup"><span data-stu-id="9fda3-135">Bookmark Notes.</span></span>

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

### <span data-ttu-id="9fda3-136">-Query</span><span class="sxs-lookup"><span data-stu-id="9fda3-136">-Query</span></span>
<span data-ttu-id="9fda3-137">책갈피 쿼리.</span><span class="sxs-lookup"><span data-stu-id="9fda3-137">Bookmark Query.</span></span>

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

### <span data-ttu-id="9fda3-138">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="9fda3-138">-QueryResult</span></span>
<span data-ttu-id="9fda3-139">책갈피 쿼리 결과입니다.</span><span class="sxs-lookup"><span data-stu-id="9fda3-139">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="9fda3-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fda3-140">-ResourceGroupName</span></span>
<span data-ttu-id="9fda3-141">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9fda3-141">Resource group name.</span></span>

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

### <span data-ttu-id="9fda3-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fda3-142">-ResourceId</span></span>
<span data-ttu-id="9fda3-143">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9fda3-143">Resource Id.</span></span>

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

### <span data-ttu-id="9fda3-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9fda3-144">-WorkspaceName</span></span>
<span data-ttu-id="9fda3-145">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9fda3-145">Workspace Name.</span></span>

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

### <span data-ttu-id="9fda3-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fda3-146">-Confirm</span></span>
<span data-ttu-id="9fda3-147">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fda3-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fda3-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fda3-148">-WhatIf</span></span>
<span data-ttu-id="9fda3-149">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9fda3-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fda3-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9fda3-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fda3-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fda3-151">CommonParameters</span></span>
<span data-ttu-id="9fda3-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9fda3-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fda3-153">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9fda3-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fda3-154">입력</span><span class="sxs-lookup"><span data-stu-id="9fda3-154">INPUTS</span></span>

### <span data-ttu-id="9fda3-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="9fda3-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

### <span data-ttu-id="9fda3-156">System.String</span><span class="sxs-lookup"><span data-stu-id="9fda3-156">System.String</span></span>

### <span data-ttu-id="9fda3-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="9fda3-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>

## <span data-ttu-id="9fda3-158">출력</span><span class="sxs-lookup"><span data-stu-id="9fda3-158">OUTPUTS</span></span>

### <span data-ttu-id="9fda3-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="9fda3-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

## <span data-ttu-id="9fda3-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9fda3-160">NOTES</span></span>

## <span data-ttu-id="9fda3-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9fda3-161">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
ms.openlocfilehash: 53dfedcfe4e61deb5064b20134bf063921532aec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494945"
---
# <span data-ttu-id="f304e-101">Get-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="f304e-101">Get-AzSentinelBookmark</span></span>

## <span data-ttu-id="f304e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f304e-102">SYNOPSIS</span></span>
<span data-ttu-id="f304e-103">책갈피를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f304e-103">Get a Bookmark.</span></span>

## <span data-ttu-id="f304e-104">구문</span><span class="sxs-lookup"><span data-stu-id="f304e-104">SYNTAX</span></span>

### <span data-ttu-id="f304e-105">WorkspaceScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="f304e-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f304e-106">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="f304e-106">BookmarkId.</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f304e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f304e-107">ResourceId</span></span>
```
Get-AzSentinelBookmark -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f304e-108">설명</span><span class="sxs-lookup"><span data-stu-id="f304e-108">DESCRIPTION</span></span>
<span data-ttu-id="f304e-109">**Get-AzSentinelBookmark** cmdlet은 지정된 작업 영역의 책갈피를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f304e-109">The **Get-AzSentinelBookmark** cmdlet gets a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="f304e-110">*BookmarkId* 매개 변수를 지정하면 단일 **Bookmark** 개체가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="f304e-110">If you specify the *BookmarkId* parameter, a single **Bookmark** object is returned.</span></span>
<span data-ttu-id="f304e-111">*BookmarkId* 매개 변수를 지정하지 않으면 지정된 작업 영역의 모든 책갈피를 포함하는 배열이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="f304e-111">If you do not specify the *BookmarkId* parameter, an array containing all of the Bookmarks in the specified workspace are returned.</span></span>
<span data-ttu-id="f304e-112">책갈피 **개체를** 사용하여 책갈피를 업데이트할 수 있습니다. 예를 들어 책갈피 노트를 추가할 **수 있습니다.**</span><span class="sxs-lookup"><span data-stu-id="f304e-112">You can use the **Bookmark** object to update the Bookmark, for example you can add Notes the **Bookmark**.</span></span>

## <span data-ttu-id="f304e-113">예제</span><span class="sxs-lookup"><span data-stu-id="f304e-113">EXAMPLES</span></span>

### <span data-ttu-id="f304e-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="f304e-114">Example 1</span></span>
```powershell
PS C:\> $Bookmarks = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="f304e-115">이 예제에서는 지정된  작업 영역의 책갈피를 모두 읽은 다음 해당 책갈피를 $Bookmarks 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f304e-115">This example gets all of the **Bookmarks** in the specified workspace, and then stores it in the $Bookmarks variable.</span></span>

### <span data-ttu-id="f304e-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="f304e-116">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="f304e-117">이 예제에서는  지정된 작업 영역의 책갈피를 읽은 다음, $Bookmark 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f304e-117">This example gets an **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="f304e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f304e-118">PARAMETERS</span></span>

### <span data-ttu-id="f304e-119">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="f304e-119">-BookmarkId</span></span>
<span data-ttu-id="f304e-120">책갈피 ID,</span><span class="sxs-lookup"><span data-stu-id="f304e-120">Bookmark Id,</span></span>

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

### <span data-ttu-id="f304e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f304e-121">-DefaultProfile</span></span>
<span data-ttu-id="f304e-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f304e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f304e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f304e-123">-ResourceGroupName</span></span>
<span data-ttu-id="f304e-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f304e-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f304e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f304e-125">-ResourceId</span></span>
<span data-ttu-id="f304e-126">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f304e-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f304e-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f304e-127">-WorkspaceName</span></span>
<span data-ttu-id="f304e-128">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f304e-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f304e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f304e-129">CommonParameters</span></span>
<span data-ttu-id="f304e-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f304e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f304e-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f304e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f304e-132">입력</span><span class="sxs-lookup"><span data-stu-id="f304e-132">INPUTS</span></span>

### <span data-ttu-id="f304e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f304e-133">System.String</span></span>
## <span data-ttu-id="f304e-134">출력</span><span class="sxs-lookup"><span data-stu-id="f304e-134">OUTPUTS</span></span>

### <span data-ttu-id="f304e-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="f304e-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="f304e-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f304e-136">NOTES</span></span>

## <span data-ttu-id="f304e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f304e-137">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
ms.openlocfilehash: d33c126da2a77736871a9ec1f950382168f52bee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178596"
---
# <span data-ttu-id="9cdf2-101">Get-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="9cdf2-101">Get-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="9cdf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cdf2-102">SYNOPSIS</span></span>
<span data-ttu-id="9cdf2-103">인시던트 주석을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9cdf2-103">Get an Incident Comment.</span></span>

## <span data-ttu-id="9cdf2-104">구문</span><span class="sxs-lookup"><span data-stu-id="9cdf2-104">SYNTAX</span></span>

### <span data-ttu-id="9cdf2-105">IncidentId(기본값)</span><span class="sxs-lookup"><span data-stu-id="9cdf2-105">IncidentId (Default)</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cdf2-106">IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="9cdf2-106">IncidentCommentId</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 -IncidentCommentId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cdf2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cdf2-107">ResourceId</span></span>
```
Get-AzSentinelIncidentComment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cdf2-108">설명</span><span class="sxs-lookup"><span data-stu-id="9cdf2-108">DESCRIPTION</span></span>
<span data-ttu-id="9cdf2-109">**Get-AzSentinelIncidentComment** cmdlet은 지정된 작업 영역의 인시던트 주석을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9cdf2-109">The **Get-AzSentinelIncidentComment** cmdlet gets a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="9cdf2-110">*IncidentCommentId* 및 *IncidentId* 매개 변수를 지정하면 단일 **IncidentComment** 개체가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="9cdf2-110">If you specify the *IncidentCommentId* and *IncidentId* parameters, a single **IncidentComment** object is returned.</span></span>
<span data-ttu-id="9cdf2-111">*IncidentCommentId* 매개 변수를 지정하지 않으면 지정된 작업 영역의 지정된 인시던트에 대한 모든 인시던트 주석이 포함된 배열이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="9cdf2-111">If you do not specify the *IncidentCommentId* parameter, an array containing all of the Incident Comments for the specified Incident in the specified workspace are returned.</span></span>

## <span data-ttu-id="9cdf2-112">예제</span><span class="sxs-lookup"><span data-stu-id="9cdf2-112">EXAMPLES</span></span>

### <span data-ttu-id="9cdf2-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="9cdf2-113">Example 1</span></span>
```powershell
PS C:\> $IncidentComments = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="9cdf2-114">이 예제에서는 지정된 작업 영역의 지정된 인시던트에 대한 **IncidentComments를** 모두 인시던트에 저장한 다음, $IncidentComments 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9cdf2-114">This example gets all of the **IncidentComments** for the specified Incident in the specified workspace, and then stores it in the $IncidentComments variable.</span></span>

### <span data-ttu-id="9cdf2-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="9cdf2-115">Example 2</span></span>
```powershell
PS C:\> $IncidentComment = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -IncidentCommentId "MyIncidentCommentId"
```

<span data-ttu-id="9cdf2-116">이 예제에서는 지정된 작업 영역의 지정된 인시던트에 대한 **IncidentComment를** 인시던트와 함께 $IncidentComment 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9cdf2-116">This example gets an **IncidentComment** for the specified Incident in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="9cdf2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cdf2-117">PARAMETERS</span></span>

### <span data-ttu-id="9cdf2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cdf2-118">-DefaultProfile</span></span>
<span data-ttu-id="9cdf2-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9cdf2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cdf2-120">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="9cdf2-120">-IncidentCommentId</span></span>
<span data-ttu-id="9cdf2-121">인시던트 주석 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9cdf2-121">Incident Comment Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cdf2-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="9cdf2-122">-IncidentId</span></span>
<span data-ttu-id="9cdf2-123">인시던트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9cdf2-123">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cdf2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cdf2-124">-ResourceGroupName</span></span>
<span data-ttu-id="9cdf2-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9cdf2-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cdf2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cdf2-126">-ResourceId</span></span>
<span data-ttu-id="9cdf2-127">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9cdf2-127">Resource Id.</span></span>

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

### <span data-ttu-id="9cdf2-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9cdf2-128">-WorkspaceName</span></span>
<span data-ttu-id="9cdf2-129">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9cdf2-129">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cdf2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cdf2-130">CommonParameters</span></span>
<span data-ttu-id="9cdf2-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9cdf2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cdf2-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9cdf2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cdf2-133">입력</span><span class="sxs-lookup"><span data-stu-id="9cdf2-133">INPUTS</span></span>

### <span data-ttu-id="9cdf2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9cdf2-134">System.String</span></span>
## <span data-ttu-id="9cdf2-135">출력</span><span class="sxs-lookup"><span data-stu-id="9cdf2-135">OUTPUTS</span></span>

### <span data-ttu-id="9cdf2-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="9cdf2-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="9cdf2-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9cdf2-137">NOTES</span></span>

## <span data-ttu-id="9cdf2-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9cdf2-138">RELATED LINKS</span></span>

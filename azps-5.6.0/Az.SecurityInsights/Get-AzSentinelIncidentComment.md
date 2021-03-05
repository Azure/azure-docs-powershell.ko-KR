---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
ms.openlocfilehash: b25e99766c4dc0433b14810352968300fd5bd129
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986407"
---
# <span data-ttu-id="5ea99-101">Get-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="5ea99-101">Get-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="5ea99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ea99-102">SYNOPSIS</span></span>
<span data-ttu-id="5ea99-103">인시던트 설명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5ea99-103">Get an Incident Comment.</span></span>

## <span data-ttu-id="5ea99-104">구문</span><span class="sxs-lookup"><span data-stu-id="5ea99-104">SYNTAX</span></span>

### <span data-ttu-id="5ea99-105">incidentId(기본값)</span><span class="sxs-lookup"><span data-stu-id="5ea99-105">IncidentId (Default)</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ea99-106">IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="5ea99-106">IncidentCommentId</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 -IncidentCommentId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ea99-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ea99-107">ResourceId</span></span>
```
Get-AzSentinelIncidentComment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ea99-108">설명</span><span class="sxs-lookup"><span data-stu-id="5ea99-108">DESCRIPTION</span></span>
<span data-ttu-id="5ea99-109">**Get-AzSentinelIncidentComment** cmdlet은 지정된 작업 영역에서 인시던트 주석을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5ea99-109">The **Get-AzSentinelIncidentComment** cmdlet gets a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="5ea99-110">*IncidentCommentId* 및 *IncidentId* 매개 변수를 지정하면 **단일 IncidentComment** 개체가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ea99-110">If you specify the *IncidentCommentId* and *IncidentId* parameters, a single **IncidentComment** object is returned.</span></span>
<span data-ttu-id="5ea99-111">*IncidentCommentId* 매개 변수를 지정하지 않으면 지정된 작업 영역의 지정된 인시던트에 대한 모든 인시던트 주석을 포함하는 배열이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ea99-111">If you do not specify the *IncidentCommentId* parameter, an array containing all of the Incident Comments for the specified Incident in the specified workspace are returned.</span></span>

## <span data-ttu-id="5ea99-112">예제</span><span class="sxs-lookup"><span data-stu-id="5ea99-112">EXAMPLES</span></span>

### <span data-ttu-id="5ea99-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="5ea99-113">Example 1</span></span>
```powershell
PS C:\> $IncidentComments = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="5ea99-114">이 예제에서는 지정된 작업 영역의 지정된 인시던트에 대한 **모든 IncidentComments를** 한 다음, 해당 인시던트 $IncidentComments 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5ea99-114">This example gets all of the **IncidentComments** for the specified Incident in the specified workspace, and then stores it in the $IncidentComments variable.</span></span>

### <span data-ttu-id="5ea99-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="5ea99-115">Example 2</span></span>
```powershell
PS C:\> $IncidentComment = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -IncidentCommentId "MyIncidentCommentId"
```

<span data-ttu-id="5ea99-116">이 예제에서는 지정된 작업 영역의 지정된 인시던트에 대한 **IncidentComment을** 다음, 해당 인시던트 변수에 $IncidentComment 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5ea99-116">This example gets an **IncidentComment** for the specified Incident in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="5ea99-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5ea99-117">PARAMETERS</span></span>

### <span data-ttu-id="5ea99-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ea99-118">-DefaultProfile</span></span>
<span data-ttu-id="5ea99-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ea99-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ea99-120">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="5ea99-120">-IncidentCommentId</span></span>
<span data-ttu-id="5ea99-121">인시던트 주석 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5ea99-121">Incident Comment Id.</span></span>

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

### <span data-ttu-id="5ea99-122">-incidentId</span><span class="sxs-lookup"><span data-stu-id="5ea99-122">-IncidentId</span></span>
<span data-ttu-id="5ea99-123">인시던트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5ea99-123">Incident Id.</span></span>

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

### <span data-ttu-id="5ea99-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ea99-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ea99-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ea99-125">Resource group name.</span></span>

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

### <span data-ttu-id="5ea99-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ea99-126">-ResourceId</span></span>
<span data-ttu-id="5ea99-127">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5ea99-127">Resource Id.</span></span>

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

### <span data-ttu-id="5ea99-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5ea99-128">-WorkspaceName</span></span>
<span data-ttu-id="5ea99-129">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ea99-129">Workspace Name.</span></span>

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

### <span data-ttu-id="5ea99-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ea99-130">CommonParameters</span></span>
<span data-ttu-id="5ea99-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5ea99-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ea99-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ea99-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ea99-133">입력</span><span class="sxs-lookup"><span data-stu-id="5ea99-133">INPUTS</span></span>

### <span data-ttu-id="5ea99-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5ea99-134">System.String</span></span>
## <span data-ttu-id="5ea99-135">출력</span><span class="sxs-lookup"><span data-stu-id="5ea99-135">OUTPUTS</span></span>

### <span data-ttu-id="5ea99-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="5ea99-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="5ea99-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5ea99-137">NOTES</span></span>

## <span data-ttu-id="5ea99-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ea99-138">RELATED LINKS</span></span>

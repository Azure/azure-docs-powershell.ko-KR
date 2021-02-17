---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 6e60f4ed93dd3963fa748db250cacfcf0aeecce3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191217"
---
# <span data-ttu-id="2b505-101">Get-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="2b505-101">Get-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="2b505-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b505-102">SYNOPSIS</span></span>
<span data-ttu-id="2b505-103">자동화된 응답(경고 규칙 작업)을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2b505-103">Get an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="2b505-104">구문</span><span class="sxs-lookup"><span data-stu-id="2b505-104">SYNTAX</span></span>

### <span data-ttu-id="2b505-105">AlertRuleId(기본값)</span><span class="sxs-lookup"><span data-stu-id="2b505-105">AlertRuleId (Default)</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b505-106">ActionId</span><span class="sxs-lookup"><span data-stu-id="2b505-106">ActionId</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b505-107">설명</span><span class="sxs-lookup"><span data-stu-id="2b505-107">DESCRIPTION</span></span>
<span data-ttu-id="2b505-108">**Get-AzSentinelAlertRuleAction** cmdlet은 지정된 작업 영역에서 자동화된 응답(경고 규칙 작업)을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2b505-108">The **Get-AzSentinelAlertRuleAction** cmdlet gets an Automated Response (Alert Rule Action) from the specified workspace.</span></span>
<span data-ttu-id="2b505-109">*ActionId* 및 *AlertRuleId* 매개 변수를 지정하면 단일 **AlertRuleAction 개체가** 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b505-109">If you specify the *ActionId* and *AlertRuleId* parameters, a single **AlertRuleAction** object is returned.</span></span>
<span data-ttu-id="2b505-110">*ActionId* 매개 변수를 지정하지 않으면 지정된 작업 영역의 특정 경고 규칙에 대한 모든 작업을 포함하는 배열이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b505-110">If you do not specify the *ActionId* parameter, an array containing all of the Actions for the specificed Alert Rule in the specified workspace are returned.</span></span>
<span data-ttu-id="2b505-111">작업 개체를  사용하여 작업을 업데이트할 수 있습니다. 예를 들어 경고 규칙에 대한 **작업을** 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b505-111">You can use the **Action** object to update the Action, for example you can change the the **Action** for an Alert Rule.</span></span>

## <span data-ttu-id="2b505-112">예제</span><span class="sxs-lookup"><span data-stu-id="2b505-112">EXAMPLES</span></span>

### <span data-ttu-id="2b505-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b505-113">Example 1</span></span>
```powershell
PS C:\> $AlertRuleActions = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="2b505-114">이 예제에서는 지정된  작업 영역의 지정된 경고 규칙에 대한 모든 작업을 수행한 다음, $AlertRuleActions 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2b505-114">This example gets all of the **Actions** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleActions variable.</span></span>

### <span data-ttu-id="2b505-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="2b505-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="2b505-116">이 예제에서는 지정된 작업 영역의 지정된 경고 규칙에 대한 **AlertRuleAction을** 구한 다음 $AlertRuleAction 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="2b505-116">This example gets an **AlertRuleAction** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="2b505-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b505-117">PARAMETERS</span></span>

### <span data-ttu-id="2b505-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="2b505-118">-ActionId</span></span>
<span data-ttu-id="2b505-119">작업 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2b505-119">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b505-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="2b505-120">-AlertRuleId</span></span>
<span data-ttu-id="2b505-121">경고 규칙 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2b505-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="2b505-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b505-122">-DefaultProfile</span></span>
<span data-ttu-id="2b505-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b505-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b505-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b505-124">-ResourceGroupName</span></span>
<span data-ttu-id="2b505-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b505-125">Resource group name.</span></span>

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

### <span data-ttu-id="2b505-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2b505-126">-WorkspaceName</span></span>
<span data-ttu-id="2b505-127">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b505-127">Workspace Name.</span></span>

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

### <span data-ttu-id="2b505-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b505-128">CommonParameters</span></span>
<span data-ttu-id="2b505-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2b505-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b505-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2b505-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b505-131">입력</span><span class="sxs-lookup"><span data-stu-id="2b505-131">INPUTS</span></span>

### <span data-ttu-id="2b505-132">없음</span><span class="sxs-lookup"><span data-stu-id="2b505-132">None</span></span>
## <span data-ttu-id="2b505-133">출력</span><span class="sxs-lookup"><span data-stu-id="2b505-133">OUTPUTS</span></span>

### <span data-ttu-id="2b505-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="2b505-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="2b505-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2b505-135">NOTES</span></span>

## <span data-ttu-id="2b505-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b505-136">RELATED LINKS</span></span>

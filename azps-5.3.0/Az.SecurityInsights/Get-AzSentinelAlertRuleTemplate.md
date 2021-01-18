---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruletemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
ms.openlocfilehash: aa5dabced1439d8a754e220d56f7309c7b2df3e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494946"
---
# <span data-ttu-id="11e29-101">Get-AzSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="11e29-101">Get-AzSentinelAlertRuleTemplate</span></span>

## <span data-ttu-id="11e29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11e29-102">SYNOPSIS</span></span>
<span data-ttu-id="11e29-103">분석 규칙 템플릿을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="11e29-103">Get Analytic Rule Template.</span></span>

## <span data-ttu-id="11e29-104">구문</span><span class="sxs-lookup"><span data-stu-id="11e29-104">SYNTAX</span></span>

### <span data-ttu-id="11e29-105">WorkspaceScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="11e29-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11e29-106">AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="11e29-106">AlertRuleTemplateId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 -AlertRuleTemplateId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11e29-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="11e29-107">ResourceId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11e29-108">설명</span><span class="sxs-lookup"><span data-stu-id="11e29-108">DESCRIPTION</span></span>
<span data-ttu-id="11e29-109">**Get-AzSentinelAlertRuleTemplate** cmdlet은 지정된 작업 영역의 경고 규칙 템플릿을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="11e29-109">The **Get-AzSentinelAlertRuleTemplate** cmdlet gets an Alert Rule Template from the specified workspace.</span></span>
<span data-ttu-id="11e29-110">*AlertRuleTemplateId* 매개 변수를 지정하면 단일 **AlertRuleTemplate** 개체가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="11e29-110">If you specify the *AlertRuleTemplateId* parameter, a single **AlertRuleTemplate** object is returned.</span></span>
<span data-ttu-id="11e29-111">*AlertRuleTemplateId* 매개 변수를 지정하지 않으면 지정된 작업 영역의 모든 경고 규칙 템플릿을 포함하는 배열이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="11e29-111">If you do not specify the *AlertRuleTemplateId* parameter, an array containing all of the Alert Rule Templates in the specified workspace are returned.</span></span>
<span data-ttu-id="11e29-112">**AlertRuleTemplate** 개체를 사용하여 새 경고 규칙을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11e29-112">You can use the **AlertRuleTemplate** object to create a new Alert Rule.</span></span>

## <span data-ttu-id="11e29-113">예제</span><span class="sxs-lookup"><span data-stu-id="11e29-113">EXAMPLES</span></span>

### <span data-ttu-id="11e29-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="11e29-114">Example 1</span></span>
```powershell
PS C:\> $AlertRuleTemplates = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="11e29-115">이 예제에서는 지정된 작업 영역의 **AlertRuleTemplates를** 모두 표시한 다음, $AlertRuleTemplates 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="11e29-115">This example gets all of the **AlertRuleTemplates** in the specified workspace, and then stores it in the $AlertRuleTemplates variable.</span></span>

### <span data-ttu-id="11e29-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="11e29-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplate = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleTemplateId "MyAlertRuleTemplateId"
```

<span data-ttu-id="11e29-117">이 예제에서는 지정된 작업 영역의 **AlertRuleTemplate을** 얻은 다음, 경고 변수에 $AlertRuleTemplate 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="11e29-117">This example gets an **AlertRuleTemplate** in the specified workspace, and then stores it in the $AlertRuleTemplate variable.</span></span>

## <span data-ttu-id="11e29-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11e29-118">PARAMETERS</span></span>

### <span data-ttu-id="11e29-119">-AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="11e29-119">-AlertRuleTemplateId</span></span>
<span data-ttu-id="11e29-120">템플릿 경고 규칙 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="11e29-120">Template Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11e29-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11e29-121">-DefaultProfile</span></span>
<span data-ttu-id="11e29-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11e29-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11e29-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11e29-123">-ResourceGroupName</span></span>
<span data-ttu-id="11e29-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11e29-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e29-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11e29-125">-ResourceId</span></span>
<span data-ttu-id="11e29-126">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="11e29-126">Resource Id.</span></span>

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

### <span data-ttu-id="11e29-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="11e29-127">-WorkspaceName</span></span>
<span data-ttu-id="11e29-128">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11e29-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11e29-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11e29-129">CommonParameters</span></span>
<span data-ttu-id="11e29-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="11e29-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11e29-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="11e29-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11e29-132">입력</span><span class="sxs-lookup"><span data-stu-id="11e29-132">INPUTS</span></span>

### <span data-ttu-id="11e29-133">System.String</span><span class="sxs-lookup"><span data-stu-id="11e29-133">System.String</span></span>
## <span data-ttu-id="11e29-134">출력</span><span class="sxs-lookup"><span data-stu-id="11e29-134">OUTPUTS</span></span>

### <span data-ttu-id="11e29-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="11e29-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span></span>
## <span data-ttu-id="11e29-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="11e29-136">NOTES</span></span>

## <span data-ttu-id="11e29-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11e29-137">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
ms.openlocfilehash: 02dc3b58d9cd4b4be58b83f36cc6e42e11008812
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197889"
---
# <span data-ttu-id="fbd5f-101">Get-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="fbd5f-101">Get-AzSentinelAlertRule</span></span>

## <span data-ttu-id="fbd5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbd5f-102">SYNOPSIS</span></span>
<span data-ttu-id="fbd5f-103">분석(경고 규칙)을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fbd5f-103">Gets an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="fbd5f-104">구문</span><span class="sxs-lookup"><span data-stu-id="fbd5f-104">SYNTAX</span></span>

### <span data-ttu-id="fbd5f-105">WorkspaceScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="fbd5f-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbd5f-106">AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="fbd5f-106">AlertRuleId</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbd5f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbd5f-107">ResourceId</span></span>
```
Get-AzSentinelAlertRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbd5f-108">설명</span><span class="sxs-lookup"><span data-stu-id="fbd5f-108">DESCRIPTION</span></span>
<span data-ttu-id="fbd5f-109">**Get-AzSentinelAlertRule** cmdlet은 지정된 작업 영역에서 분석(경고 규칙)을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fbd5f-109">The **Get-AzSentinelAlertRule** cmdlet gets an Analytic (Alert Rule) from the specified workspace.</span></span>
<span data-ttu-id="fbd5f-110">*AlertRuleId* 매개 변수를 지정하면 단일 **AlertRule** 개체가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbd5f-110">If you specify the *AlertRuleId* parameter, a single **AlertRule** object is returned.</span></span>
<span data-ttu-id="fbd5f-111">*AlertRuleId* 매개 변수를 지정하지 않으면 지정된 작업 영역의 모든 경고 규칙을 포함하는 배열이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="fbd5f-111">If you do not specify the *AlertRuleId* parameter, an array containing all of the Alert Rules in the specified workspace are returned.</span></span>
<span data-ttu-id="fbd5f-112">**AlertRule** 개체를 사용하여 AlertRule을 업데이트할 수 있습니다. 예를 들어 **AlertRule을** 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbd5f-112">You can use the **AlertRule** object to update the AlertRule, for example you can disable the **AlertRule**.</span></span>

## <span data-ttu-id="fbd5f-113">예제</span><span class="sxs-lookup"><span data-stu-id="fbd5f-113">EXAMPLES</span></span>

### <span data-ttu-id="fbd5f-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="fbd5f-114">Example 1</span></span>
```powershell
PS C:\> $AlertRules = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="fbd5f-115">이 예제에서는 지정된 작업 영역의 **AlertRules를** 모두 인용한 다음, $AlertRules 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd5f-115">This example gets all of the **AlertRules** in the specified workspace, and then stores it in the $AlertRules variable.</span></span>

### <span data-ttu-id="fbd5f-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="fbd5f-116">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="fbd5f-117">이 예제에서는 지정된 작업 영역의 **AlertRule을** 구한 다음, 경고 변수에 $AlertRule 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd5f-117">This example gets an **AlertRule** in the specified workspace, and then stores it in the $AlertRule variable.</span></span>

## <span data-ttu-id="fbd5f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbd5f-118">PARAMETERS</span></span>

### <span data-ttu-id="fbd5f-119">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="fbd5f-119">-AlertRuleId</span></span>
<span data-ttu-id="fbd5f-120">경고 규칙 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fbd5f-120">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbd5f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbd5f-121">-DefaultProfile</span></span>
<span data-ttu-id="fbd5f-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fbd5f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbd5f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbd5f-123">-ResourceGroupName</span></span>
<span data-ttu-id="fbd5f-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbd5f-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd5f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbd5f-125">-ResourceId</span></span>
<span data-ttu-id="fbd5f-126">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fbd5f-126">Resource Id.</span></span>

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

### <span data-ttu-id="fbd5f-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fbd5f-127">-WorkspaceName</span></span>
<span data-ttu-id="fbd5f-128">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbd5f-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbd5f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbd5f-129">CommonParameters</span></span>
<span data-ttu-id="fbd5f-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fbd5f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbd5f-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fbd5f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbd5f-132">입력</span><span class="sxs-lookup"><span data-stu-id="fbd5f-132">INPUTS</span></span>

### <span data-ttu-id="fbd5f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="fbd5f-133">System.String</span></span>
## <span data-ttu-id="fbd5f-134">출력</span><span class="sxs-lookup"><span data-stu-id="fbd5f-134">OUTPUTS</span></span>

### <span data-ttu-id="fbd5f-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="fbd5f-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="fbd5f-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fbd5f-136">NOTES</span></span>

## <span data-ttu-id="fbd5f-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fbd5f-137">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: e1eb623fcb4b77dda95fe3f849c86e20ad5d1601
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034670"
---
# <span data-ttu-id="6e939-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="6e939-101">Get-AzActionRule</span></span>

## <span data-ttu-id="6e939-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e939-102">SYNOPSIS</span></span>
<span data-ttu-id="6e939-103">작업 규칙 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="6e939-103">Get Action Rules Information</span></span>

## <span data-ttu-id="6e939-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e939-104">SYNTAX</span></span>

### <span data-ttu-id="6e939-105">ListActionRules (기본값)</span><span class="sxs-lookup"><span data-stu-id="6e939-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e939-106">리소스</span><span class="sxs-lookup"><span data-stu-id="6e939-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e939-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="6e939-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e939-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6e939-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e939-109">설명은</span><span class="sxs-lookup"><span data-stu-id="6e939-109">DESCRIPTION</span></span>
<span data-ttu-id="6e939-110">**AzActionRule cmdlet은** 구성 된 작업 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e939-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="6e939-111">예제의</span><span class="sxs-lookup"><span data-stu-id="6e939-111">EXAMPLES</span></span>

### <span data-ttu-id="6e939-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="6e939-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="6e939-113">Sev2 심각도 및 플랫폼 모니터 서비스에 대해 필터링 된 리소스 그룹 테스트-rg에서 구성한 모든 작업 규칙을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e939-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="6e939-114">Format-List를 사용 하 여 목록의 각 작업 규칙에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e939-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="6e939-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="6e939-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="6e939-116">테스트 rg 리소스 그룹의 이름 테스트-작업 규칙을 사용 하 여 작업 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e939-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="6e939-117">변수</span><span class="sxs-lookup"><span data-stu-id="6e939-117">PARAMETERS</span></span>

### <span data-ttu-id="6e939-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="6e939-118">-ActionGroup</span></span>
<span data-ttu-id="6e939-119">작업 그룹</span><span class="sxs-lookup"><span data-stu-id="6e939-119">Action group</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e939-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="6e939-120">-AlertRuleId</span></span>
<span data-ttu-id="6e939-121">경고 규칙 Id에 대 한 필터</span><span class="sxs-lookup"><span data-stu-id="6e939-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e939-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e939-122">-DefaultProfile</span></span>
<span data-ttu-id="6e939-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e939-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e939-124">-설명</span><span class="sxs-lookup"><span data-stu-id="6e939-124">-Description</span></span>
<span data-ttu-id="6e939-125">스마트 그룹 Id를 갖는 모든 경고 필터링</span><span class="sxs-lookup"><span data-stu-id="6e939-125">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e939-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="6e939-126">-ImpactedScope</span></span>
<span data-ttu-id="6e939-127">영향을 받는 범위에 대해 필터링</span><span class="sxs-lookup"><span data-stu-id="6e939-127">Filter on Impacted scope</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e939-128">-모니터 서비스</span><span class="sxs-lookup"><span data-stu-id="6e939-128">-MonitorService</span></span>
<span data-ttu-id="6e939-129">Moniter 서비스에 대 한 필터링</span><span class="sxs-lookup"><span data-stu-id="6e939-129">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e939-130">-이름</span><span class="sxs-lookup"><span data-stu-id="6e939-130">-Name</span></span>
<span data-ttu-id="6e939-131">작업 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e939-131">Name of action rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e939-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e939-132">-ResourceGroupName</span></span>
<span data-ttu-id="6e939-133">작업 규칙이 있는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e939-133">Resource Group Name in which action rule resides.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e939-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e939-134">-ResourceId</span></span>
<span data-ttu-id="6e939-135">Resoure id를 기준으로 작업 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e939-135">Get Action rule by resoure id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e939-136">-심각도</span><span class="sxs-lookup"><span data-stu-id="6e939-136">-Severity</span></span>
<span data-ttu-id="6e939-137">알림의 심각도에 대 한 필터링</span><span class="sxs-lookup"><span data-stu-id="6e939-137">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e939-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6e939-138">-TargetResourceGroup</span></span>
<span data-ttu-id="6e939-139">경고 대상 리소스의 리소스 그룹 이름에 대 한 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="6e939-139">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e939-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6e939-140">-TargetResourceId</span></span>
<span data-ttu-id="6e939-141">경고 대상 리소스의 리소스 Id에 대 한 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="6e939-141">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e939-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="6e939-142">-TargetResourceType</span></span>
<span data-ttu-id="6e939-143">경고 대상 리소스의 리소스 종류에 대 한 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="6e939-143">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e939-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e939-144">CommonParameters</span></span>
<span data-ttu-id="6e939-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e939-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e939-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e939-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e939-147">입력</span><span class="sxs-lookup"><span data-stu-id="6e939-147">INPUTS</span></span>

### <span data-ttu-id="6e939-148">않아야</span><span class="sxs-lookup"><span data-stu-id="6e939-148">None</span></span>

## <span data-ttu-id="6e939-149">출력</span><span class="sxs-lookup"><span data-stu-id="6e939-149">OUTPUTS</span></span>

### <span data-ttu-id="6e939-150">AlertsManagement 모델. a PSActionRule</span><span class="sxs-lookup"><span data-stu-id="6e939-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="6e939-151">상속자</span><span class="sxs-lookup"><span data-stu-id="6e939-151">NOTES</span></span>

## <span data-ttu-id="6e939-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e939-152">RELATED LINKS</span></span>

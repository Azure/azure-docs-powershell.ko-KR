---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
ms.openlocfilehash: 86559299a4711d95e1b5c94c455bdbb841e141e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870437"
---
# <span data-ttu-id="c2d07-101">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c2d07-101">Get-AzScheduledQueryRule</span></span>

## <span data-ttu-id="c2d07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2d07-102">SYNOPSIS</span></span>
<span data-ttu-id="c2d07-103">예약 된 쿼리 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2d07-103">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="c2d07-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2d07-104">SYNTAX</span></span>

### <span data-ttu-id="c2d07-105">BySubscriptionOrResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="c2d07-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzScheduledQueryRule [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2d07-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="c2d07-106">ByRuleName</span></span>
```
Get-AzScheduledQueryRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2d07-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2d07-107">ByResourceId</span></span>
```
Get-AzScheduledQueryRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2d07-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c2d07-108">DESCRIPTION</span></span>
<span data-ttu-id="c2d07-109">예약 된 쿼리 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c2d07-109">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="c2d07-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c2d07-110">EXAMPLES</span></span>

### <span data-ttu-id="c2d07-111">예제 1-구독 또는 리소스 그룹별 목록 표시</span><span class="sxs-lookup"><span data-stu-id="c2d07-111">Example 1 - List by subscription or resource group</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup"

Description       : description 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}

Description       : description 2
Enabled           : true
LastUpdatedTime   : 15-Apr-19 6:57:00 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.Action
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule2
Name              : LogAlertRule2
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="c2d07-112">예제 2-규칙 이름으로 가져오기</span><span class="sxs-lookup"><span data-stu-id="c2d07-112">Example 2 - Get by rule name</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="c2d07-113">예제 3-리소스 Id로 가져오기</span><span class="sxs-lookup"><span data-stu-id="c2d07-113">Example 3 - Get by resource Id</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="c2d07-114">변수</span><span class="sxs-lookup"><span data-stu-id="c2d07-114">PARAMETERS</span></span>

### <span data-ttu-id="c2d07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2d07-115">-DefaultProfile</span></span>
<span data-ttu-id="c2d07-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2d07-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2d07-117">-이름</span><span class="sxs-lookup"><span data-stu-id="c2d07-117">-Name</span></span>
<span data-ttu-id="c2d07-118">경고 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="c2d07-118">The alert rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2d07-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2d07-119">-ResourceGroupName</span></span>
<span data-ttu-id="c2d07-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c2d07-120">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2d07-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2d07-121">-ResourceId</span></span>
<span data-ttu-id="c2d07-122">리소스 Id</span><span class="sxs-lookup"><span data-stu-id="c2d07-122">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2d07-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2d07-123">CommonParameters</span></span>
<span data-ttu-id="c2d07-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d07-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2d07-125">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c2d07-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2d07-126">입력</span><span class="sxs-lookup"><span data-stu-id="c2d07-126">INPUTS</span></span>

### <span data-ttu-id="c2d07-127">않아야</span><span class="sxs-lookup"><span data-stu-id="c2d07-127">None</span></span>

## <span data-ttu-id="c2d07-128">출력</span><span class="sxs-lookup"><span data-stu-id="c2d07-128">OUTPUTS</span></span>

### <span data-ttu-id="c2d07-129">PSScheduledQueryRuleResource를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2d07-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="c2d07-130">상속자</span><span class="sxs-lookup"><span data-stu-id="c2d07-130">NOTES</span></span>

## <span data-ttu-id="c2d07-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2d07-131">RELATED LINKS</span></span>

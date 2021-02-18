---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationupdatemanagementazurequery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
ms.openlocfilehash: 68139ff184df62583b3077a38fbc2e26fd5eae09
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201012"
---
# <span data-ttu-id="5105d-101">New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="5105d-101">New-AzAutomationUpdateManagementAzureQuery</span></span>

## <span data-ttu-id="5105d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5105d-102">SYNOPSIS</span></span>
<span data-ttu-id="5105d-103">Azure Automation 소프트웨어 업데이트 구성 Azure 쿼리 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5105d-103">Creates azure automation software update configuration azure query object.</span></span>

## <span data-ttu-id="5105d-104">구문</span><span class="sxs-lookup"><span data-stu-id="5105d-104">SYNTAX</span></span>

```
New-AzAutomationUpdateManagementAzureQuery -Scope <String[]> [-Location <String[]>] [-Tag <Hashtable>]
 [-FilterOperator <TagOperators>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5105d-105">설명</span><span class="sxs-lookup"><span data-stu-id="5105d-105">DESCRIPTION</span></span>
<span data-ttu-id="5105d-106">Azure 가상 머신의 동적으로 확인된 목록 목록을 업데이트하기 위해 일정에 따라 실행되는 소프트웨어 업데이트 구성을 만드는 데 사용할 소프트웨어 업데이트 구성 Azure 쿼리 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5105d-106">Creates a software update configuration azure queries object that will be used to create a software update configuration which will runs on a schedule to update a list of dynamically resolved list of azure virtual machines.</span></span>

## <span data-ttu-id="5105d-107">예제</span><span class="sxs-lookup"><span data-stu-id="5105d-107">EXAMPLES</span></span>

### <span data-ttu-id="5105d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5105d-108">Example 1</span></span>
```powershell
PS C:\>$query1Scope = @(        
"/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/resourceGroupName",
"/subscriptions/32e2445a-0984-4fa5-86a4-0280d76c4b2d/"
    )
PS C:\>$query1Location =@("Japan East", "UK South")
PS C:\>$query1FilterOperator = "All"
PS C:\>$tag1 = @{"tag1"= @("tag1Value1", "tag1Value2")}
PS C:\>$tag1.add("tag2", "tag2Value")
PS C:\>$azq = New-AzAutomationUpdateManagementAzureQuery -ResourceGroupName "mygroup" `
                                       -AutomationAccountName "myaccount" `
                                       -Scope $query1Scope `
                                       -Location $query1Location `
                                       -Tag $tag1
PS C:\>$AzureQueries = @($azq)
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"

PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `                                                 
                                                 -AzureQuery $AzureQueries `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :

```

## <span data-ttu-id="5105d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5105d-109">PARAMETERS</span></span>

### <span data-ttu-id="5105d-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5105d-110">-AutomationAccountName</span></span>
<span data-ttu-id="5105d-111">자동화 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5105d-111">The automation account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5105d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5105d-112">-DefaultProfile</span></span>
<span data-ttu-id="5105d-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5105d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5105d-114">-FilterOperator</span><span class="sxs-lookup"><span data-stu-id="5105d-114">-FilterOperator</span></span>
<span data-ttu-id="5105d-115">태그 필터 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="5105d-115">Tag filter operator.</span></span>

```yaml
Type: TagOperators
Parameter Sets: (All)
Aliases:
Accepted values: All, Any

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="5105d-116">-Location</span><span class="sxs-lookup"><span data-stu-id="5105d-116">-Location</span></span>
<span data-ttu-id="5105d-117">Azure 가상 머신에 대한 위치 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5105d-117">List of locations for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="5105d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5105d-118">-ResourceGroupName</span></span>
<span data-ttu-id="5105d-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5105d-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5105d-120">-Scope</span><span class="sxs-lookup"><span data-stu-id="5105d-120">-Scope</span></span>
<span data-ttu-id="5105d-121">Azure 가상 머신에 대한 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5105d-121">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="5105d-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="5105d-122">-Tag</span></span>
<span data-ttu-id="5105d-123">Azure 가상 머신에 대한 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="5105d-123">Tag for azure virtual machines.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="5105d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5105d-124">CommonParameters</span></span>
<span data-ttu-id="5105d-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5105d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5105d-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5105d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5105d-127">입력</span><span class="sxs-lookup"><span data-stu-id="5105d-127">INPUTS</span></span>

### <span data-ttu-id="5105d-128">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5105d-128">System.String[]</span></span>

### <span data-ttu-id="5105d-129">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5105d-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5105d-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span><span class="sxs-lookup"><span data-stu-id="5105d-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span></span>

### <span data-ttu-id="5105d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="5105d-131">System.String</span></span>

## <span data-ttu-id="5105d-132">출력</span><span class="sxs-lookup"><span data-stu-id="5105d-132">OUTPUTS</span></span>

### <span data-ttu-id="5105d-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span><span class="sxs-lookup"><span data-stu-id="5105d-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span></span>

## <span data-ttu-id="5105d-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5105d-134">NOTES</span></span>

## <span data-ttu-id="5105d-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5105d-135">RELATED LINKS</span></span>

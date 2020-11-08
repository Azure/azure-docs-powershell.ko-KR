---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationupdatemanagementazurequery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
ms.openlocfilehash: 68139ff184df62583b3077a38fbc2e26fd5eae09
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047922"
---
# <span data-ttu-id="afd94-101">New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="afd94-101">New-AzAutomationUpdateManagementAzureQuery</span></span>

## <span data-ttu-id="afd94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afd94-102">SYNOPSIS</span></span>
<span data-ttu-id="afd94-103">Azure automation 소프트웨어 업데이트 구성 azure query 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="afd94-103">Creates azure automation software update configuration azure query object.</span></span>

## <span data-ttu-id="afd94-104">구문과</span><span class="sxs-lookup"><span data-stu-id="afd94-104">SYNTAX</span></span>

```
New-AzAutomationUpdateManagementAzureQuery -Scope <String[]> [-Location <String[]>] [-Tag <Hashtable>]
 [-FilterOperator <TagOperators>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afd94-105">설명은</span><span class="sxs-lookup"><span data-stu-id="afd94-105">DESCRIPTION</span></span>
<span data-ttu-id="afd94-106">동적으로 확인 된 azure 가상 컴퓨터 목록의 목록을 업데이트 하기 위해 일정에 따라 실행 되는 소프트웨어 업데이트 구성을 만드는 데 사용 되는 소프트웨어 업데이트 구성 azure 쿼리 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="afd94-106">Creates a software update configuration azure queries object that will be used to create a software update configuration which will runs on a schedule to update a list of dynamically resolved list of azure virtual machines.</span></span>

## <span data-ttu-id="afd94-107">예제의</span><span class="sxs-lookup"><span data-stu-id="afd94-107">EXAMPLES</span></span>

### <span data-ttu-id="afd94-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="afd94-108">Example 1</span></span>
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

## <span data-ttu-id="afd94-109">변수</span><span class="sxs-lookup"><span data-stu-id="afd94-109">PARAMETERS</span></span>

### <span data-ttu-id="afd94-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="afd94-110">-AutomationAccountName</span></span>
<span data-ttu-id="afd94-111">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd94-111">The automation account name.</span></span>

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

### <span data-ttu-id="afd94-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd94-112">-DefaultProfile</span></span>
<span data-ttu-id="afd94-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="afd94-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afd94-114">-FilterOperator</span><span class="sxs-lookup"><span data-stu-id="afd94-114">-FilterOperator</span></span>
<span data-ttu-id="afd94-115">태그 필터 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="afd94-115">Tag filter operator.</span></span>

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

### <span data-ttu-id="afd94-116">-위치</span><span class="sxs-lookup"><span data-stu-id="afd94-116">-Location</span></span>
<span data-ttu-id="afd94-117">Azure 가상 컴퓨터의 위치 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="afd94-117">List of locations for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="afd94-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afd94-118">-ResourceGroupName</span></span>
<span data-ttu-id="afd94-119">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd94-119">The resource group name.</span></span>

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

### <span data-ttu-id="afd94-120">-범위</span><span class="sxs-lookup"><span data-stu-id="afd94-120">-Scope</span></span>
<span data-ttu-id="afd94-121">Azure 가상 컴퓨터의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="afd94-121">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="afd94-122">태그</span><span class="sxs-lookup"><span data-stu-id="afd94-122">-Tag</span></span>
<span data-ttu-id="afd94-123">Azure 가상 컴퓨터용 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="afd94-123">Tag for azure virtual machines.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="afd94-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd94-124">CommonParameters</span></span>
<span data-ttu-id="afd94-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd94-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="afd94-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afd94-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd94-127">입력</span><span class="sxs-lookup"><span data-stu-id="afd94-127">INPUTS</span></span>

### <span data-ttu-id="afd94-128">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="afd94-128">System.String[]</span></span>

### <span data-ttu-id="afd94-129">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="afd94-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="afd94-130">UpdateManagement. TagOperators에 대 한 자동.</span><span class="sxs-lookup"><span data-stu-id="afd94-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span></span>

### <span data-ttu-id="afd94-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="afd94-131">System.String</span></span>

## <span data-ttu-id="afd94-132">출력</span><span class="sxs-lookup"><span data-stu-id="afd94-132">OUTPUTS</span></span>

### <span data-ttu-id="afd94-133">UpdateManagement. AzureQueryProperties에 대 한 자동.</span><span class="sxs-lookup"><span data-stu-id="afd94-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span></span>

## <span data-ttu-id="afd94-134">상속자</span><span class="sxs-lookup"><span data-stu-id="afd94-134">NOTES</span></span>

## <span data-ttu-id="afd94-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="afd94-135">RELATED LINKS</span></span>

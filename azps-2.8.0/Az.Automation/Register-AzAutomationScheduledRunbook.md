---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
ms.openlocfilehash: df6fc949fe1aa105a84ede2329c71feb4b27a449
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697779"
---
# <span data-ttu-id="55375-101">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="55375-101">Register-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="55375-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55375-102">SYNOPSIS</span></span>
<span data-ttu-id="55375-103">Runbook을 일정에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="55375-103">Associates a runbook to a schedule.</span></span>

## <span data-ttu-id="55375-104">구문과</span><span class="sxs-lookup"><span data-stu-id="55375-104">SYNTAX</span></span>

### <span data-ttu-id="55375-105">ByRunbookName (기본값)</span><span class="sxs-lookup"><span data-stu-id="55375-105">ByRunbookName (Default)</span></span>
```
Register-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55375-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="55375-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Parameters <IDictionary>]
 [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55375-107">설명은</span><span class="sxs-lookup"><span data-stu-id="55375-107">DESCRIPTION</span></span>
<span data-ttu-id="55375-108">**AzAutomationScheduledRunbook** Cmdlet은 Azure Automation runbook을 일정에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="55375-108">The **Register-AzAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="55375-109">*ScheduleName* 매개 변수를 사용 하 여 지정한 일정에 따라 runbook이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="55375-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="55375-110">예제의</span><span class="sxs-lookup"><span data-stu-id="55375-110">EXAMPLES</span></span>

### <span data-ttu-id="55375-111">예제 1: runbook과 일정 연결</span><span class="sxs-lookup"><span data-stu-id="55375-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="55375-112">이 명령은 Runbk01 이라는 runbook을 Contoso17 이라는 Azure Automation 계정의 Sched01 이라는 일정과 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="55375-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="55375-113">변수</span><span class="sxs-lookup"><span data-stu-id="55375-113">PARAMETERS</span></span>

### <span data-ttu-id="55375-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="55375-114">-AutomationAccountName</span></span>
<span data-ttu-id="55375-115">이 cmdlet이 작동 하는 runbook에 대 한 자동화 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55375-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55375-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55375-116">-DefaultProfile</span></span>
<span data-ttu-id="55375-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="55375-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55375-118">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="55375-118">-Parameters</span></span>
<span data-ttu-id="55375-119">키/값 쌍의 해시 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55375-119">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="55375-120">키는 runbook 매개 변수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55375-120">The keys are runbook parameter names.</span></span>
<span data-ttu-id="55375-121">값은 runbook 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="55375-121">The values are runbook parameter values.</span></span>
<span data-ttu-id="55375-122">연결 된 일정에 따라 runbook이 시작 되 면 이러한 매개 변수는 runbook으로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="55375-122">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55375-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55375-123">-ResourceGroupName</span></span>
<span data-ttu-id="55375-124">예약 된 runbook에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55375-124">Specifies the name of a resource group for the scheduled runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55375-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="55375-125">-RunbookName</span></span>
<span data-ttu-id="55375-126">이 cmdlet이 일정에 연결 하는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55375-126">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55375-127">-RunOn</span><span class="sxs-lookup"><span data-stu-id="55375-127">-RunOn</span></span>
<span data-ttu-id="55375-128">Hybrid runbook worker 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55375-128">The name of the hybrid runbook worker group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55375-129">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="55375-129">-ScheduleName</span></span>
<span data-ttu-id="55375-130">이 cmdlet이 runbook을 연결 하는 일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55375-130">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55375-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55375-131">CommonParameters</span></span>
<span data-ttu-id="55375-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="55375-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55375-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55375-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55375-134">입력</span><span class="sxs-lookup"><span data-stu-id="55375-134">INPUTS</span></span>

### <span data-ttu-id="55375-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="55375-135">System.String</span></span>

## <span data-ttu-id="55375-136">출력</span><span class="sxs-lookup"><span data-stu-id="55375-136">OUTPUTS</span></span>

### <span data-ttu-id="55375-137">Microsoft. Azure.-JobSchedule. 모델</span><span class="sxs-lookup"><span data-stu-id="55375-137">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="55375-138">상속자</span><span class="sxs-lookup"><span data-stu-id="55375-138">NOTES</span></span>

## <span data-ttu-id="55375-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55375-139">RELATED LINKS</span></span>

[<span data-ttu-id="55375-140">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="55375-140">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="55375-141">등록 취소-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="55375-141">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)



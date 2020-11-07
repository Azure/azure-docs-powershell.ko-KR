---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: ae638c693366568458a4194d1625d19eaac6af93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701613"
---
# <span data-ttu-id="c46e3-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c46e3-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="c46e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c46e3-102">SYNOPSIS</span></span>
<span data-ttu-id="c46e3-103">자동화 runbook 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="c46e3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c46e3-104">SYNTAX</span></span>

### <span data-ttu-id="c46e3-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="c46e3-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c46e3-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="c46e3-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c46e3-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="c46e3-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c46e3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c46e3-108">DESCRIPTION</span></span>
<span data-ttu-id="c46e3-109">**AzAutomationJob** Cmdlet은 Azure Automation에서 runbook 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="c46e3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c46e3-110">EXAMPLES</span></span>

### <span data-ttu-id="c46e3-111">예제 1: 특정 runbook 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="c46e3-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="c46e3-112">이 명령은 지정 된 GUID가 있는 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="c46e3-113">예제 2: runbook에 대 한 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="c46e3-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="c46e3-114">이 명령은 Runbook02 이라는 runbook과 연결 된 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="c46e3-115">예제 3: 실행 중인 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="c46e3-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="c46e3-116">이 명령은 Contoso17 이라는 자동화 계정에서 실행 중인 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c46e3-117">변수</span><span class="sxs-lookup"><span data-stu-id="c46e3-117">PARAMETERS</span></span>

### <span data-ttu-id="c46e3-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c46e3-118">-AutomationAccountName</span></span>
<span data-ttu-id="c46e3-119">이 cmdlet이 작업을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="c46e3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c46e3-120">-DefaultProfile</span></span>
<span data-ttu-id="c46e3-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c46e3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c46e3-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c46e3-122">-EndTime</span></span>
<span data-ttu-id="c46e3-123">작업의 종료 시간을 **DateTimeOffset** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="c46e3-124">유효한 **DateTimeOffset** 으로 변환할 수 있는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="c46e3-125">이 cmdlet은이 매개 변수에서 지정 하는 값 또는 그 이전에 종료 시간이 있는 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46e3-126">-Id</span><span class="sxs-lookup"><span data-stu-id="c46e3-126">-Id</span></span>
<span data-ttu-id="c46e3-127">이 cmdlet이 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-127">Specifies the ID of a job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c46e3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c46e3-128">-ResourceGroupName</span></span>
<span data-ttu-id="c46e3-129">이 cmdlet이 작업을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="c46e3-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="c46e3-130">-RunbookName</span></span>
<span data-ttu-id="c46e3-131">이 cmdlet이 작업을 가져오는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46e3-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c46e3-132">-StartTime</span></span>
<span data-ttu-id="c46e3-133">작업의 시작 시간을 **DateTimeOffset** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="c46e3-134">이 cmdlet은이 매개 변수에서 지정 하는 값의 시작 시간 또는 그 이후의 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByRunbookName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46e3-135">-상태</span><span class="sxs-lookup"><span data-stu-id="c46e3-135">-Status</span></span>
<span data-ttu-id="c46e3-136">작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-136">Specifies the status of a job.</span></span>
<span data-ttu-id="c46e3-137">이 cmdlet은이 매개 변수와 일치 하는 상태의 상태가 있는 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="c46e3-138">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-138">Valid values are:</span></span> 
- <span data-ttu-id="c46e3-139">인증과</span><span class="sxs-lookup"><span data-stu-id="c46e3-139">Activating</span></span>
- <span data-ttu-id="c46e3-140">완료</span><span class="sxs-lookup"><span data-stu-id="c46e3-140">Completed</span></span>
- <span data-ttu-id="c46e3-141">못함</span><span class="sxs-lookup"><span data-stu-id="c46e3-141">Failed</span></span>
- <span data-ttu-id="c46e3-142">시킵니다</span><span class="sxs-lookup"><span data-stu-id="c46e3-142">Queued</span></span>
- <span data-ttu-id="c46e3-143">계속</span><span class="sxs-lookup"><span data-stu-id="c46e3-143">Resuming</span></span>
- <span data-ttu-id="c46e3-144">실행</span><span class="sxs-lookup"><span data-stu-id="c46e3-144">Running</span></span>
- <span data-ttu-id="c46e3-145">시작</span><span class="sxs-lookup"><span data-stu-id="c46e3-145">Starting</span></span>
- <span data-ttu-id="c46e3-146">멈추었습니다</span><span class="sxs-lookup"><span data-stu-id="c46e3-146">Stopped</span></span>
- <span data-ttu-id="c46e3-147">시작점</span><span class="sxs-lookup"><span data-stu-id="c46e3-147">Stopping</span></span>
- <span data-ttu-id="c46e3-148">된</span><span class="sxs-lookup"><span data-stu-id="c46e3-148">Suspended</span></span>
- <span data-ttu-id="c46e3-149">시키면</span><span class="sxs-lookup"><span data-stu-id="c46e3-149">Suspending</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByRunbookName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c46e3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c46e3-150">CommonParameters</span></span>
<span data-ttu-id="c46e3-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c46e3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c46e3-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c46e3-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c46e3-153">입력</span><span class="sxs-lookup"><span data-stu-id="c46e3-153">INPUTS</span></span>

### <span data-ttu-id="c46e3-154">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="c46e3-154">System.Guid</span></span>

### <span data-ttu-id="c46e3-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c46e3-155">System.String</span></span>

## <span data-ttu-id="c46e3-156">출력</span><span class="sxs-lookup"><span data-stu-id="c46e3-156">OUTPUTS</span></span>

### <span data-ttu-id="c46e3-157">Microsoft. Azure. 작업</span><span class="sxs-lookup"><span data-stu-id="c46e3-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="c46e3-158">상속자</span><span class="sxs-lookup"><span data-stu-id="c46e3-158">NOTES</span></span>

## <span data-ttu-id="c46e3-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c46e3-159">RELATED LINKS</span></span>

[<span data-ttu-id="c46e3-160">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="c46e3-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="c46e3-161">이력서-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c46e3-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="c46e3-162">중지-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c46e3-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="c46e3-163">일시 중단-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c46e3-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)



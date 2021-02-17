---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BD32B909-296B-4E46-A24F-6E2BD4B9764B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJob.md
ms.openlocfilehash: 31390ccb19574b6b88c26828bf504dbc8ac5d924
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210221"
---
# <span data-ttu-id="492b3-101">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="492b3-101">Get-AzAutomationJob</span></span>

## <span data-ttu-id="492b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="492b3-102">SYNOPSIS</span></span>
<span data-ttu-id="492b3-103">Automation Runbook 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="492b3-103">Gets Automation runbook jobs.</span></span>

## <span data-ttu-id="492b3-104">구문</span><span class="sxs-lookup"><span data-stu-id="492b3-104">SYNTAX</span></span>

### <span data-ttu-id="492b3-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="492b3-105">ByAll (Default)</span></span>
```
Get-AzAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="492b3-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="492b3-106">ByJobId</span></span>
```
Get-AzAutomationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="492b3-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="492b3-107">ByRunbookName</span></span>
```
Get-AzAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="492b3-108">설명</span><span class="sxs-lookup"><span data-stu-id="492b3-108">DESCRIPTION</span></span>
<span data-ttu-id="492b3-109">**Get-AzAutomationJob** cmdlet은 Azure Automation에서 Runbook 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="492b3-109">The **Get-AzAutomationJob** cmdlet gets runbook jobs in Azure Automation.</span></span>

## <span data-ttu-id="492b3-110">예제</span><span class="sxs-lookup"><span data-stu-id="492b3-110">EXAMPLES</span></span>

### <span data-ttu-id="492b3-111">예제 1: 특정 Runbook 작업 다운로드</span><span class="sxs-lookup"><span data-stu-id="492b3-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="492b3-112">이 명령은 지정된 GUID가 있는 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="492b3-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="492b3-113">예제 2: Runbook에 대한 모든 작업 다운로드</span><span class="sxs-lookup"><span data-stu-id="492b3-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbook02"
```

<span data-ttu-id="492b3-114">이 명령은 Runbook02라는 Runbook과 연결된 모든 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="492b3-114">This command gets all jobs associated with a runbook named Runbook02.</span></span>

### <span data-ttu-id="492b3-115">예제 3: 실행 중인 모든 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="492b3-115">Example 3: Get all running jobs</span></span>
```
PS C:\>Get-AzAutomationJob -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Status "Running"
```

<span data-ttu-id="492b3-116">이 명령은 Contoso17이라는 Automation 계정에서 실행 중인 모든 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="492b3-116">This command gets all running jobs in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="492b3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="492b3-117">PARAMETERS</span></span>

### <span data-ttu-id="492b3-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="492b3-118">-AutomationAccountName</span></span>
<span data-ttu-id="492b3-119">이 cmdlet이 작업을 받을 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="492b3-119">Specifies the name of an Automation account for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="492b3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="492b3-120">-DefaultProfile</span></span>
<span data-ttu-id="492b3-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="492b3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="492b3-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="492b3-122">-EndTime</span></span>
<span data-ttu-id="492b3-123">작업의 종료 시간을 **DateTimeOffset** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="492b3-123">Specifies the end time for a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="492b3-124">유효한 **DateTimeOffset으로** 변환할 수 있는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="492b3-124">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="492b3-125">이 cmdlet은 이 매개 변수가 지정한 값의 종료 시간이 있는 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="492b3-125">This cmdlet gets jobs that have an end time at or before the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="492b3-126">-Id</span><span class="sxs-lookup"><span data-stu-id="492b3-126">-Id</span></span>
<span data-ttu-id="492b3-127">이 cmdlet이 얻을 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="492b3-127">Specifies the ID of a job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="492b3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="492b3-128">-ResourceGroupName</span></span>
<span data-ttu-id="492b3-129">이 cmdlet이 작업을 받을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="492b3-129">Specifies the name of a resource group in which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="492b3-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="492b3-130">-RunbookName</span></span>
<span data-ttu-id="492b3-131">이 cmdlet이 작업을 받을 Runbook의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="492b3-131">Specifies the name of a runbook for which this cmdlet gets jobs.</span></span>

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

### <span data-ttu-id="492b3-132">-StartTime</span><span class="sxs-lookup"><span data-stu-id="492b3-132">-StartTime</span></span>
<span data-ttu-id="492b3-133">작업의 시작 시간을 **DateTimeOffset** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="492b3-133">Specifies the start time of a job as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="492b3-134">이 cmdlet은 이 매개 변수가 지정한 값의 시작 시간이 있는 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="492b3-134">This cmdlet gets jobs that have a start time at or after the value that this parameter specifies.</span></span>

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

### <span data-ttu-id="492b3-135">-Status</span><span class="sxs-lookup"><span data-stu-id="492b3-135">-Status</span></span>
<span data-ttu-id="492b3-136">작업의 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="492b3-136">Specifies the status of a job.</span></span>
<span data-ttu-id="492b3-137">이 cmdlet은 이 매개 변수와 일치하는 상태가 있는 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="492b3-137">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="492b3-138">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="492b3-138">Valid values are:</span></span> 
- <span data-ttu-id="492b3-139">활성화</span><span class="sxs-lookup"><span data-stu-id="492b3-139">Activating</span></span>
- <span data-ttu-id="492b3-140">완료</span><span class="sxs-lookup"><span data-stu-id="492b3-140">Completed</span></span>
- <span data-ttu-id="492b3-141">실패</span><span class="sxs-lookup"><span data-stu-id="492b3-141">Failed</span></span>
- <span data-ttu-id="492b3-142">큐에 대기</span><span class="sxs-lookup"><span data-stu-id="492b3-142">Queued</span></span>
- <span data-ttu-id="492b3-143">다시 10000</span><span class="sxs-lookup"><span data-stu-id="492b3-143">Resuming</span></span>
- <span data-ttu-id="492b3-144">실행 중</span><span class="sxs-lookup"><span data-stu-id="492b3-144">Running</span></span>
- <span data-ttu-id="492b3-145">시작</span><span class="sxs-lookup"><span data-stu-id="492b3-145">Starting</span></span>
- <span data-ttu-id="492b3-146">중지됨</span><span class="sxs-lookup"><span data-stu-id="492b3-146">Stopped</span></span>
- <span data-ttu-id="492b3-147">중지</span><span class="sxs-lookup"><span data-stu-id="492b3-147">Stopping</span></span>
- <span data-ttu-id="492b3-148">일시 중단</span><span class="sxs-lookup"><span data-stu-id="492b3-148">Suspended</span></span>
- <span data-ttu-id="492b3-149">일시 중단</span><span class="sxs-lookup"><span data-stu-id="492b3-149">Suspending</span></span>

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

### <span data-ttu-id="492b3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="492b3-150">CommonParameters</span></span>
<span data-ttu-id="492b3-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="492b3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="492b3-152">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="492b3-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="492b3-153">입력</span><span class="sxs-lookup"><span data-stu-id="492b3-153">INPUTS</span></span>

### <span data-ttu-id="492b3-154">System.Guid</span><span class="sxs-lookup"><span data-stu-id="492b3-154">System.Guid</span></span>

### <span data-ttu-id="492b3-155">System.String</span><span class="sxs-lookup"><span data-stu-id="492b3-155">System.String</span></span>

## <span data-ttu-id="492b3-156">출력</span><span class="sxs-lookup"><span data-stu-id="492b3-156">OUTPUTS</span></span>

### <span data-ttu-id="492b3-157">Microsoft.Azure.Commands.Automation.Model.Job</span><span class="sxs-lookup"><span data-stu-id="492b3-157">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="492b3-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="492b3-158">NOTES</span></span>

## <span data-ttu-id="492b3-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="492b3-159">RELATED LINKS</span></span>

[<span data-ttu-id="492b3-160">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="492b3-160">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="492b3-161">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="492b3-161">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="492b3-162">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="492b3-162">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="492b3-163">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="492b3-163">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)



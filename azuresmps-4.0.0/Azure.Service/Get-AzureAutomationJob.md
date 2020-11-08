---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6527FF45-9C16-47E8-8E70-619A0581D2F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: c595779fa8c6b4c246f102a346290e931dc89379
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046369"
---
# <span data-ttu-id="6e259-101">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="6e259-101">Get-AzureAutomationJob</span></span>

## <span data-ttu-id="6e259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e259-102">SYNOPSIS</span></span>

<span data-ttu-id="6e259-103">하나 이상의 Azure 자동화 runbook 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e259-103">Gets one or more Azure Automation runbook jobs.</span></span>

## <span data-ttu-id="6e259-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e259-104">SYNTAX</span></span>

### <span data-ttu-id="6e259-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="6e259-105">ByAll (Default)</span></span>
```
Get-AzureAutomationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6e259-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="6e259-106">ByJobId</span></span>
```
Get-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e259-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="6e259-107">ByRunbookName</span></span>
```
Get-AzureAutomationJob -RunbookName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6e259-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6e259-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="6e259-109">**Get-AzureAutomationJob** Cmdlet은 Microsoft Azure Automation에서 하나 이상의 runbook 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e259-109">The **Get-AzureAutomationJob** cmdlet gets one or more runbook jobs in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="6e259-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6e259-110">EXAMPLES</span></span>

### <span data-ttu-id="6e259-111">예제 1: 특정 runbook 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="6e259-111">Example 1: Get a specific runbook job</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b647
```

<span data-ttu-id="6e259-112">이 명령은 지정 된 GUID가 있는 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e259-112">This command gets the job that has the specified GUID.</span></span>

### <span data-ttu-id="6e259-113">예제 2: runbook에 대 한 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="6e259-113">Example 2: Get all jobs for a runbook</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -RunbookName "MyRunbook"
```

<span data-ttu-id="6e259-114">이 명령은 MyRunbook 이라는 runbook과 연결 된 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e259-114">This command gets all jobs associated with a runbook named MyRunbook.</span></span>

### <span data-ttu-id="6e259-115">예제 2: 실행 중인 모든 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="6e259-115">Example 2: Get all running jobs</span></span>
```
PS C:\> Get-AzureAutomationJob -AutomationAccountName "Contoso17" -Status "Running"
```

<span data-ttu-id="6e259-116">이 명령은 Contoso17 이름을 사용 하 여 자동화 계정에서 실행 중인 모든 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e259-116">This command gets all running jobs in the automation account with the name Contoso17.</span></span>

## <span data-ttu-id="6e259-117">변수</span><span class="sxs-lookup"><span data-stu-id="6e259-117">PARAMETERS</span></span>

### <span data-ttu-id="6e259-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6e259-118">-AutomationAccountName</span></span>
<span data-ttu-id="6e259-119">Azure Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e259-119">Specifies the name of an Azure Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e259-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="6e259-120">-EndTime</span></span>
<span data-ttu-id="6e259-121">작업의 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e259-121">Specifies the end time for a job.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e259-122">-Id</span><span class="sxs-lookup"><span data-stu-id="6e259-122">-Id</span></span>
<span data-ttu-id="6e259-123">작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e259-123">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e259-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="6e259-124">-Profile</span></span>
<span data-ttu-id="6e259-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e259-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6e259-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="6e259-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e259-127">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="6e259-127">-RunbookName</span></span>
<span data-ttu-id="6e259-128">Runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e259-128">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e259-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6e259-129">-StartTime</span></span>
<span data-ttu-id="6e259-130">작업의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e259-130">Specifies the start time of a job.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e259-131">-상태</span><span class="sxs-lookup"><span data-stu-id="6e259-131">-Status</span></span>
<span data-ttu-id="6e259-132">작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e259-132">Specifies the status of a job.</span></span>
<span data-ttu-id="6e259-133">이 cmdlet은이 매개 변수와 일치 하는 상태의 상태가 있는 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6e259-133">This cmdlet gets jobs that have a status matching this parameter.</span></span>
<span data-ttu-id="6e259-134">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6e259-134">Valid values are:</span></span> 

- <span data-ttu-id="6e259-135">완료</span><span class="sxs-lookup"><span data-stu-id="6e259-135">Completed</span></span>
- <span data-ttu-id="6e259-136">못함</span><span class="sxs-lookup"><span data-stu-id="6e259-136">Failed</span></span>
- <span data-ttu-id="6e259-137">시킵니다</span><span class="sxs-lookup"><span data-stu-id="6e259-137">Queued</span></span>
- <span data-ttu-id="6e259-138">시작</span><span class="sxs-lookup"><span data-stu-id="6e259-138">Starting</span></span>
- <span data-ttu-id="6e259-139">계속</span><span class="sxs-lookup"><span data-stu-id="6e259-139">Resuming</span></span>
- <span data-ttu-id="6e259-140">실행</span><span class="sxs-lookup"><span data-stu-id="6e259-140">Running</span></span>
- <span data-ttu-id="6e259-141">멈추었습니다</span><span class="sxs-lookup"><span data-stu-id="6e259-141">Stopped</span></span>
- <span data-ttu-id="6e259-142">시작점</span><span class="sxs-lookup"><span data-stu-id="6e259-142">Stopping</span></span>
- <span data-ttu-id="6e259-143">된</span><span class="sxs-lookup"><span data-stu-id="6e259-143">Suspended</span></span>
- <span data-ttu-id="6e259-144">시키면</span><span class="sxs-lookup"><span data-stu-id="6e259-144">Suspending</span></span>
- <span data-ttu-id="6e259-145">인증과</span><span class="sxs-lookup"><span data-stu-id="6e259-145">Activating</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByRunbookName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e259-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e259-146">CommonParameters</span></span>
<span data-ttu-id="6e259-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e259-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e259-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e259-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e259-149">입력</span><span class="sxs-lookup"><span data-stu-id="6e259-149">INPUTS</span></span>

## <span data-ttu-id="6e259-150">출력</span><span class="sxs-lookup"><span data-stu-id="6e259-150">OUTPUTS</span></span>

### <span data-ttu-id="6e259-151">Microsoft. Azure. 작업</span><span class="sxs-lookup"><span data-stu-id="6e259-151">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="6e259-152">상속자</span><span class="sxs-lookup"><span data-stu-id="6e259-152">NOTES</span></span>

## <span data-ttu-id="6e259-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e259-153">RELATED LINKS</span></span>

[<span data-ttu-id="6e259-154">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="6e259-154">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="6e259-155">정지-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="6e259-155">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="6e259-156">일시 중단-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="6e259-156">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)



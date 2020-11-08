---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2F66B0F2-37F3-4046-9FB0-B8C4B90D84A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: d03364038a7a0563e5a8ab2f2f88d36b24da0ebc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046357"
---
# <span data-ttu-id="c203d-101">Get-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="c203d-101">Get-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="c203d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c203d-102">SYNOPSIS</span></span>

<span data-ttu-id="c203d-103">Azure Automation runbook 및 관련 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c203d-103">Gets Azure Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="c203d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c203d-104">SYNTAX</span></span>

### <span data-ttu-id="c203d-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="c203d-105">ByAll (Default)</span></span>
```
Get-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c203d-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="c203d-106">ByJobScheduleId</span></span>
```
Get-AzureAutomationScheduledRunbook -JobScheduleId <Guid> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c203d-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="c203d-107">ByRunbookName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c203d-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="c203d-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c203d-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="c203d-109">ByScheduleName</span></span>
```
Get-AzureAutomationScheduledRunbook -ScheduleName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c203d-110">설명은</span><span class="sxs-lookup"><span data-stu-id="c203d-110">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="c203d-111">**AzureAutomationScheduledRunbook** 는 하나 이상의 Azure 자동화 runbook 및 관련 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c203d-111">The **Get-AzureAutomationScheduledRunbook** gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="c203d-112">기본적으로 예약 된 모든 runbook이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c203d-112">By default, all scheduled runbooks are returned.</span></span>

<span data-ttu-id="c203d-113">예약 된 특정 runbook을 얻으려면 runbook 이름과 일정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c203d-113">To get a specific scheduled runbook, specify the runbook name and the schedule name.</span></span>
<span data-ttu-id="c203d-114">Runbook과 연결 된 모든 일정을 가져오려면 runbook 이름만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c203d-114">To get all schedules associated with a runbook, specify just the runbook name.</span></span>
<span data-ttu-id="c203d-115">일정과 연결 된 모든 runbook을 가져오려면 일정 이름만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c203d-115">To get all runbooks associated with a schedule, specify just the schedule name.</span></span>

## <span data-ttu-id="c203d-116">예제의</span><span class="sxs-lookup"><span data-stu-id="c203d-116">EXAMPLES</span></span>

### <span data-ttu-id="c203d-117">예제 1: 예약 된 모든 runbook 가져오기</span><span class="sxs-lookup"><span data-stu-id="c203d-117">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17"
```

<span data-ttu-id="c203d-118">이 명령은 Contoso17 이라는 자동화 계정에 예약 된 모든 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c203d-118">This command gets all scheduled runbooks in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c203d-119">예제 2: runbook과 연결 된 모든 일정 가져오기</span><span class="sxs-lookup"><span data-stu-id="c203d-119">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -RunbookName "Runbk01"
```

<span data-ttu-id="c203d-120">이 명령은 Contoso17 이라는 Automation 계정에서 runbook Runbk01에 대해 예약 된 모든 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c203d-120">This command gets all scheduled runbooks for the runbook Runbk01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c203d-121">예제 3: 일정과 연결 된 모든 runbook 가져오기</span><span class="sxs-lookup"><span data-stu-id="c203d-121">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\> Get-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ScheduleName "Schedule01"
```

<span data-ttu-id="c203d-122">이 명령은 Contoso17 이라는 Automation 계정에서 일정 Schedule01에 대해 예약 된 모든 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c203d-122">This command gets all scheduled runbooks for the schedule Schedule01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c203d-123">변수</span><span class="sxs-lookup"><span data-stu-id="c203d-123">PARAMETERS</span></span>

### <span data-ttu-id="c203d-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c203d-124">-AutomationAccountName</span></span>
<span data-ttu-id="c203d-125">Azure Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c203d-125">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="c203d-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="c203d-126">-JobScheduleId</span></span>
<span data-ttu-id="c203d-127">예약 된 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c203d-127">Specifies the ID of a scheduled job.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c203d-128">-프로필</span><span class="sxs-lookup"><span data-stu-id="c203d-128">-Profile</span></span>
<span data-ttu-id="c203d-129">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c203d-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c203d-130">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c203d-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c203d-131">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="c203d-131">-RunbookName</span></span>
<span data-ttu-id="c203d-132">Runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c203d-132">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c203d-133">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="c203d-133">-ScheduleName</span></span>
<span data-ttu-id="c203d-134">일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c203d-134">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c203d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c203d-135">CommonParameters</span></span>
<span data-ttu-id="c203d-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c203d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c203d-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c203d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c203d-138">입력</span><span class="sxs-lookup"><span data-stu-id="c203d-138">INPUTS</span></span>

## <span data-ttu-id="c203d-139">출력</span><span class="sxs-lookup"><span data-stu-id="c203d-139">OUTPUTS</span></span>

### <span data-ttu-id="c203d-140">Microsoft. Azure.-JobSchedule. 모델</span><span class="sxs-lookup"><span data-stu-id="c203d-140">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="c203d-141">상속자</span><span class="sxs-lookup"><span data-stu-id="c203d-141">NOTES</span></span>

## <span data-ttu-id="c203d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c203d-142">RELATED LINKS</span></span>

[<span data-ttu-id="c203d-143">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="c203d-143">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)

[<span data-ttu-id="c203d-144">등록 취소-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="c203d-144">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)



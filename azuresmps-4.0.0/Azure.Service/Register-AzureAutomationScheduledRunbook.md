---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6D15837A-22A9-4C5A-8064-C3605088EA71
online version: ''
schema: 2.0.0
ms.openlocfilehash: d31a2ef49674054ca6bb257df67d3439f5abe074
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045873"
---
# <span data-ttu-id="c6d5f-101">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="c6d5f-101">Register-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="c6d5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6d5f-102">SYNOPSIS</span></span>

<span data-ttu-id="c6d5f-103">Runbook을 일정에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d5f-103">Associates a runbook with a schedule.</span></span>

## <span data-ttu-id="c6d5f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6d5f-104">SYNTAX</span></span>

### <span data-ttu-id="c6d5f-105">ByRunbookName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c6d5f-105">ByRunbookName (Default)</span></span>
```
Register-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6d5f-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="c6d5f-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c6d5f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c6d5f-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="c6d5f-108">**AzureAutomationScheduledRunbook** cmdlet은 runbook을 일정과 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d5f-108">The **Register-AzureAutomationScheduledRunbook** cmdlet associates a runbook with a schedule.</span></span>
<span data-ttu-id="c6d5f-109">*ScheduleName* 매개 변수를 사용 하 여 지정한 일정에 따라 runbook이 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6d5f-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="c6d5f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c6d5f-110">EXAMPLES</span></span>

### <span data-ttu-id="c6d5f-111">예제 1: runbook과 일정 연결</span><span class="sxs-lookup"><span data-stu-id="c6d5f-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\> Register-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01"
```

<span data-ttu-id="c6d5f-112">이 명령은 Runbk01 이라는 runbook을 Contoso17 이라는 Azure Automation 계정의 Sched01 이라는 일정과 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d5f-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="c6d5f-113">변수</span><span class="sxs-lookup"><span data-stu-id="c6d5f-113">PARAMETERS</span></span>

### <span data-ttu-id="c6d5f-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c6d5f-114">-AutomationAccountName</span></span>
<span data-ttu-id="c6d5f-115">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d5f-115">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="c6d5f-116">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="c6d5f-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d5f-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="c6d5f-117">-Profile</span></span>
<span data-ttu-id="c6d5f-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d5f-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c6d5f-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c6d5f-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c6d5f-120">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="c6d5f-120">-RunbookName</span></span>
<span data-ttu-id="c6d5f-121">Runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d5f-121">Specifies the name of the runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d5f-122">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="c6d5f-122">-ScheduleName</span></span>
<span data-ttu-id="c6d5f-123">일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d5f-123">Specifies the name of the schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d5f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6d5f-124">CommonParameters</span></span>
<span data-ttu-id="c6d5f-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d5f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6d5f-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6d5f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6d5f-127">입력</span><span class="sxs-lookup"><span data-stu-id="c6d5f-127">INPUTS</span></span>

## <span data-ttu-id="c6d5f-128">출력</span><span class="sxs-lookup"><span data-stu-id="c6d5f-128">OUTPUTS</span></span>

### <span data-ttu-id="c6d5f-129">Microsoft. Azure.-JobSchedule. 모델</span><span class="sxs-lookup"><span data-stu-id="c6d5f-129">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="c6d5f-130">상속자</span><span class="sxs-lookup"><span data-stu-id="c6d5f-130">NOTES</span></span>

## <span data-ttu-id="c6d5f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6d5f-131">RELATED LINKS</span></span>

[<span data-ttu-id="c6d5f-132">새-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c6d5f-132">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="c6d5f-133">등록 취소-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="c6d5f-133">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)



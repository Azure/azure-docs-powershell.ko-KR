---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: EA7C1449-E11F-4AE8-A513-59BDCA38875D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e432edd2469fa25519c12f0cd1f2dadb1d0dca2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046587"
---
# <span data-ttu-id="02b80-101">Unregister-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="02b80-101">Unregister-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="02b80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02b80-102">SYNOPSIS</span></span>

<span data-ttu-id="02b80-103">Runbook과 일정 간의 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b80-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="02b80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02b80-104">SYNTAX</span></span>

### <span data-ttu-id="02b80-105">ByJobScheduleId (기본값)</span><span class="sxs-lookup"><span data-stu-id="02b80-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="02b80-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="02b80-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="02b80-107">설명은</span><span class="sxs-lookup"><span data-stu-id="02b80-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="02b80-108">**AzureAutomationScheduledRunbook** cmdlet은 일정을 시작할 때 runbook이 시작 되는 것을 중지 하는 Microsoft Azure Automation runbook과 일정 간의 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b80-108">The **Unregister-AzureAutomationScheduledRunbook** cmdlet removes the association between a Microsoft Azure Automation runbook and a schedule, which stops the runbook from starting when the schedule fires.</span></span>

## <span data-ttu-id="02b80-109">예제의</span><span class="sxs-lookup"><span data-stu-id="02b80-109">EXAMPLES</span></span>

### <span data-ttu-id="02b80-110">예제 1: runbook과 일정 간 연결 제거</span><span class="sxs-lookup"><span data-stu-id="02b80-110">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\> Unregister-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="02b80-111">이 명령은 Runbk01 이라는 runbook과 Runbk01Sched 이라는 일정 간의 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b80-111">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="02b80-112">변수</span><span class="sxs-lookup"><span data-stu-id="02b80-112">PARAMETERS</span></span>

### <span data-ttu-id="02b80-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="02b80-113">-AutomationAccountName</span></span>
<span data-ttu-id="02b80-114">Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b80-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="02b80-115">-Force</span><span class="sxs-lookup"><span data-stu-id="02b80-115">-Force</span></span>
<span data-ttu-id="02b80-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b80-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02b80-117">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="02b80-117">-JobScheduleId</span></span>
<span data-ttu-id="02b80-118">예약 된 runbook의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b80-118">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="02b80-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="02b80-119">-Profile</span></span>
<span data-ttu-id="02b80-120">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b80-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="02b80-121">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="02b80-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02b80-122">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="02b80-122">-RunbookName</span></span>
<span data-ttu-id="02b80-123">Runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b80-123">Specifies the name of a runbook.</span></span>

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

### <span data-ttu-id="02b80-124">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="02b80-124">-ScheduleName</span></span>
<span data-ttu-id="02b80-125">일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b80-125">Specifies the name of a schedule.</span></span>

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

### <span data-ttu-id="02b80-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02b80-126">CommonParameters</span></span>
<span data-ttu-id="02b80-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02b80-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02b80-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02b80-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02b80-129">입력</span><span class="sxs-lookup"><span data-stu-id="02b80-129">INPUTS</span></span>

## <span data-ttu-id="02b80-130">출력</span><span class="sxs-lookup"><span data-stu-id="02b80-130">OUTPUTS</span></span>

## <span data-ttu-id="02b80-131">상속자</span><span class="sxs-lookup"><span data-stu-id="02b80-131">NOTES</span></span>

## <span data-ttu-id="02b80-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02b80-132">RELATED LINKS</span></span>

[<span data-ttu-id="02b80-133">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="02b80-133">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)



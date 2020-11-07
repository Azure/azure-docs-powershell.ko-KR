---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 2444579c8a155cc2957ab8432eb63cc28300bfe9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697834"
---
# <span data-ttu-id="d02ad-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="d02ad-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="d02ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d02ad-102">SYNOPSIS</span></span>
<span data-ttu-id="d02ad-103">자동화 runbook 및 관련 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d02ad-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="d02ad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d02ad-104">SYNTAX</span></span>

### <span data-ttu-id="d02ad-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="d02ad-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d02ad-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="d02ad-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d02ad-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="d02ad-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d02ad-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="d02ad-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d02ad-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="d02ad-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d02ad-110">설명은</span><span class="sxs-lookup"><span data-stu-id="d02ad-110">DESCRIPTION</span></span>
<span data-ttu-id="d02ad-111">**AzAutomationScheduledRunbook** cmdlet은 하나 이상의 Azure 자동화 runbook 및 관련 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d02ad-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="d02ad-112">기본적으로이 cmdlet은 예약 된 모든 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d02ad-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="d02ad-113">특정 runbook 일정을 보려면 runbook 또는 일정 이름 또는 둘 다를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d02ad-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="d02ad-114">예제의</span><span class="sxs-lookup"><span data-stu-id="d02ad-114">EXAMPLES</span></span>

### <span data-ttu-id="d02ad-115">예제 1: 예약 된 모든 runbook 가져오기</span><span class="sxs-lookup"><span data-stu-id="d02ad-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d02ad-116">이 명령은 Contoso17 이라는 Azure Automation 계정에서 예약 된 모든 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d02ad-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="d02ad-117">예제 2: runbook과 연결 된 모든 일정 가져오기</span><span class="sxs-lookup"><span data-stu-id="d02ad-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="d02ad-118">이 명령은 Contoso17 이라는 Azure Automation 계정에서 runbook Runbk01에 대해 예약 된 모든 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d02ad-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="d02ad-119">예제 3: 일정과 연결 된 모든 runbook 가져오기</span><span class="sxs-lookup"><span data-stu-id="d02ad-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="d02ad-120">이 명령은 Contoso17 이라는 Azure Automation 계정에서 일정 Schedule01에 대해 예약 된 모든 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d02ad-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d02ad-121">변수</span><span class="sxs-lookup"><span data-stu-id="d02ad-121">PARAMETERS</span></span>

### <span data-ttu-id="d02ad-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d02ad-122">-AutomationAccountName</span></span>
<span data-ttu-id="d02ad-123">이 cmdlet이 작동 하는 runbook에 대 한 자동화 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d02ad-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d02ad-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d02ad-124">-DefaultProfile</span></span>
<span data-ttu-id="d02ad-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d02ad-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d02ad-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="d02ad-126">-JobScheduleId</span></span>
<span data-ttu-id="d02ad-127">이 cmdlet이 가져오는 예약 된 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d02ad-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d02ad-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d02ad-128">-ResourceGroupName</span></span>
<span data-ttu-id="d02ad-129">이 cmdlet이 가져오는 예약 된 runbook에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d02ad-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d02ad-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="d02ad-130">-RunbookName</span></span>
<span data-ttu-id="d02ad-131">이 cmdlet에서 예약 된 runbook을 가져오는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d02ad-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d02ad-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="d02ad-132">-ScheduleName</span></span>
<span data-ttu-id="d02ad-133">이 cmdlet에서 예약 된 runbook을 가져오는 일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d02ad-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d02ad-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d02ad-134">CommonParameters</span></span>
<span data-ttu-id="d02ad-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d02ad-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d02ad-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d02ad-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d02ad-137">입력</span><span class="sxs-lookup"><span data-stu-id="d02ad-137">INPUTS</span></span>

### <span data-ttu-id="d02ad-138">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d02ad-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d02ad-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d02ad-139">System.String</span></span>

## <span data-ttu-id="d02ad-140">출력</span><span class="sxs-lookup"><span data-stu-id="d02ad-140">OUTPUTS</span></span>

### <span data-ttu-id="d02ad-141">Microsoft. Azure.-JobSchedule. 모델</span><span class="sxs-lookup"><span data-stu-id="d02ad-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="d02ad-142">상속자</span><span class="sxs-lookup"><span data-stu-id="d02ad-142">NOTES</span></span>

## <span data-ttu-id="d02ad-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d02ad-143">RELATED LINKS</span></span>

[<span data-ttu-id="d02ad-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="d02ad-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="d02ad-145">등록 취소-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="d02ad-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)



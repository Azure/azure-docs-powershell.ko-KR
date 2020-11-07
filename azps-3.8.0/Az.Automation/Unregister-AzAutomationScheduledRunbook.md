---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 53cfa3ccd708871dfe639b0053cb6ab24946bace
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878542"
---
# <span data-ttu-id="ea471-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="ea471-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="ea471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea471-102">SYNOPSIS</span></span>
<span data-ttu-id="ea471-103">Runbook과 일정 간의 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea471-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="ea471-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea471-104">SYNTAX</span></span>

### <span data-ttu-id="ea471-105">ByJobScheduleId (기본값)</span><span class="sxs-lookup"><span data-stu-id="ea471-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea471-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="ea471-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea471-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ea471-107">DESCRIPTION</span></span>
<span data-ttu-id="ea471-108">**AzAutomationScheduledRunbook** Cmdlet은 Azure Automation runbook과 일정 간의 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea471-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="ea471-109">일정이 더 이상 runbook을 시작 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea471-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="ea471-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ea471-110">EXAMPLES</span></span>

### <span data-ttu-id="ea471-111">예제 1: runbook과 일정 간 연결 제거</span><span class="sxs-lookup"><span data-stu-id="ea471-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="ea471-112">이 명령은 Runbk01 이라는 runbook과 Runbk01Sched 이라는 일정 간의 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea471-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="ea471-113">변수</span><span class="sxs-lookup"><span data-stu-id="ea471-113">PARAMETERS</span></span>

### <span data-ttu-id="ea471-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ea471-114">-AutomationAccountName</span></span>
<span data-ttu-id="ea471-115">이 cmdlet이 작동 하는 runbook에 대 한 자동화 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea471-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ea471-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea471-116">-DefaultProfile</span></span>
<span data-ttu-id="ea471-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ea471-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea471-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ea471-118">-Force</span></span>
<span data-ttu-id="ea471-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="ea471-119">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea471-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="ea471-120">-JobScheduleId</span></span>
<span data-ttu-id="ea471-121">예약 된 runbook의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea471-121">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="ea471-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea471-122">-ResourceGroupName</span></span>
<span data-ttu-id="ea471-123">예약 된 runbook에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea471-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="ea471-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="ea471-124">-RunbookName</span></span>
<span data-ttu-id="ea471-125">이 cmdlet이 일정에서 dissociates는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea471-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

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

### <span data-ttu-id="ea471-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="ea471-126">-ScheduleName</span></span>
<span data-ttu-id="ea471-127">이 cmdlet이 runbook을 dissociates 하는 일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea471-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

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

### <span data-ttu-id="ea471-128">-확인</span><span class="sxs-lookup"><span data-stu-id="ea471-128">-Confirm</span></span>
<span data-ttu-id="ea471-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea471-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea471-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea471-130">-WhatIf</span></span>
<span data-ttu-id="ea471-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea471-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea471-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea471-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea471-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea471-133">CommonParameters</span></span>
<span data-ttu-id="ea471-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea471-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea471-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea471-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea471-136">입력</span><span class="sxs-lookup"><span data-stu-id="ea471-136">INPUTS</span></span>

### <span data-ttu-id="ea471-137">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ea471-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ea471-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ea471-138">System.String</span></span>

## <span data-ttu-id="ea471-139">출력</span><span class="sxs-lookup"><span data-stu-id="ea471-139">OUTPUTS</span></span>

### <span data-ttu-id="ea471-140">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="ea471-140">System.Void</span></span>

## <span data-ttu-id="ea471-141">상속자</span><span class="sxs-lookup"><span data-stu-id="ea471-141">NOTES</span></span>

## <span data-ttu-id="ea471-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea471-142">RELATED LINKS</span></span>

[<span data-ttu-id="ea471-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="ea471-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="ea471-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="ea471-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)



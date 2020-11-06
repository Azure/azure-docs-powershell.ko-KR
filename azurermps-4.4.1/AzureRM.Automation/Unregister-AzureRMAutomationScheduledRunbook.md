---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: aa970f71be1e80f9eb5fcc1b4ec24cf0ce7f0e9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535500"
---
# <span data-ttu-id="aada1-101">Unregister-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="aada1-101">Unregister-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="aada1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aada1-102">SYNOPSIS</span></span>
<span data-ttu-id="aada1-103">Runbook과 일정 간의 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aada1-103">Removes an association between a runbook and a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aada1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aada1-104">SYNTAX</span></span>

### <span data-ttu-id="aada1-105">ByJobScheduleId (기본값)</span><span class="sxs-lookup"><span data-stu-id="aada1-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aada1-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="aada1-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aada1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="aada1-107">DESCRIPTION</span></span>
<span data-ttu-id="aada1-108">**AzureRmAutomationScheduledRunbook** Cmdlet은 Azure Automation runbook과 일정 간의 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aada1-108">The **Unregister-AzureRmAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="aada1-109">일정이 더 이상 runbook을 시작 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aada1-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="aada1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="aada1-110">EXAMPLES</span></span>

### <span data-ttu-id="aada1-111">예제 1: runbook과 일정 간 연결 제거</span><span class="sxs-lookup"><span data-stu-id="aada1-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="aada1-112">이 명령은 Runbk01 이라는 runbook과 Runbk01Sched 이라는 일정 간의 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aada1-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="aada1-113">변수</span><span class="sxs-lookup"><span data-stu-id="aada1-113">PARAMETERS</span></span>

### <span data-ttu-id="aada1-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aada1-114">-AutomationAccountName</span></span>
<span data-ttu-id="aada1-115">이 cmdlet이 작동 하는 runbook에 대 한 자동화 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aada1-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="aada1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="aada1-116">-Force</span></span>
<span data-ttu-id="aada1-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="aada1-117">ps_force</span></span>

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

### <span data-ttu-id="aada1-118">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="aada1-118">-JobScheduleId</span></span>
<span data-ttu-id="aada1-119">예약 된 runbook의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aada1-119">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="aada1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aada1-120">-ResourceGroupName</span></span>
<span data-ttu-id="aada1-121">예약 된 runbook에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aada1-121">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="aada1-122">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="aada1-122">-RunbookName</span></span>
<span data-ttu-id="aada1-123">이 cmdlet이 일정에서 dissociates는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aada1-123">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

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

### <span data-ttu-id="aada1-124">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="aada1-124">-ScheduleName</span></span>
<span data-ttu-id="aada1-125">이 cmdlet이 runbook을 dissociates 하는 일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aada1-125">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

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

### <span data-ttu-id="aada1-126">-확인</span><span class="sxs-lookup"><span data-stu-id="aada1-126">-Confirm</span></span>
<span data-ttu-id="aada1-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aada1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aada1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aada1-128">-WhatIf</span></span>
<span data-ttu-id="aada1-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aada1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aada1-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aada1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aada1-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aada1-131">-DefaultProfile</span></span>
<span data-ttu-id="aada1-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aada1-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aada1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aada1-133">CommonParameters</span></span>
<span data-ttu-id="aada1-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aada1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aada1-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aada1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aada1-136">입력</span><span class="sxs-lookup"><span data-stu-id="aada1-136">INPUTS</span></span>

## <span data-ttu-id="aada1-137">출력</span><span class="sxs-lookup"><span data-stu-id="aada1-137">OUTPUTS</span></span>

## <span data-ttu-id="aada1-138">상속자</span><span class="sxs-lookup"><span data-stu-id="aada1-138">NOTES</span></span>

## <span data-ttu-id="aada1-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aada1-139">RELATED LINKS</span></span>

[<span data-ttu-id="aada1-140">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="aada1-140">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="aada1-141">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="aada1-141">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)



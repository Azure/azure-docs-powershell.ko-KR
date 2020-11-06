---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: 459c217904ba44662d18c81c4c493a3b7f2033e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530567"
---
# <span data-ttu-id="06000-101">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="06000-101">Get-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="06000-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06000-102">SYNOPSIS</span></span>
<span data-ttu-id="06000-103">자동화 runbook 및 관련 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06000-103">Gets Automation runbooks and associated schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06000-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06000-104">SYNTAX</span></span>

### <span data-ttu-id="06000-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="06000-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06000-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="06000-106">ByJobScheduleId</span></span>
```
Get-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06000-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="06000-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06000-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="06000-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06000-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="06000-109">ByScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06000-110">설명은</span><span class="sxs-lookup"><span data-stu-id="06000-110">DESCRIPTION</span></span>
<span data-ttu-id="06000-111">**AzureRmAutomationScheduledRunbook** cmdlet은 하나 이상의 Azure 자동화 runbook 및 관련 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06000-111">The **Get-AzureRmAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="06000-112">기본적으로이 cmdlet은 예약 된 모든 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06000-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="06000-113">특정 runbook 일정을 보려면 runbook 또는 일정 이름 또는 둘 다를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06000-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="06000-114">예제의</span><span class="sxs-lookup"><span data-stu-id="06000-114">EXAMPLES</span></span>

### <span data-ttu-id="06000-115">예제 1: 예약 된 모든 runbook 가져오기</span><span class="sxs-lookup"><span data-stu-id="06000-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="06000-116">이 명령은 Contoso17 이라는 Azure Automation 계정에서 예약 된 모든 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06000-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="06000-117">예제 2: runbook과 연결 된 모든 일정 가져오기</span><span class="sxs-lookup"><span data-stu-id="06000-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="06000-118">이 명령은 Contoso17 이라는 Azure Automation 계정에서 runbook Runbk01에 대해 예약 된 모든 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06000-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="06000-119">예제 3: 일정과 연결 된 모든 runbook 가져오기</span><span class="sxs-lookup"><span data-stu-id="06000-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="06000-120">이 명령은 Contoso17 이라는 Azure Automation 계정에서 일정 Schedule01에 대해 예약 된 모든 runbook을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06000-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="06000-121">변수</span><span class="sxs-lookup"><span data-stu-id="06000-121">PARAMETERS</span></span>

### <span data-ttu-id="06000-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="06000-122">-AutomationAccountName</span></span>
<span data-ttu-id="06000-123">이 cmdlet이 작동 하는 runbook에 대 한 자동화 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06000-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06000-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06000-124">-DefaultProfile</span></span>
<span data-ttu-id="06000-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="06000-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06000-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="06000-126">-JobScheduleId</span></span>
<span data-ttu-id="06000-127">이 cmdlet이 가져오는 예약 된 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06000-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="06000-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06000-128">-ResourceGroupName</span></span>
<span data-ttu-id="06000-129">이 cmdlet이 가져오는 예약 된 runbook에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06000-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06000-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="06000-130">-RunbookName</span></span>
<span data-ttu-id="06000-131">이 cmdlet에서 예약 된 runbook을 가져오는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06000-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="06000-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="06000-132">-ScheduleName</span></span>
<span data-ttu-id="06000-133">이 cmdlet에서 예약 된 runbook을 가져오는 일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06000-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="06000-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06000-134">CommonParameters</span></span>
<span data-ttu-id="06000-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06000-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06000-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06000-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06000-137">입력</span><span class="sxs-lookup"><span data-stu-id="06000-137">INPUTS</span></span>

### <span data-ttu-id="06000-138">않아야</span><span class="sxs-lookup"><span data-stu-id="06000-138">None</span></span>
<span data-ttu-id="06000-139">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06000-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06000-140">출력</span><span class="sxs-lookup"><span data-stu-id="06000-140">OUTPUTS</span></span>

### <span data-ttu-id="06000-141">Microsoft. Azure.-JobSchedule. 모델</span><span class="sxs-lookup"><span data-stu-id="06000-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="06000-142">상속자</span><span class="sxs-lookup"><span data-stu-id="06000-142">NOTES</span></span>

## <span data-ttu-id="06000-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06000-143">RELATED LINKS</span></span>

[<span data-ttu-id="06000-144">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="06000-144">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="06000-145">등록 취소-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="06000-145">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)



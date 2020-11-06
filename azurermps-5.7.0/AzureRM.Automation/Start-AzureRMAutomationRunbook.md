---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
ms.openlocfilehash: c3c59c8c4f503b090a77a93014f50dd7e2ce01dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529039"
---
# <span data-ttu-id="18b50-101">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18b50-101">Start-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="18b50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18b50-102">SYNOPSIS</span></span>
<span data-ttu-id="18b50-103">Runbook 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-103">Starts a runbook job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18b50-104">구문과</span><span class="sxs-lookup"><span data-stu-id="18b50-104">SYNTAX</span></span>

### <span data-ttu-id="18b50-105">ByAsynchronousReturnJob (기본값)</span><span class="sxs-lookup"><span data-stu-id="18b50-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18b50-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="18b50-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18b50-107">설명은</span><span class="sxs-lookup"><span data-stu-id="18b50-107">DESCRIPTION</span></span>
<span data-ttu-id="18b50-108">**AzureRmAutomationRunbook** Cmdlet은 Azure Automation runbook 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-108">The **Start-AzureRmAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="18b50-109">Runbook의 ID 또는 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="18b50-110">예제의</span><span class="sxs-lookup"><span data-stu-id="18b50-110">EXAMPLES</span></span>

### <span data-ttu-id="18b50-111">예제 1: runbook 작업 시작</span><span class="sxs-lookup"><span data-stu-id="18b50-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="18b50-112">이 명령은 Contoso17 이라는 Azure Automation 계정에서 Runbk01 이라는 runbook 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="18b50-113">예제 2: runbook 작업 시작 및 결과 대기</span><span class="sxs-lookup"><span data-stu-id="18b50-113">Example 2: Start a runbook job and wait for results</span></span>
```
Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="18b50-114">이 명령은 Contoso17 이라는 Azure Automation 계정에서 Runbk01 이라는 runbook 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-114">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="18b50-115">이 명령은 _Wait_ 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-115">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="18b50-116">따라서 작업이 완료 된 후 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-116">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="18b50-117">Cmdlet은 결과를 최대 1000 초로 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-117">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="18b50-118">변수</span><span class="sxs-lookup"><span data-stu-id="18b50-118">PARAMETERS</span></span>

### <span data-ttu-id="18b50-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="18b50-119">-AutomationAccountName</span></span>
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

### <span data-ttu-id="18b50-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b50-120">-DefaultProfile</span></span>
<span data-ttu-id="18b50-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="18b50-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18b50-122">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="18b50-122">-MaxWaitSeconds</span></span>
<span data-ttu-id="18b50-123">작업을 중단 하기 전에 작업이 완료 될 때까지이 cmdlet이 대기 하는 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-123">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="18b50-124">기본값은 10800 또는 3 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-124">The default value is 10800, or three hours.</span></span>

```yaml
Type: Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b50-125">-이름</span><span class="sxs-lookup"><span data-stu-id="18b50-125">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b50-126">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="18b50-126">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b50-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18b50-127">-ResourceGroupName</span></span>
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

### <span data-ttu-id="18b50-128">-RunOn</span><span class="sxs-lookup"><span data-stu-id="18b50-128">-RunOn</span></span>
<span data-ttu-id="18b50-129">Runbook을 실행할 하이브리드 작업자 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-129">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b50-130">-대기</span><span class="sxs-lookup"><span data-stu-id="18b50-130">-Wait</span></span>
<span data-ttu-id="18b50-131">이 cmdlet이 작업이 완료, 일시 중단 또는 실패할 때까지 기다린 후 Azure PowerShell로 제어를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-131">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18b50-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b50-132">CommonParameters</span></span>
<span data-ttu-id="18b50-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b50-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18b50-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b50-135">입력</span><span class="sxs-lookup"><span data-stu-id="18b50-135">INPUTS</span></span>

### <span data-ttu-id="18b50-136">않아야</span><span class="sxs-lookup"><span data-stu-id="18b50-136">None</span></span>
<span data-ttu-id="18b50-137">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18b50-138">출력</span><span class="sxs-lookup"><span data-stu-id="18b50-138">OUTPUTS</span></span>

### <span data-ttu-id="18b50-139">Microsoft. Azure. 작업</span><span class="sxs-lookup"><span data-stu-id="18b50-139">Microsoft.Azure.Commands.Automation.Model.Job</span></span>
<span data-ttu-id="18b50-140">이 cmdlet은 _Wait_ 매개 변수를 지정 하지 않는 한 **작업** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-140">This cmdlet returns a **Job** object, unless you specify the _Wait_ parameter.</span></span>

<span data-ttu-id="18b50-141">_Wait_ 를 지정 하지 않으면 Azure PowerShell은 **작업** 개체를 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-141">If you do not specify _Wait_ , Azure PowerShell returns a **Job** object immediately.</span></span>
<span data-ttu-id="18b50-142">_Wait_ 를 지정 하는 경우 Azure PowerShell은 작업을 완료 한 다음 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-142">If you specify _Wait_ , Azure PowerShell completes the job, and then returns the result.</span></span>
<span data-ttu-id="18b50-143">결과는 **Job** 개체가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="18b50-143">The result is not a **Job** object.</span></span>

## <span data-ttu-id="18b50-144">상속자</span><span class="sxs-lookup"><span data-stu-id="18b50-144">NOTES</span></span>

## <span data-ttu-id="18b50-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="18b50-145">RELATED LINKS</span></span>

[<span data-ttu-id="18b50-146">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18b50-146">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18b50-147">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18b50-147">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18b50-148">가져오기-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18b50-148">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18b50-149">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18b50-149">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18b50-150">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18b50-150">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18b50-151">게시-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18b50-151">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18b50-152">제거-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18b50-152">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="18b50-153">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="18b50-153">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

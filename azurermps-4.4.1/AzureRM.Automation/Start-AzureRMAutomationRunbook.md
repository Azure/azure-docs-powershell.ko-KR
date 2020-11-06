---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
ms.openlocfilehash: c84410a38cb803eab9dbe4866c7a9426c9c3a21d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528300"
---
# <span data-ttu-id="c00ea-101">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c00ea-101">Start-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="c00ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c00ea-102">SYNOPSIS</span></span>
<span data-ttu-id="c00ea-103">Runbook 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-103">Starts a runbook job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c00ea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c00ea-104">SYNTAX</span></span>

### <span data-ttu-id="c00ea-105">ByAsynchronousReturnJob (기본값)</span><span class="sxs-lookup"><span data-stu-id="c00ea-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c00ea-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="c00ea-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c00ea-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c00ea-107">DESCRIPTION</span></span>
<span data-ttu-id="c00ea-108">**AzureRmAutomationRunbook** Cmdlet은 Azure Automation runbook 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-108">The **Start-AzureRmAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="c00ea-109">Runbook의 ID 또는 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="c00ea-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c00ea-110">EXAMPLES</span></span>

### <span data-ttu-id="c00ea-111">예제 1: runbook 작업 시작</span><span class="sxs-lookup"><span data-stu-id="c00ea-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c00ea-112">이 명령은 Contoso17 이라는 Azure Automation 계정에서 Runbk01 이라는 runbook 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="c00ea-113">예제 2: runbook 작업 시작 및 결과 대기</span><span class="sxs-lookup"><span data-stu-id="c00ea-113">Example 2: Start a runbook job and wait for results</span></span>
```
Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="c00ea-114">이 명령은 Contoso17 이라는 Azure Automation 계정에서 Runbk01 이라는 runbook 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-114">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="c00ea-115">이 명령은 _Wait_ 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-115">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="c00ea-116">따라서 작업이 완료 된 후 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-116">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="c00ea-117">Cmdlet은 결과를 최대 1000 초로 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-117">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="c00ea-118">변수</span><span class="sxs-lookup"><span data-stu-id="c00ea-118">PARAMETERS</span></span>

### <span data-ttu-id="c00ea-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c00ea-119">-AutomationAccountName</span></span>
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

### <span data-ttu-id="c00ea-120">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="c00ea-120">-MaxWaitSeconds</span></span>
<span data-ttu-id="c00ea-121">작업을 중단 하기 전에 작업이 완료 될 때까지이 cmdlet이 대기 하는 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-121">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="c00ea-122">기본값은 10800 또는 3 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-122">The default value is 10800, or three hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00ea-123">-이름</span><span class="sxs-lookup"><span data-stu-id="c00ea-123">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c00ea-124">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="c00ea-124">-Parameters</span></span>
```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00ea-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c00ea-125">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c00ea-126">-RunOn</span><span class="sxs-lookup"><span data-stu-id="c00ea-126">-RunOn</span></span>
<span data-ttu-id="c00ea-127">Runbook을 실행할 하이브리드 작업자 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-127">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c00ea-128">-대기</span><span class="sxs-lookup"><span data-stu-id="c00ea-128">-Wait</span></span>
<span data-ttu-id="c00ea-129">이 cmdlet이 작업이 완료, 일시 중단 또는 실패할 때까지 기다린 후 Azure PowerShell로 제어를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-129">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c00ea-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c00ea-130">-DefaultProfile</span></span>
<span data-ttu-id="c00ea-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c00ea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c00ea-132">CommonParameters</span></span>
<span data-ttu-id="c00ea-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c00ea-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c00ea-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c00ea-135">입력</span><span class="sxs-lookup"><span data-stu-id="c00ea-135">INPUTS</span></span>

## <span data-ttu-id="c00ea-136">출력</span><span class="sxs-lookup"><span data-stu-id="c00ea-136">OUTPUTS</span></span>

### <span data-ttu-id="c00ea-137">Microsoft. Azure. 작업</span><span class="sxs-lookup"><span data-stu-id="c00ea-137">Microsoft.Azure.Commands.Automation.Model.Job</span></span>
<span data-ttu-id="c00ea-138">이 cmdlet은 _Wait_ 매개 변수를 지정 하지 않는 한 **작업** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-138">This cmdlet returns a **Job** object, unless you specify the _Wait_ parameter.</span></span>

<span data-ttu-id="c00ea-139">_Wait_ 를 지정 하지 않으면 Azure PowerShell은 **작업** 개체를 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-139">If you do not specify _Wait_ , Azure PowerShell returns a **Job** object immediately.</span></span>
<span data-ttu-id="c00ea-140">_Wait_ 를 지정 하는 경우 Azure PowerShell은 작업을 완료 한 다음 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-140">If you specify _Wait_ , Azure PowerShell completes the job, and then returns the result.</span></span>
<span data-ttu-id="c00ea-141">결과는 **Job** 개체가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="c00ea-141">The result is not a **Job** object.</span></span>

## <span data-ttu-id="c00ea-142">상속자</span><span class="sxs-lookup"><span data-stu-id="c00ea-142">NOTES</span></span>

## <span data-ttu-id="c00ea-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c00ea-143">RELATED LINKS</span></span>

[<span data-ttu-id="c00ea-144">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c00ea-144">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c00ea-145">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c00ea-145">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c00ea-146">가져오기-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c00ea-146">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c00ea-147">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c00ea-147">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c00ea-148">새로운 AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c00ea-148">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c00ea-149">게시-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c00ea-149">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c00ea-150">제거-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c00ea-150">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c00ea-151">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c00ea-151">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

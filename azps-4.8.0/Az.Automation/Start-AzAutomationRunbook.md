---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 70d322b46f8aa9dc90696cbd813e576cc9dd9fbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049202"
---
# <span data-ttu-id="7c01e-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c01e-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="7c01e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c01e-102">SYNOPSIS</span></span>
<span data-ttu-id="7c01e-103">Runbook 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c01e-103">Starts a runbook job.</span></span>

## <span data-ttu-id="7c01e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c01e-104">SYNTAX</span></span>

### <span data-ttu-id="7c01e-105">ByAsynchronousReturnJob (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c01e-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c01e-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="7c01e-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c01e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7c01e-107">DESCRIPTION</span></span>
<span data-ttu-id="7c01e-108">**AzAutomationRunbook** Cmdlet은 Azure Automation runbook 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c01e-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="7c01e-109">Runbook의 ID 또는 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c01e-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="7c01e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7c01e-110">EXAMPLES</span></span>

### <span data-ttu-id="7c01e-111">예제 1: runbook 작업 시작</span><span class="sxs-lookup"><span data-stu-id="7c01e-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7c01e-112">이 명령은 Contoso17 이라는 Azure Automation 계정에서 Runbk01 이라는 runbook 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c01e-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="7c01e-113">예제 2: 매개 변수를 사용 하 여 Python 2 runbook 작업 시작</span><span class="sxs-lookup"><span data-stu-id="7c01e-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="7c01e-114">이 명령은 "ValueForPosition1"이 있는 Contoso17 이라는 Azure Automation 계정에서 RunbkPy01 이라는 Python 2 runbook에 대 한 runbook 작업을 첫 번째 위치 매개 변수 및 "ValueForPosition2"로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c01e-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="7c01e-115">예제 3: runbook 작업 시작 및 결과 대기</span><span class="sxs-lookup"><span data-stu-id="7c01e-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="7c01e-116">이 명령은 Contoso17 이라는 Azure Automation 계정에서 Runbk01 이라는 runbook 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c01e-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="7c01e-117">이 명령은 _Wait_ 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c01e-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="7c01e-118">따라서 작업이 완료 된 후 결과를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c01e-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="7c01e-119">Cmdlet은 결과를 최대 1000 초로 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="7c01e-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="7c01e-120">변수</span><span class="sxs-lookup"><span data-stu-id="7c01e-120">PARAMETERS</span></span>

### <span data-ttu-id="7c01e-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7c01e-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="7c01e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c01e-122">-DefaultProfile</span></span>
<span data-ttu-id="7c01e-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7c01e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c01e-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="7c01e-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="7c01e-125">작업을 중단 하기 전에 작업이 완료 될 때까지이 cmdlet이 대기 하는 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c01e-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="7c01e-126">기본값은 10800 또는 3 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="7c01e-126">The default value is 10800, or three hours.</span></span>

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

### <span data-ttu-id="7c01e-127">-이름</span><span class="sxs-lookup"><span data-stu-id="7c01e-127">-Name</span></span>
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

### <span data-ttu-id="7c01e-128">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="7c01e-128">-Parameters</span></span>
```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: JobParameters

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c01e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c01e-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="7c01e-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="7c01e-130">-RunOn</span></span>
<span data-ttu-id="7c01e-131">Runbook을 실행할 하이브리드 작업자 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c01e-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

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

### <span data-ttu-id="7c01e-132">-대기</span><span class="sxs-lookup"><span data-stu-id="7c01e-132">-Wait</span></span>
<span data-ttu-id="7c01e-133">이 cmdlet이 작업이 완료, 일시 중단 또는 실패할 때까지 기다린 후 Azure PowerShell로 제어를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7c01e-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

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

### <span data-ttu-id="7c01e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c01e-134">CommonParameters</span></span>
<span data-ttu-id="7c01e-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c01e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c01e-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c01e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c01e-137">입력</span><span class="sxs-lookup"><span data-stu-id="7c01e-137">INPUTS</span></span>

### <span data-ttu-id="7c01e-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c01e-138">System.String</span></span>

## <span data-ttu-id="7c01e-139">출력</span><span class="sxs-lookup"><span data-stu-id="7c01e-139">OUTPUTS</span></span>

### <span data-ttu-id="7c01e-140">Microsoft. Azure. 작업</span><span class="sxs-lookup"><span data-stu-id="7c01e-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="7c01e-141">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="7c01e-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7c01e-142">상속자</span><span class="sxs-lookup"><span data-stu-id="7c01e-142">NOTES</span></span>

## <span data-ttu-id="7c01e-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c01e-143">RELATED LINKS</span></span>

[<span data-ttu-id="7c01e-144">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c01e-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="7c01e-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c01e-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="7c01e-146">가져오기-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c01e-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="7c01e-147">새로운 AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c01e-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="7c01e-148">새로운 AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c01e-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="7c01e-149">게시-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c01e-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="7c01e-150">제거-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c01e-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="7c01e-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7c01e-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

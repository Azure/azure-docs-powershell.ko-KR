---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 5b2c8685596771cd7986d8cfa071808daa63435c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182193"
---
# <span data-ttu-id="dbff7-101">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="dbff7-101">Get-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="dbff7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbff7-102">SYNOPSIS</span></span>
<span data-ttu-id="dbff7-103">Automation에서 DSC 컴파일 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dbff7-103">Gets DSC compilation jobs in Automation.</span></span>

## <span data-ttu-id="dbff7-104">구문</span><span class="sxs-lookup"><span data-stu-id="dbff7-104">SYNTAX</span></span>

### <span data-ttu-id="dbff7-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="dbff7-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dbff7-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="dbff7-106">ByJobId</span></span>
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbff7-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="dbff7-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbff7-108">설명</span><span class="sxs-lookup"><span data-stu-id="dbff7-108">DESCRIPTION</span></span>
<span data-ttu-id="dbff7-109">**Get-AzAutomationDscCompilationJob** cmdlet은 Azure Automation에서 APS DSC(Desired State Configuration) 컴파일 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dbff7-109">The **Get-AzAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="dbff7-110">예제</span><span class="sxs-lookup"><span data-stu-id="dbff7-110">EXAMPLES</span></span>

### <span data-ttu-id="dbff7-111">예제 1: 모든 DSC 컴파일 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="dbff7-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="dbff7-112">이 명령은 Contoso17이라는 Automation 계정의 모든 컴파일 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dbff7-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="dbff7-113">예제 2: 구성에 대한 DSC 컴파일 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="dbff7-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="dbff7-114">이 명령은 Contoso17이라는 Automation 계정에서 ContosoConfiguration이라는 DSC 구성에 대한 모든 컴파일 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dbff7-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="dbff7-115">예제 3: 특정 DSC 컴파일 작업 얻기</span><span class="sxs-lookup"><span data-stu-id="dbff7-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="dbff7-116">이 명령은 Contoso17이라는 Automation 계정에서 지정된 ID를 사용하여 컴파일 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dbff7-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="dbff7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbff7-117">PARAMETERS</span></span>

### <span data-ttu-id="dbff7-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dbff7-118">-AutomationAccountName</span></span>
<span data-ttu-id="dbff7-119">이 cmdlet에서 얻을 DSC 컴파일 작업을 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dbff7-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dbff7-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="dbff7-120">-ConfigurationName</span></span>
<span data-ttu-id="dbff7-121">이 cmdlet이 컴파일 작업을 받을 DSC 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dbff7-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbff7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbff7-122">-DefaultProfile</span></span>
<span data-ttu-id="dbff7-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dbff7-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbff7-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="dbff7-124">-EndTime</span></span>
<span data-ttu-id="dbff7-125">종료 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dbff7-125">Specifies an end time.</span></span>
<span data-ttu-id="dbff7-126">이 cmdlet은 이 매개 변수가 지정한 시간까지 시작된 컴파일 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dbff7-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbff7-127">-Id</span><span class="sxs-lookup"><span data-stu-id="dbff7-127">-Id</span></span>
<span data-ttu-id="dbff7-128">이 cmdlet에서 얻을 DSC 컴파일 작업의 고유 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dbff7-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbff7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbff7-129">-ResourceGroupName</span></span>
<span data-ttu-id="dbff7-130">이 cmdlet이 DSC 컴파일 작업을 받을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dbff7-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="dbff7-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dbff7-131">-StartTime</span></span>
<span data-ttu-id="dbff7-132">시작 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dbff7-132">Specifies a start time.</span></span>
<span data-ttu-id="dbff7-133">이 cmdlet은 이 매개 변수가 지정한 시간 이후에 시작하는 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dbff7-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbff7-134">-Status</span><span class="sxs-lookup"><span data-stu-id="dbff7-134">-Status</span></span>
<span data-ttu-id="dbff7-135">이 cmdlet이 얻을 작업의 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dbff7-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="dbff7-136">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="dbff7-136">Valid values are:</span></span> 
- <span data-ttu-id="dbff7-137">완료</span><span class="sxs-lookup"><span data-stu-id="dbff7-137">Completed</span></span> 
- <span data-ttu-id="dbff7-138">실패</span><span class="sxs-lookup"><span data-stu-id="dbff7-138">Failed</span></span> 
- <span data-ttu-id="dbff7-139">큐에 대기</span><span class="sxs-lookup"><span data-stu-id="dbff7-139">Queued</span></span> 
- <span data-ttu-id="dbff7-140">시작</span><span class="sxs-lookup"><span data-stu-id="dbff7-140">Starting</span></span> 
- <span data-ttu-id="dbff7-141">다시 10000</span><span class="sxs-lookup"><span data-stu-id="dbff7-141">Resuming</span></span> 
- <span data-ttu-id="dbff7-142">실행 중</span><span class="sxs-lookup"><span data-stu-id="dbff7-142">Running</span></span> 
- <span data-ttu-id="dbff7-143">중지됨</span><span class="sxs-lookup"><span data-stu-id="dbff7-143">Stopped</span></span> 
- <span data-ttu-id="dbff7-144">중지</span><span class="sxs-lookup"><span data-stu-id="dbff7-144">Stopping</span></span> 
- <span data-ttu-id="dbff7-145">일시 중단</span><span class="sxs-lookup"><span data-stu-id="dbff7-145">Suspended</span></span> 
- <span data-ttu-id="dbff7-146">일시 중단</span><span class="sxs-lookup"><span data-stu-id="dbff7-146">Suspending</span></span> 
- <span data-ttu-id="dbff7-147">활성화</span><span class="sxs-lookup"><span data-stu-id="dbff7-147">Activating</span></span>
- <span data-ttu-id="dbff7-148">새로운</span><span class="sxs-lookup"><span data-stu-id="dbff7-148">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbff7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbff7-149">CommonParameters</span></span>
<span data-ttu-id="dbff7-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dbff7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbff7-151">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dbff7-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbff7-152">입력</span><span class="sxs-lookup"><span data-stu-id="dbff7-152">INPUTS</span></span>

### <span data-ttu-id="dbff7-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="dbff7-153">System.Guid</span></span>

### <span data-ttu-id="dbff7-154">System.String</span><span class="sxs-lookup"><span data-stu-id="dbff7-154">System.String</span></span>

## <span data-ttu-id="dbff7-155">출력</span><span class="sxs-lookup"><span data-stu-id="dbff7-155">OUTPUTS</span></span>

### <span data-ttu-id="dbff7-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="dbff7-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="dbff7-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dbff7-157">NOTES</span></span>

## <span data-ttu-id="dbff7-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbff7-158">RELATED LINKS</span></span>

[<span data-ttu-id="dbff7-159">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="dbff7-159">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="dbff7-160">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="dbff7-160">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)



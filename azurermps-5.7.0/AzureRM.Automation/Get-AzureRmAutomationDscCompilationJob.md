---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: c7e4043cb6883020b8af15d13dd46c395997e116
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538072"
---
# <span data-ttu-id="fcdc5-101">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="fcdc5-101">Get-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="fcdc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcdc5-102">SYNOPSIS</span></span>
<span data-ttu-id="fcdc5-103">자동화에서 DSC 컴파일 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-103">Gets DSC compilation jobs in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcdc5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fcdc5-104">SYNTAX</span></span>

### <span data-ttu-id="fcdc5-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="fcdc5-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcdc5-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="fcdc5-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcdc5-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="fcdc5-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>]
 [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcdc5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fcdc5-108">DESCRIPTION</span></span>
<span data-ttu-id="fcdc5-109">**AzureRmAutomationDscCompilationJob** Cmdlet은 Azure AUTOMATION의 DSC (원하는 상태 구성) 컴파일 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-109">The **Get-AzureRmAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="fcdc5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fcdc5-110">EXAMPLES</span></span>

### <span data-ttu-id="fcdc5-111">예제 1: 모든 DSC 컴파일 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="fcdc5-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="fcdc5-112">이 명령은 Contoso17 이라는 자동화 계정에 있는 모든 컴파일 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="fcdc5-113">예제 2: 구성에 대 한 DSC 컴파일 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="fcdc5-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="fcdc5-114">이 명령은 Contoso17 이라는 Automation 계정에서 ContosoConfiguration 이라는 DSC 구성에 대 한 모든 컴파일 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="fcdc5-115">예제 3: 특정 DSC 컴파일 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="fcdc5-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="fcdc5-116">이 명령은 Contoso17 이라는 자동화 계정에서 지정 된 ID를 가진 컴파일 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="fcdc5-117">변수</span><span class="sxs-lookup"><span data-stu-id="fcdc5-117">PARAMETERS</span></span>

### <span data-ttu-id="fcdc5-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fcdc5-118">-AutomationAccountName</span></span>
<span data-ttu-id="fcdc5-119">이 cmdlet이 가져오는 DSC 컴파일 작업을 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fcdc5-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="fcdc5-120">-ConfigurationName</span></span>
<span data-ttu-id="fcdc5-121">이 cmdlet이 컴파일 작업을 가져오는 DSC 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

```yaml
Type: String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcdc5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcdc5-122">-DefaultProfile</span></span>
<span data-ttu-id="fcdc5-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fcdc5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcdc5-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="fcdc5-124">-EndTime</span></span>
<span data-ttu-id="fcdc5-125">종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-125">Specifies an end time.</span></span>
<span data-ttu-id="fcdc5-126">이 cmdlet은이 매개 변수가 지정 하는 시간까지 시작 되는 컴파일 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByConfigurationName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcdc5-127">-Id</span><span class="sxs-lookup"><span data-stu-id="fcdc5-127">-Id</span></span>
<span data-ttu-id="fcdc5-128">이 cmdlet이 가져오는 DSC 컴파일 작업의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcdc5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcdc5-129">-ResourceGroupName</span></span>
<span data-ttu-id="fcdc5-130">이 cmdlet이 DSC 컴파일 작업을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="fcdc5-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="fcdc5-131">-StartTime</span></span>
<span data-ttu-id="fcdc5-132">시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-132">Specifies a start time.</span></span>
<span data-ttu-id="fcdc5-133">이 cmdlet은이 매개 변수가 지정 하는 시간 또는 그 이후에 시작 되는 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll, ByConfigurationName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcdc5-134">-상태</span><span class="sxs-lookup"><span data-stu-id="fcdc5-134">-Status</span></span>
<span data-ttu-id="fcdc5-135">이 cmdlet이 가져오는 작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="fcdc5-136">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-136">Valid values are:</span></span> 

- <span data-ttu-id="fcdc5-137">완료</span><span class="sxs-lookup"><span data-stu-id="fcdc5-137">Completed</span></span> 
- <span data-ttu-id="fcdc5-138">못함</span><span class="sxs-lookup"><span data-stu-id="fcdc5-138">Failed</span></span> 
- <span data-ttu-id="fcdc5-139">시킵니다</span><span class="sxs-lookup"><span data-stu-id="fcdc5-139">Queued</span></span> 
- <span data-ttu-id="fcdc5-140">시작</span><span class="sxs-lookup"><span data-stu-id="fcdc5-140">Starting</span></span> 
- <span data-ttu-id="fcdc5-141">계속</span><span class="sxs-lookup"><span data-stu-id="fcdc5-141">Resuming</span></span> 
- <span data-ttu-id="fcdc5-142">실행</span><span class="sxs-lookup"><span data-stu-id="fcdc5-142">Running</span></span> 
- <span data-ttu-id="fcdc5-143">멈추었습니다</span><span class="sxs-lookup"><span data-stu-id="fcdc5-143">Stopped</span></span> 
- <span data-ttu-id="fcdc5-144">시작점</span><span class="sxs-lookup"><span data-stu-id="fcdc5-144">Stopping</span></span> 
- <span data-ttu-id="fcdc5-145">된</span><span class="sxs-lookup"><span data-stu-id="fcdc5-145">Suspended</span></span> 
- <span data-ttu-id="fcdc5-146">시키면</span><span class="sxs-lookup"><span data-stu-id="fcdc5-146">Suspending</span></span> 
- <span data-ttu-id="fcdc5-147">인증과</span><span class="sxs-lookup"><span data-stu-id="fcdc5-147">Activating</span></span>
- <span data-ttu-id="fcdc5-148">새로운</span><span class="sxs-lookup"><span data-stu-id="fcdc5-148">New</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcdc5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcdc5-149">CommonParameters</span></span>
<span data-ttu-id="fcdc5-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcdc5-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcdc5-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcdc5-152">입력</span><span class="sxs-lookup"><span data-stu-id="fcdc5-152">INPUTS</span></span>

### <span data-ttu-id="fcdc5-153">않아야</span><span class="sxs-lookup"><span data-stu-id="fcdc5-153">None</span></span>
<span data-ttu-id="fcdc5-154">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fcdc5-155">출력</span><span class="sxs-lookup"><span data-stu-id="fcdc5-155">OUTPUTS</span></span>

### <span data-ttu-id="fcdc5-156">CompilationJob를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="fcdc5-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="fcdc5-157">상속자</span><span class="sxs-lookup"><span data-stu-id="fcdc5-157">NOTES</span></span>

## <span data-ttu-id="fcdc5-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcdc5-158">RELATED LINKS</span></span>

[<span data-ttu-id="fcdc5-159">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="fcdc5-159">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="fcdc5-160">시작-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="fcdc5-160">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)



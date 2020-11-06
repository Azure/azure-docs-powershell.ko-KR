---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 59263dab3037e050229bab2a69c43559c2c1827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533188"
---
# <span data-ttu-id="55c4d-101">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="55c4d-101">Get-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="55c4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="55c4d-103">자동화에서 DSC 컴파일 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="55c4d-103">Gets DSC compilation jobs in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55c4d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="55c4d-104">SYNTAX</span></span>

### <span data-ttu-id="55c4d-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="55c4d-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55c4d-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="55c4d-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55c4d-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="55c4d-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>]
 [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55c4d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="55c4d-108">DESCRIPTION</span></span>
<span data-ttu-id="55c4d-109">**AzureRmAutomationDscCompilationJob** Cmdlet은 Azure AUTOMATION의 DSC (원하는 상태 구성) 컴파일 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="55c4d-109">The **Get-AzureRmAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="55c4d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="55c4d-110">EXAMPLES</span></span>

### <span data-ttu-id="55c4d-111">예제 1: 모든 DSC 컴파일 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="55c4d-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="55c4d-112">이 명령은 Contoso17 이라는 자동화 계정에 있는 모든 컴파일 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="55c4d-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="55c4d-113">예제 2: 구성에 대 한 DSC 컴파일 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="55c4d-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="55c4d-114">이 명령은 Contoso17 이라는 Automation 계정에서 ContosoConfiguration 이라는 DSC 구성에 대 한 모든 컴파일 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="55c4d-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="55c4d-115">예제 3: 특정 DSC 컴파일 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="55c4d-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="55c4d-116">이 명령은 Contoso17 이라는 자동화 계정에서 지정 된 ID를 가진 컴파일 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="55c4d-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="55c4d-117">변수</span><span class="sxs-lookup"><span data-stu-id="55c4d-117">PARAMETERS</span></span>

### <span data-ttu-id="55c4d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="55c4d-118">-AutomationAccountName</span></span>
<span data-ttu-id="55c4d-119">이 cmdlet이 가져오는 DSC 컴파일 작업을 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55c4d-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="55c4d-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="55c4d-120">-ConfigurationName</span></span>
<span data-ttu-id="55c4d-121">이 cmdlet이 컴파일 작업을 가져오는 DSC 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55c4d-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

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

### <span data-ttu-id="55c4d-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="55c4d-122">-EndTime</span></span>
<span data-ttu-id="55c4d-123">종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55c4d-123">Specifies an end time.</span></span>
<span data-ttu-id="55c4d-124">이 cmdlet은이 매개 변수가 지정 하는 시간까지 시작 되는 컴파일 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="55c4d-124">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="55c4d-125">-Id</span><span class="sxs-lookup"><span data-stu-id="55c4d-125">-Id</span></span>
<span data-ttu-id="55c4d-126">이 cmdlet이 가져오는 DSC 컴파일 작업의 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55c4d-126">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="55c4d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55c4d-127">-ResourceGroupName</span></span>
<span data-ttu-id="55c4d-128">이 cmdlet이 DSC 컴파일 작업을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55c4d-128">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="55c4d-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="55c4d-129">-StartTime</span></span>
<span data-ttu-id="55c4d-130">시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55c4d-130">Specifies a start time.</span></span>
<span data-ttu-id="55c4d-131">이 cmdlet은이 매개 변수가 지정 하는 시간 또는 그 이후에 시작 되는 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="55c4d-131">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="55c4d-132">-상태</span><span class="sxs-lookup"><span data-stu-id="55c4d-132">-Status</span></span>
<span data-ttu-id="55c4d-133">이 cmdlet이 가져오는 작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="55c4d-133">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="55c4d-134">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="55c4d-134">Valid values are:</span></span> 

- <span data-ttu-id="55c4d-135">완료</span><span class="sxs-lookup"><span data-stu-id="55c4d-135">Completed</span></span> 
- <span data-ttu-id="55c4d-136">못함</span><span class="sxs-lookup"><span data-stu-id="55c4d-136">Failed</span></span> 
- <span data-ttu-id="55c4d-137">시킵니다</span><span class="sxs-lookup"><span data-stu-id="55c4d-137">Queued</span></span> 
- <span data-ttu-id="55c4d-138">시작</span><span class="sxs-lookup"><span data-stu-id="55c4d-138">Starting</span></span> 
- <span data-ttu-id="55c4d-139">계속</span><span class="sxs-lookup"><span data-stu-id="55c4d-139">Resuming</span></span> 
- <span data-ttu-id="55c4d-140">실행</span><span class="sxs-lookup"><span data-stu-id="55c4d-140">Running</span></span> 
- <span data-ttu-id="55c4d-141">멈추었습니다</span><span class="sxs-lookup"><span data-stu-id="55c4d-141">Stopped</span></span> 
- <span data-ttu-id="55c4d-142">시작점</span><span class="sxs-lookup"><span data-stu-id="55c4d-142">Stopping</span></span> 
- <span data-ttu-id="55c4d-143">된</span><span class="sxs-lookup"><span data-stu-id="55c4d-143">Suspended</span></span> 
- <span data-ttu-id="55c4d-144">시키면</span><span class="sxs-lookup"><span data-stu-id="55c4d-144">Suspending</span></span> 
- <span data-ttu-id="55c4d-145">인증과</span><span class="sxs-lookup"><span data-stu-id="55c4d-145">Activating</span></span>
- <span data-ttu-id="55c4d-146">새로운</span><span class="sxs-lookup"><span data-stu-id="55c4d-146">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c4d-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55c4d-147">-DefaultProfile</span></span>
<span data-ttu-id="55c4d-148">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55c4d-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55c4d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c4d-149">CommonParameters</span></span>
<span data-ttu-id="55c4d-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="55c4d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c4d-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55c4d-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c4d-152">입력</span><span class="sxs-lookup"><span data-stu-id="55c4d-152">INPUTS</span></span>

## <span data-ttu-id="55c4d-153">출력</span><span class="sxs-lookup"><span data-stu-id="55c4d-153">OUTPUTS</span></span>

### <span data-ttu-id="55c4d-154">CompilationJob를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="55c4d-154">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="55c4d-155">상속자</span><span class="sxs-lookup"><span data-stu-id="55c4d-155">NOTES</span></span>

## <span data-ttu-id="55c4d-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55c4d-156">RELATED LINKS</span></span>

[<span data-ttu-id="55c4d-157">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="55c4d-157">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="55c4d-158">시작-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="55c4d-158">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)



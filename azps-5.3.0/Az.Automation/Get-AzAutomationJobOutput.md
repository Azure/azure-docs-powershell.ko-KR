---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: 53ae09ba82de2a96bc9db17ad7ca538c48b23a47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494328"
---
# <span data-ttu-id="1f4f4-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="1f4f4-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="1f4f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f4f4-102">SYNOPSIS</span></span>
<span data-ttu-id="1f4f4-103">Automation 작업의 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f4-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="1f4f4-104">구문</span><span class="sxs-lookup"><span data-stu-id="1f4f4-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f4f4-105">설명</span><span class="sxs-lookup"><span data-stu-id="1f4f4-105">DESCRIPTION</span></span>
<span data-ttu-id="1f4f4-106">**Get-AzAutomationJobOutput** cmdlet은 Azure Automation 작업의 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f4-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="1f4f4-107">예제</span><span class="sxs-lookup"><span data-stu-id="1f4f4-107">EXAMPLES</span></span>

### <span data-ttu-id="1f4f4-108">예제 1: Automation 작업의 출력을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f4-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="1f4f4-109">이 명령은 지정된 ID가 있는 작업의 모든 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f4-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="1f4f4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f4f4-110">PARAMETERS</span></span>

### <span data-ttu-id="1f4f4-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1f4f4-111">-AutomationAccountName</span></span>
<span data-ttu-id="1f4f4-112">이 cmdlet이 작업 출력을 얻을 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f4-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="1f4f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f4f4-113">-DefaultProfile</span></span>
<span data-ttu-id="1f4f4-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1f4f4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f4f4-115">-Id</span><span class="sxs-lookup"><span data-stu-id="1f4f4-115">-Id</span></span>
<span data-ttu-id="1f4f4-116">이 cmdlet이 출력을 받을 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f4-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f4f4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f4f4-117">-ResourceGroupName</span></span>
<span data-ttu-id="1f4f4-118">이 cmdlet이 작업 출력을 얻을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f4-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="1f4f4-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1f4f4-119">-StartTime</span></span>
<span data-ttu-id="1f4f4-120">시작 시간을 **DateTimeOffset 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="1f4f4-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="1f4f4-121">유효한 **DateTimeOffset으로** 변환할 수 있는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f4-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="1f4f4-122">cmdlet은 이 시간 후에 생성된 출력을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f4-122">The cmdlet retrieves output created after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f4f4-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="1f4f4-123">-Stream</span></span>
<span data-ttu-id="1f4f4-124">출력의 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f4-124">Specifies the type of output.</span></span>
<span data-ttu-id="1f4f4-125">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="1f4f4-125">Valid values are:</span></span> 
- <span data-ttu-id="1f4f4-126">모든</span><span class="sxs-lookup"><span data-stu-id="1f4f4-126">Any</span></span>
- <span data-ttu-id="1f4f4-127">디버그</span><span class="sxs-lookup"><span data-stu-id="1f4f4-127">Debug</span></span>
- <span data-ttu-id="1f4f4-128">오류</span><span class="sxs-lookup"><span data-stu-id="1f4f4-128">Error</span></span>
- <span data-ttu-id="1f4f4-129">출력</span><span class="sxs-lookup"><span data-stu-id="1f4f4-129">Output</span></span>
- <span data-ttu-id="1f4f4-130">진행률</span><span class="sxs-lookup"><span data-stu-id="1f4f4-130">Progress</span></span>
- <span data-ttu-id="1f4f4-131">Verbose</span><span class="sxs-lookup"><span data-stu-id="1f4f4-131">Verbose</span></span>
- <span data-ttu-id="1f4f4-132">경고</span><span class="sxs-lookup"><span data-stu-id="1f4f4-132">Warning</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Progress, Output, Warning, Error, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f4f4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f4f4-133">CommonParameters</span></span>
<span data-ttu-id="1f4f4-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1f4f4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f4f4-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1f4f4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f4f4-136">입력</span><span class="sxs-lookup"><span data-stu-id="1f4f4-136">INPUTS</span></span>

### <span data-ttu-id="1f4f4-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="1f4f4-137">System.Guid</span></span>

### <span data-ttu-id="1f4f4-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span><span class="sxs-lookup"><span data-stu-id="1f4f4-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="1f4f4-139">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1f4f4-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1f4f4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1f4f4-140">System.String</span></span>

## <span data-ttu-id="1f4f4-141">출력</span><span class="sxs-lookup"><span data-stu-id="1f4f4-141">OUTPUTS</span></span>

### <span data-ttu-id="1f4f4-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="1f4f4-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="1f4f4-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1f4f4-143">NOTES</span></span>

## <span data-ttu-id="1f4f4-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f4f4-144">RELATED LINKS</span></span>

[<span data-ttu-id="1f4f4-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1f4f4-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="1f4f4-146">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1f4f4-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="1f4f4-147">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1f4f4-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="1f4f4-148">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1f4f4-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: f49c0bbf17ed87d782b03052d9caeb5aba51eeff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996963"
---
# <span data-ttu-id="bc348-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="bc348-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="bc348-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc348-102">SYNOPSIS</span></span>
<span data-ttu-id="bc348-103">Automation 작업의 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bc348-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="bc348-104">구문</span><span class="sxs-lookup"><span data-stu-id="bc348-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc348-105">설명</span><span class="sxs-lookup"><span data-stu-id="bc348-105">DESCRIPTION</span></span>
<span data-ttu-id="bc348-106">**Get-AzAutomationJobOutput** cmdlet은 Azure Automation 작업의 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bc348-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="bc348-107">예제</span><span class="sxs-lookup"><span data-stu-id="bc348-107">EXAMPLES</span></span>

### <span data-ttu-id="bc348-108">예제 1: Automation 작업의 출력을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc348-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="bc348-109">이 명령은 지정된 ID가 있는 작업의 모든 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bc348-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="bc348-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bc348-110">PARAMETERS</span></span>

### <span data-ttu-id="bc348-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bc348-111">-AutomationAccountName</span></span>
<span data-ttu-id="bc348-112">이 cmdlet에서 작업 출력을 얻을 수 있는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc348-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="bc348-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc348-113">-DefaultProfile</span></span>
<span data-ttu-id="bc348-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bc348-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc348-115">-Id</span><span class="sxs-lookup"><span data-stu-id="bc348-115">-Id</span></span>
<span data-ttu-id="bc348-116">이 cmdlet에서 출력을 얻을 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc348-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="bc348-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc348-117">-ResourceGroupName</span></span>
<span data-ttu-id="bc348-118">이 cmdlet에서 작업 출력을 얻을 수 있는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc348-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="bc348-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bc348-119">-StartTime</span></span>
<span data-ttu-id="bc348-120">시작 시간을 **DateTimeOffset 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="bc348-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="bc348-121">유효한 **DateTimeOffset로** 변환할 수 있는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc348-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="bc348-122">cmdlet은 이 시간 이후에 생성된 출력을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="bc348-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="bc348-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="bc348-123">-Stream</span></span>
<span data-ttu-id="bc348-124">출력 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bc348-124">Specifies the type of output.</span></span>
<span data-ttu-id="bc348-125">유효한 값은:</span><span class="sxs-lookup"><span data-stu-id="bc348-125">Valid values are:</span></span> 
- <span data-ttu-id="bc348-126">모든</span><span class="sxs-lookup"><span data-stu-id="bc348-126">Any</span></span>
- <span data-ttu-id="bc348-127">디버그</span><span class="sxs-lookup"><span data-stu-id="bc348-127">Debug</span></span>
- <span data-ttu-id="bc348-128">오류</span><span class="sxs-lookup"><span data-stu-id="bc348-128">Error</span></span>
- <span data-ttu-id="bc348-129">출력</span><span class="sxs-lookup"><span data-stu-id="bc348-129">Output</span></span>
- <span data-ttu-id="bc348-130">진행률</span><span class="sxs-lookup"><span data-stu-id="bc348-130">Progress</span></span>
- <span data-ttu-id="bc348-131">현명한</span><span class="sxs-lookup"><span data-stu-id="bc348-131">Verbose</span></span>
- <span data-ttu-id="bc348-132">경고</span><span class="sxs-lookup"><span data-stu-id="bc348-132">Warning</span></span>

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

### <span data-ttu-id="bc348-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc348-133">CommonParameters</span></span>
<span data-ttu-id="bc348-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc348-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc348-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bc348-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc348-136">입력</span><span class="sxs-lookup"><span data-stu-id="bc348-136">INPUTS</span></span>

### <span data-ttu-id="bc348-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="bc348-137">System.Guid</span></span>

### <span data-ttu-id="bc348-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span><span class="sxs-lookup"><span data-stu-id="bc348-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="bc348-139">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bc348-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bc348-140">System.String</span><span class="sxs-lookup"><span data-stu-id="bc348-140">System.String</span></span>

## <span data-ttu-id="bc348-141">출력</span><span class="sxs-lookup"><span data-stu-id="bc348-141">OUTPUTS</span></span>

### <span data-ttu-id="bc348-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="bc348-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="bc348-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bc348-143">NOTES</span></span>

## <span data-ttu-id="bc348-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc348-144">RELATED LINKS</span></span>

[<span data-ttu-id="bc348-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="bc348-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="bc348-146">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="bc348-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="bc348-147">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="bc348-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="bc348-148">suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="bc348-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)



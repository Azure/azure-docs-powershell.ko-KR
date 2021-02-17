---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: 53ae09ba82de2a96bc9db17ad7ca538c48b23a47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210213"
---
# <span data-ttu-id="97896-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="97896-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="97896-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97896-102">SYNOPSIS</span></span>
<span data-ttu-id="97896-103">Automation 작업의 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="97896-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="97896-104">구문</span><span class="sxs-lookup"><span data-stu-id="97896-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97896-105">설명</span><span class="sxs-lookup"><span data-stu-id="97896-105">DESCRIPTION</span></span>
<span data-ttu-id="97896-106">**Get-AzAutomationJobOutput** cmdlet은 Azure Automation 작업의 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="97896-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="97896-107">예제</span><span class="sxs-lookup"><span data-stu-id="97896-107">EXAMPLES</span></span>

### <span data-ttu-id="97896-108">예제 1: Automation 작업의 출력을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="97896-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="97896-109">이 명령은 지정된 ID가 있는 작업의 모든 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="97896-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="97896-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97896-110">PARAMETERS</span></span>

### <span data-ttu-id="97896-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="97896-111">-AutomationAccountName</span></span>
<span data-ttu-id="97896-112">이 cmdlet이 작업 출력을 얻을 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="97896-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="97896-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97896-113">-DefaultProfile</span></span>
<span data-ttu-id="97896-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="97896-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97896-115">-Id</span><span class="sxs-lookup"><span data-stu-id="97896-115">-Id</span></span>
<span data-ttu-id="97896-116">이 cmdlet이 출력을 얻을 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="97896-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="97896-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97896-117">-ResourceGroupName</span></span>
<span data-ttu-id="97896-118">이 cmdlet이 작업 출력을 얻을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="97896-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="97896-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="97896-119">-StartTime</span></span>
<span data-ttu-id="97896-120">시작 시간을 **DateTimeOffset 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="97896-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="97896-121">유효한 **DateTimeOffset으로** 변환할 수 있는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97896-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="97896-122">cmdlet은 이 시간 후에 생성된 출력을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="97896-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="97896-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="97896-123">-Stream</span></span>
<span data-ttu-id="97896-124">출력 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="97896-124">Specifies the type of output.</span></span>
<span data-ttu-id="97896-125">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="97896-125">Valid values are:</span></span> 
- <span data-ttu-id="97896-126">모든</span><span class="sxs-lookup"><span data-stu-id="97896-126">Any</span></span>
- <span data-ttu-id="97896-127">디버그</span><span class="sxs-lookup"><span data-stu-id="97896-127">Debug</span></span>
- <span data-ttu-id="97896-128">오류</span><span class="sxs-lookup"><span data-stu-id="97896-128">Error</span></span>
- <span data-ttu-id="97896-129">출력</span><span class="sxs-lookup"><span data-stu-id="97896-129">Output</span></span>
- <span data-ttu-id="97896-130">진행률</span><span class="sxs-lookup"><span data-stu-id="97896-130">Progress</span></span>
- <span data-ttu-id="97896-131">Verbose</span><span class="sxs-lookup"><span data-stu-id="97896-131">Verbose</span></span>
- <span data-ttu-id="97896-132">경고</span><span class="sxs-lookup"><span data-stu-id="97896-132">Warning</span></span>

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

### <span data-ttu-id="97896-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97896-133">CommonParameters</span></span>
<span data-ttu-id="97896-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="97896-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97896-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="97896-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97896-136">입력</span><span class="sxs-lookup"><span data-stu-id="97896-136">INPUTS</span></span>

### <span data-ttu-id="97896-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="97896-137">System.Guid</span></span>

### <span data-ttu-id="97896-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span><span class="sxs-lookup"><span data-stu-id="97896-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="97896-139">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="97896-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="97896-140">System.String</span><span class="sxs-lookup"><span data-stu-id="97896-140">System.String</span></span>

## <span data-ttu-id="97896-141">출력</span><span class="sxs-lookup"><span data-stu-id="97896-141">OUTPUTS</span></span>

### <span data-ttu-id="97896-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="97896-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="97896-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="97896-143">NOTES</span></span>

## <span data-ttu-id="97896-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97896-144">RELATED LINKS</span></span>

[<span data-ttu-id="97896-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="97896-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="97896-146">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="97896-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="97896-147">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="97896-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="97896-148">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="97896-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)



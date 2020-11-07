---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: 60de6b852d516cd4742ed253d149ea031449548b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701616"
---
# <span data-ttu-id="b6bd7-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="b6bd7-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="b6bd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6bd7-102">SYNOPSIS</span></span>
<span data-ttu-id="b6bd7-103">자동화 작업의 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6bd7-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="b6bd7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b6bd7-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6bd7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b6bd7-105">DESCRIPTION</span></span>
<span data-ttu-id="b6bd7-106">**AzAutomationJobOutput** Cmdlet은 Azure Automation 작업의 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6bd7-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="b6bd7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b6bd7-107">EXAMPLES</span></span>

### <span data-ttu-id="b6bd7-108">예제 1: 자동화 작업의 출력 가져오기</span><span class="sxs-lookup"><span data-stu-id="b6bd7-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="b6bd7-109">이 명령은 지정 된 ID를 갖는 모든 작업의 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6bd7-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="b6bd7-110">변수</span><span class="sxs-lookup"><span data-stu-id="b6bd7-110">PARAMETERS</span></span>

### <span data-ttu-id="b6bd7-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b6bd7-111">-AutomationAccountName</span></span>
<span data-ttu-id="b6bd7-112">이 cmdlet에서 작업 출력을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bd7-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="b6bd7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6bd7-113">-DefaultProfile</span></span>
<span data-ttu-id="b6bd7-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b6bd7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6bd7-115">-Id</span><span class="sxs-lookup"><span data-stu-id="b6bd7-115">-Id</span></span>
<span data-ttu-id="b6bd7-116">이 cmdlet이 출력을 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bd7-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="b6bd7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6bd7-117">-ResourceGroupName</span></span>
<span data-ttu-id="b6bd7-118">이 cmdlet에서 작업 출력을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bd7-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="b6bd7-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b6bd7-119">-StartTime</span></span>
<span data-ttu-id="b6bd7-120">시작 시간을 **DateTimeOffset** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bd7-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="b6bd7-121">유효한 **DateTimeOffset** 으로 변환할 수 있는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6bd7-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="b6bd7-122">Cmdlet은이 시간 후에 만들어진 출력을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bd7-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="b6bd7-123">-스트림</span><span class="sxs-lookup"><span data-stu-id="b6bd7-123">-Stream</span></span>
<span data-ttu-id="b6bd7-124">출력 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bd7-124">Specifies the type of output.</span></span>
<span data-ttu-id="b6bd7-125">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b6bd7-125">Valid values are:</span></span> 
- <span data-ttu-id="b6bd7-126">이상</span><span class="sxs-lookup"><span data-stu-id="b6bd7-126">Any</span></span>
- <span data-ttu-id="b6bd7-127">디버깅이</span><span class="sxs-lookup"><span data-stu-id="b6bd7-127">Debug</span></span>
- <span data-ttu-id="b6bd7-128">오류</span><span class="sxs-lookup"><span data-stu-id="b6bd7-128">Error</span></span>
- <span data-ttu-id="b6bd7-129">결과물</span><span class="sxs-lookup"><span data-stu-id="b6bd7-129">Output</span></span>
- <span data-ttu-id="b6bd7-130">진행률과</span><span class="sxs-lookup"><span data-stu-id="b6bd7-130">Progress</span></span>
- <span data-ttu-id="b6bd7-131">정보</span><span class="sxs-lookup"><span data-stu-id="b6bd7-131">Verbose</span></span>
- <span data-ttu-id="b6bd7-132">오류</span><span class="sxs-lookup"><span data-stu-id="b6bd7-132">Warning</span></span>

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

### <span data-ttu-id="b6bd7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6bd7-133">CommonParameters</span></span>
<span data-ttu-id="b6bd7-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bd7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6bd7-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6bd7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6bd7-136">입력</span><span class="sxs-lookup"><span data-stu-id="b6bd7-136">INPUTS</span></span>

### <span data-ttu-id="b6bd7-137">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="b6bd7-137">System.Guid</span></span>

### <span data-ttu-id="b6bd7-138">Microsoft Azure. 일반적인 StreamType</span><span class="sxs-lookup"><span data-stu-id="b6bd7-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="b6bd7-139">시스템 Null 허용 ' 1 [[CoreLib, System.webserver, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b6bd7-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b6bd7-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b6bd7-140">System.String</span></span>

## <span data-ttu-id="b6bd7-141">출력</span><span class="sxs-lookup"><span data-stu-id="b6bd7-141">OUTPUTS</span></span>

### <span data-ttu-id="b6bd7-142">Microsoft. Azure. JobStream</span><span class="sxs-lookup"><span data-stu-id="b6bd7-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="b6bd7-143">상속자</span><span class="sxs-lookup"><span data-stu-id="b6bd7-143">NOTES</span></span>

## <span data-ttu-id="b6bd7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6bd7-144">RELATED LINKS</span></span>

[<span data-ttu-id="b6bd7-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b6bd7-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="b6bd7-146">이력서-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b6bd7-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="b6bd7-147">중지-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b6bd7-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="b6bd7-148">일시 중단-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b6bd7-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


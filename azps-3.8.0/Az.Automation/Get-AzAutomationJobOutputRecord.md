---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: e43cb76db410752aef0a0cffc72d3d5bb6f8e28f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042675"
---
# <span data-ttu-id="e4243-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="e4243-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="e4243-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4243-102">SYNOPSIS</span></span>
<span data-ttu-id="e4243-103">자동화 작업 출력 레코드의 전체 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4243-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="e4243-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e4243-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4243-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e4243-105">DESCRIPTION</span></span>
<span data-ttu-id="e4243-106">**Get-AzAutomationJobOutputRecord** Cmdlet은 자동화 작업 출력 레코드의 전체 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4243-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="e4243-107">**AzAutomationJobOutput** cmdlet에는 하나 이상의 작업 출력 레코드가 나열 되지만 출력 레코드의 값에 대 한 요약만 문자열로 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4243-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="e4243-108">원본 형식에 출력 레코드의 출력할 수 있는 값의 전체 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4243-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="e4243-109">또한 요약에는이 cmdlet이 출력 하는 전체 값이 초과할 수 있는 최대 길이가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4243-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="e4243-110">**Get-AzAutomationJobOutput** 와 달리이 cmdlet은 출력 레코드의 출력 된 값에 대해 원래 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4243-110">Unlike **Get-AzAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="e4243-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e4243-111">EXAMPLES</span></span>

### <span data-ttu-id="e4243-112">예제 1: 자동화 작업의 전체 출력 가져오기</span><span class="sxs-lookup"><span data-stu-id="e4243-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="e4243-113">이 명령은 지정 된 작업 ID를 가진 작업의 전체 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4243-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="e4243-114">변수</span><span class="sxs-lookup"><span data-stu-id="e4243-114">PARAMETERS</span></span>

### <span data-ttu-id="e4243-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e4243-115">-AutomationAccountName</span></span>
<span data-ttu-id="e4243-116">이 cmdlet에서 작업 출력 레코드를 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4243-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="e4243-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4243-117">-DefaultProfile</span></span>
<span data-ttu-id="e4243-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e4243-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4243-119">-Id</span><span class="sxs-lookup"><span data-stu-id="e4243-119">-Id</span></span>
<span data-ttu-id="e4243-120">이 cmdlet이 검색할 작업 출력 레코드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4243-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4243-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="e4243-121">-JobId</span></span>
<span data-ttu-id="e4243-122">이 cmdlet에서 출력 레코드를 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4243-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4243-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4243-123">-ResourceGroupName</span></span>
<span data-ttu-id="e4243-124">이 cmdlet에서 작업 출력 레코드를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4243-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="e4243-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4243-125">CommonParameters</span></span>
<span data-ttu-id="e4243-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4243-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4243-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4243-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4243-128">입력</span><span class="sxs-lookup"><span data-stu-id="e4243-128">INPUTS</span></span>

### <span data-ttu-id="e4243-129">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="e4243-129">System.Guid</span></span>

### <span data-ttu-id="e4243-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e4243-130">System.String</span></span>

## <span data-ttu-id="e4243-131">출력</span><span class="sxs-lookup"><span data-stu-id="e4243-131">OUTPUTS</span></span>

### <span data-ttu-id="e4243-132">Microsoft. Azure. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="e4243-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="e4243-133">상속자</span><span class="sxs-lookup"><span data-stu-id="e4243-133">NOTES</span></span>

## <span data-ttu-id="e4243-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4243-134">RELATED LINKS</span></span>

[<span data-ttu-id="e4243-135">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="e4243-135">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)



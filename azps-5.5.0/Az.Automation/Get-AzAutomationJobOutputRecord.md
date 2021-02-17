---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210189"
---
# <span data-ttu-id="fd179-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="fd179-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="fd179-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd179-102">SYNOPSIS</span></span>
<span data-ttu-id="fd179-103">Automation 작업 출력 레코드의 전체 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fd179-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="fd179-104">구문</span><span class="sxs-lookup"><span data-stu-id="fd179-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd179-105">설명</span><span class="sxs-lookup"><span data-stu-id="fd179-105">DESCRIPTION</span></span>
<span data-ttu-id="fd179-106">**Get-AzAutomationJobOutputRecord** cmdlet은 Automation 작업 출력 레코드의 전체 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fd179-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="fd179-107">**Get-AzAutomationJobOutput** cmdlet은 하나 이상의 작업 출력 레코드를 나열하나, 출력 레코드 값의 문자열로 요약만 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fd179-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="fd179-108">원래 형식에서 출력 레코드의 출력 값의 전체 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd179-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="fd179-109">또한 요약에는 이 cmdlet 출력이 초과할 수 있는 전체 값이 있는 최대 길이가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd179-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>

## <span data-ttu-id="fd179-110">예제</span><span class="sxs-lookup"><span data-stu-id="fd179-110">EXAMPLES</span></span>

### <span data-ttu-id="fd179-111">예제 1: Automation 작업의 전체 출력을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd179-111">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="fd179-112">이 명령은 지정된 작업 ID가 있는 작업의 전체 출력을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fd179-112">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="fd179-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd179-113">PARAMETERS</span></span>

### <span data-ttu-id="fd179-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fd179-114">-AutomationAccountName</span></span>
<span data-ttu-id="fd179-115">이 cmdlet이 작업 출력 레코드를 얻을 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd179-115">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="fd179-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd179-116">-DefaultProfile</span></span>
<span data-ttu-id="fd179-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fd179-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd179-118">-Id</span><span class="sxs-lookup"><span data-stu-id="fd179-118">-Id</span></span>
<span data-ttu-id="fd179-119">검색할 이 cmdlet에 대한 작업 출력 레코드의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd179-119">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="fd179-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="fd179-120">-JobId</span></span>
<span data-ttu-id="fd179-121">이 cmdlet이 출력 레코드를 얻을 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd179-121">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="fd179-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd179-122">-ResourceGroupName</span></span>
<span data-ttu-id="fd179-123">이 cmdlet이 작업 출력 레코드를 얻을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd179-123">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="fd179-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd179-124">CommonParameters</span></span>
<span data-ttu-id="fd179-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fd179-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd179-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fd179-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd179-127">입력</span><span class="sxs-lookup"><span data-stu-id="fd179-127">INPUTS</span></span>

### <span data-ttu-id="fd179-128">System.Guid</span><span class="sxs-lookup"><span data-stu-id="fd179-128">System.Guid</span></span>

### <span data-ttu-id="fd179-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fd179-129">System.String</span></span>

## <span data-ttu-id="fd179-130">출력</span><span class="sxs-lookup"><span data-stu-id="fd179-130">OUTPUTS</span></span>

### <span data-ttu-id="fd179-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="fd179-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="fd179-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fd179-132">NOTES</span></span>

## <span data-ttu-id="fd179-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd179-133">RELATED LINKS</span></span>

[<span data-ttu-id="fd179-134">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="fd179-134">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)



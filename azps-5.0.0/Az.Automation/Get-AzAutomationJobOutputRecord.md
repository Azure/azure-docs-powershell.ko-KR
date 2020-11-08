---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219116"
---
# <span data-ttu-id="628c0-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="628c0-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="628c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="628c0-102">SYNOPSIS</span></span>
<span data-ttu-id="628c0-103">자동화 작업 출력 레코드의 전체 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="628c0-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="628c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="628c0-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="628c0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="628c0-105">DESCRIPTION</span></span>
<span data-ttu-id="628c0-106">**Get-AzAutomationJobOutputRecord** Cmdlet은 자동화 작업 출력 레코드의 전체 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="628c0-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="628c0-107">**AzAutomationJobOutput** cmdlet에는 하나 이상의 작업 출력 레코드가 나열 되지만 출력 레코드의 값에 대 한 요약만 문자열로 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="628c0-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="628c0-108">원본 형식에 출력 레코드의 출력할 수 있는 값의 전체 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="628c0-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="628c0-109">또한 요약에는이 cmdlet이 출력 하는 전체 값이 초과할 수 있는 최대 길이가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="628c0-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>

## <span data-ttu-id="628c0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="628c0-110">EXAMPLES</span></span>

### <span data-ttu-id="628c0-111">예제 1: 자동화 작업의 전체 출력 가져오기</span><span class="sxs-lookup"><span data-stu-id="628c0-111">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="628c0-112">이 명령은 지정 된 작업 ID를 가진 작업의 전체 출력을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="628c0-112">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="628c0-113">변수</span><span class="sxs-lookup"><span data-stu-id="628c0-113">PARAMETERS</span></span>

### <span data-ttu-id="628c0-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="628c0-114">-AutomationAccountName</span></span>
<span data-ttu-id="628c0-115">이 cmdlet에서 작업 출력 레코드를 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="628c0-115">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="628c0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="628c0-116">-DefaultProfile</span></span>
<span data-ttu-id="628c0-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="628c0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="628c0-118">-Id</span><span class="sxs-lookup"><span data-stu-id="628c0-118">-Id</span></span>
<span data-ttu-id="628c0-119">이 cmdlet이 검색할 작업 출력 레코드의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="628c0-119">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="628c0-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="628c0-120">-JobId</span></span>
<span data-ttu-id="628c0-121">이 cmdlet에서 출력 레코드를 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="628c0-121">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="628c0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="628c0-122">-ResourceGroupName</span></span>
<span data-ttu-id="628c0-123">이 cmdlet에서 작업 출력 레코드를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="628c0-123">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="628c0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="628c0-124">CommonParameters</span></span>
<span data-ttu-id="628c0-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="628c0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="628c0-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="628c0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="628c0-127">입력</span><span class="sxs-lookup"><span data-stu-id="628c0-127">INPUTS</span></span>

### <span data-ttu-id="628c0-128">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="628c0-128">System.Guid</span></span>

### <span data-ttu-id="628c0-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="628c0-129">System.String</span></span>

## <span data-ttu-id="628c0-130">출력</span><span class="sxs-lookup"><span data-stu-id="628c0-130">OUTPUTS</span></span>

### <span data-ttu-id="628c0-131">Microsoft. Azure. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="628c0-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="628c0-132">상속자</span><span class="sxs-lookup"><span data-stu-id="628c0-132">NOTES</span></span>

## <span data-ttu-id="628c0-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="628c0-133">RELATED LINKS</span></span>

[<span data-ttu-id="628c0-134">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="628c0-134">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)



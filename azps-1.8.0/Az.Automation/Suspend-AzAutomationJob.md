---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 850ff932bdae35bd21ab83c745b5da8c056d778d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701483"
---
# <span data-ttu-id="d206c-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d206c-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="d206c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d206c-102">SYNOPSIS</span></span>
<span data-ttu-id="d206c-103">자동화 작업을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="d206c-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="d206c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d206c-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d206c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d206c-105">DESCRIPTION</span></span>
<span data-ttu-id="d206c-106">**AzAutomationJob** Cmdlet은 Azure Automation 작업을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="d206c-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="d206c-107">실행 중인 자동화 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d206c-107">Specify a running Automation job.</span></span>
<span data-ttu-id="d206c-108">일시 중단 된 작업을 다시 시작 하려면 Resume-AzAutomationJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d206c-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="d206c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d206c-109">EXAMPLES</span></span>

### <span data-ttu-id="d206c-110">예제 1: 작업 일시 중단</span><span class="sxs-lookup"><span data-stu-id="d206c-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d206c-111">이 명령은 지정 된 ID를 가진 작업을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="d206c-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="d206c-112">변수</span><span class="sxs-lookup"><span data-stu-id="d206c-112">PARAMETERS</span></span>

### <span data-ttu-id="d206c-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d206c-113">-AutomationAccountName</span></span>
<span data-ttu-id="d206c-114">이 cmdlet이 작업을 일시 중단 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d206c-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="d206c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d206c-115">-DefaultProfile</span></span>
<span data-ttu-id="d206c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d206c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d206c-117">-Id</span><span class="sxs-lookup"><span data-stu-id="d206c-117">-Id</span></span>
<span data-ttu-id="d206c-118">이 cmdlet이 일시 중단 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d206c-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="d206c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d206c-119">-ResourceGroupName</span></span>
<span data-ttu-id="d206c-120">이 cmdlet이 일시 중단 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d206c-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="d206c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d206c-121">CommonParameters</span></span>
<span data-ttu-id="d206c-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d206c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d206c-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d206c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d206c-124">입력</span><span class="sxs-lookup"><span data-stu-id="d206c-124">INPUTS</span></span>

### <span data-ttu-id="d206c-125">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="d206c-125">System.Guid</span></span>

### <span data-ttu-id="d206c-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d206c-126">System.String</span></span>

## <span data-ttu-id="d206c-127">출력</span><span class="sxs-lookup"><span data-stu-id="d206c-127">OUTPUTS</span></span>

### <span data-ttu-id="d206c-128">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="d206c-128">System.Void</span></span>

## <span data-ttu-id="d206c-129">상속자</span><span class="sxs-lookup"><span data-stu-id="d206c-129">NOTES</span></span>

## <span data-ttu-id="d206c-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d206c-130">RELATED LINKS</span></span>

[<span data-ttu-id="d206c-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d206c-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="d206c-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="d206c-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="d206c-133">이력서-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d206c-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="d206c-134">중지-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="d206c-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)



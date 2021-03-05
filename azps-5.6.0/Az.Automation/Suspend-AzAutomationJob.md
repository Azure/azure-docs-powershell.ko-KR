---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 035cd77ab389b9c3cdce686620b3157b4b046c41
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981275"
---
# <span data-ttu-id="0c03d-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0c03d-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="0c03d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c03d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c03d-103">Automation 작업을 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="0c03d-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="0c03d-104">구문</span><span class="sxs-lookup"><span data-stu-id="0c03d-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c03d-105">설명</span><span class="sxs-lookup"><span data-stu-id="0c03d-105">DESCRIPTION</span></span>
<span data-ttu-id="0c03d-106">**Suspend-AzAutomationJob** cmdlet은 Azure Automation 작업을 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="0c03d-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="0c03d-107">실행 중인 Automation 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c03d-107">Specify a running Automation job.</span></span>
<span data-ttu-id="0c03d-108">일시 중단된 작업을 다시 시작하기 위해 Resume-AzAutomationJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c03d-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="0c03d-109">예제</span><span class="sxs-lookup"><span data-stu-id="0c03d-109">EXAMPLES</span></span>

### <span data-ttu-id="0c03d-110">예제 1: 작업 일시 중단</span><span class="sxs-lookup"><span data-stu-id="0c03d-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0c03d-111">이 명령은 지정된 ID가 있는 작업을 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="0c03d-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="0c03d-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0c03d-112">PARAMETERS</span></span>

### <span data-ttu-id="0c03d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0c03d-113">-AutomationAccountName</span></span>
<span data-ttu-id="0c03d-114">이 cmdlet이 작업을 일시 중단하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c03d-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="0c03d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c03d-115">-DefaultProfile</span></span>
<span data-ttu-id="0c03d-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0c03d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c03d-117">-Id</span><span class="sxs-lookup"><span data-stu-id="0c03d-117">-Id</span></span>
<span data-ttu-id="0c03d-118">이 cmdlet이 일시 중단하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c03d-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="0c03d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c03d-119">-ResourceGroupName</span></span>
<span data-ttu-id="0c03d-120">이 cmdlet이 일시 중단하는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c03d-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="0c03d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c03d-121">CommonParameters</span></span>
<span data-ttu-id="0c03d-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0c03d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c03d-123">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0c03d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c03d-124">입력</span><span class="sxs-lookup"><span data-stu-id="0c03d-124">INPUTS</span></span>

### <span data-ttu-id="0c03d-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="0c03d-125">System.Guid</span></span>

### <span data-ttu-id="0c03d-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0c03d-126">System.String</span></span>

## <span data-ttu-id="0c03d-127">출력</span><span class="sxs-lookup"><span data-stu-id="0c03d-127">OUTPUTS</span></span>

### <span data-ttu-id="0c03d-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="0c03d-128">System.Void</span></span>

## <span data-ttu-id="0c03d-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0c03d-129">NOTES</span></span>

## <span data-ttu-id="0c03d-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c03d-130">RELATED LINKS</span></span>

[<span data-ttu-id="0c03d-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0c03d-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="0c03d-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="0c03d-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="0c03d-133">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0c03d-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="0c03d-134">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="0c03d-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)



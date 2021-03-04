---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/powershell/module/az.automation/resume-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
ms.openlocfilehash: 68520eda43b3586e63930b6a96cec2fc6483c594
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957755"
---
# <span data-ttu-id="8cf5a-101">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8cf5a-101">Resume-AzAutomationJob</span></span>

## <span data-ttu-id="8cf5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cf5a-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf5a-103">일시 중단된 Automation 작업을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="8cf5a-104">구문</span><span class="sxs-lookup"><span data-stu-id="8cf5a-104">SYNTAX</span></span>

```
Resume-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cf5a-105">설명</span><span class="sxs-lookup"><span data-stu-id="8cf5a-105">DESCRIPTION</span></span>
<span data-ttu-id="8cf5a-106">**Resume-AzAutomationJob** cmdlet은 일시 중단된 Azure Automation 작업을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-106">The **Resume-AzAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="8cf5a-107">일시 중단된 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-107">Specify the suspended job.</span></span>
<span data-ttu-id="8cf5a-108">작업을 일시 중단하기 위해 Suspend-AzAutomationJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-108">To suspend a job, use the Suspend-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="8cf5a-109">예제</span><span class="sxs-lookup"><span data-stu-id="8cf5a-109">EXAMPLES</span></span>

### <span data-ttu-id="8cf5a-110">예제 1: 일시 중단된 작업 다시 시작</span><span class="sxs-lookup"><span data-stu-id="8cf5a-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8cf5a-111">이 명령은 지정된 ID가 있는 작업을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="8cf5a-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8cf5a-112">PARAMETERS</span></span>

### <span data-ttu-id="8cf5a-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8cf5a-113">-AutomationAccountName</span></span>
<span data-ttu-id="8cf5a-114">이 cmdlet이 작업을 다시 시작하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="8cf5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf5a-115">-DefaultProfile</span></span>
<span data-ttu-id="8cf5a-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8cf5a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cf5a-117">-Id</span><span class="sxs-lookup"><span data-stu-id="8cf5a-117">-Id</span></span>
<span data-ttu-id="8cf5a-118">이 cmdlet이 다시 시작되는 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="8cf5a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cf5a-119">-ResourceGroupName</span></span>
<span data-ttu-id="8cf5a-120">이 cmdlet이 작업을 다시 시작할 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="8cf5a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf5a-121">CommonParameters</span></span>
<span data-ttu-id="8cf5a-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf5a-123">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8cf5a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf5a-124">입력</span><span class="sxs-lookup"><span data-stu-id="8cf5a-124">INPUTS</span></span>

### <span data-ttu-id="8cf5a-125">System.Guid</span><span class="sxs-lookup"><span data-stu-id="8cf5a-125">System.Guid</span></span>

### <span data-ttu-id="8cf5a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8cf5a-126">System.String</span></span>

## <span data-ttu-id="8cf5a-127">출력</span><span class="sxs-lookup"><span data-stu-id="8cf5a-127">OUTPUTS</span></span>

### <span data-ttu-id="8cf5a-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="8cf5a-128">System.Void</span></span>

## <span data-ttu-id="8cf5a-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8cf5a-129">NOTES</span></span>

## <span data-ttu-id="8cf5a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8cf5a-130">RELATED LINKS</span></span>

[<span data-ttu-id="8cf5a-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8cf5a-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="8cf5a-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="8cf5a-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="8cf5a-133">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8cf5a-133">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="8cf5a-134">suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="8cf5a-134">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/resume-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
ms.openlocfilehash: 731a2df87ce6ad575e9aa3e10eb124e52ec1b60b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212634"
---
# <span data-ttu-id="b4911-101">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b4911-101">Resume-AzAutomationJob</span></span>

## <span data-ttu-id="b4911-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4911-102">SYNOPSIS</span></span>
<span data-ttu-id="b4911-103">일시 중단 된 자동화 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4911-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="b4911-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4911-104">SYNTAX</span></span>

```
Resume-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4911-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b4911-105">DESCRIPTION</span></span>
<span data-ttu-id="b4911-106">**AzAutomationJob** cmdlet은 일시 중단 된 Azure 자동화 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4911-106">The **Resume-AzAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="b4911-107">일시 중단 된 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4911-107">Specify the suspended job.</span></span>
<span data-ttu-id="b4911-108">작업을 일시 중단 하려면 Suspend-AzAutomationJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4911-108">To suspend a job, use the Suspend-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="b4911-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b4911-109">EXAMPLES</span></span>

### <span data-ttu-id="b4911-110">예제 1: 일시 중단 된 작업 다시 시작</span><span class="sxs-lookup"><span data-stu-id="b4911-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b4911-111">이 명령은 지정 된 ID를 가진 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4911-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="b4911-112">변수</span><span class="sxs-lookup"><span data-stu-id="b4911-112">PARAMETERS</span></span>

### <span data-ttu-id="b4911-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b4911-113">-AutomationAccountName</span></span>
<span data-ttu-id="b4911-114">이 cmdlet이 작업을 다시 시작 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4911-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="b4911-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4911-115">-DefaultProfile</span></span>
<span data-ttu-id="b4911-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b4911-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4911-117">-Id</span><span class="sxs-lookup"><span data-stu-id="b4911-117">-Id</span></span>
<span data-ttu-id="b4911-118">이 cmdlet이 다시 시작 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4911-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="b4911-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4911-119">-ResourceGroupName</span></span>
<span data-ttu-id="b4911-120">이 cmdlet이 작업을 다시 시작할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4911-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="b4911-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4911-121">CommonParameters</span></span>
<span data-ttu-id="b4911-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4911-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4911-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4911-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4911-124">입력</span><span class="sxs-lookup"><span data-stu-id="b4911-124">INPUTS</span></span>

### <span data-ttu-id="b4911-125">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="b4911-125">System.Guid</span></span>

### <span data-ttu-id="b4911-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b4911-126">System.String</span></span>

## <span data-ttu-id="b4911-127">출력</span><span class="sxs-lookup"><span data-stu-id="b4911-127">OUTPUTS</span></span>

### <span data-ttu-id="b4911-128">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="b4911-128">System.Void</span></span>

## <span data-ttu-id="b4911-129">상속자</span><span class="sxs-lookup"><span data-stu-id="b4911-129">NOTES</span></span>

## <span data-ttu-id="b4911-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4911-130">RELATED LINKS</span></span>

[<span data-ttu-id="b4911-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b4911-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="b4911-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="b4911-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="b4911-133">중지-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b4911-133">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="b4911-134">일시 중단-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b4911-134">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)



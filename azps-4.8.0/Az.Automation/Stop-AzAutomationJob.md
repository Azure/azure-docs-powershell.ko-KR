---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: 451457cf4483d9af6d8a7aca8731b95dc5c95859
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048502"
---
# <span data-ttu-id="35861-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="35861-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="35861-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35861-102">SYNOPSIS</span></span>
<span data-ttu-id="35861-103">자동화 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="35861-103">Stops an Automation job.</span></span>

## <span data-ttu-id="35861-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35861-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35861-105">설명은</span><span class="sxs-lookup"><span data-stu-id="35861-105">DESCRIPTION</span></span>
<span data-ttu-id="35861-106">**AzAutomationJob** Cmdlet은 Azure Automation 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="35861-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="35861-107">실행 중인 자동화 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35861-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="35861-108">예제의</span><span class="sxs-lookup"><span data-stu-id="35861-108">EXAMPLES</span></span>

### <span data-ttu-id="35861-109">예제 1: 작업 중지</span><span class="sxs-lookup"><span data-stu-id="35861-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="35861-110">이 명령은 지정 된 ID를 가진 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="35861-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="35861-111">변수</span><span class="sxs-lookup"><span data-stu-id="35861-111">PARAMETERS</span></span>

### <span data-ttu-id="35861-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="35861-112">-AutomationAccountName</span></span>
<span data-ttu-id="35861-113">이 cmdlet이 작업을 중지 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35861-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="35861-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35861-114">-DefaultProfile</span></span>
<span data-ttu-id="35861-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="35861-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35861-116">-Id</span><span class="sxs-lookup"><span data-stu-id="35861-116">-Id</span></span>
<span data-ttu-id="35861-117">이 cmdlet이 중지 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35861-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="35861-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35861-118">-ResourceGroupName</span></span>
<span data-ttu-id="35861-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35861-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="35861-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35861-120">CommonParameters</span></span>
<span data-ttu-id="35861-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35861-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35861-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35861-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35861-123">입력</span><span class="sxs-lookup"><span data-stu-id="35861-123">INPUTS</span></span>

### <span data-ttu-id="35861-124">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="35861-124">System.Guid</span></span>

### <span data-ttu-id="35861-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="35861-125">System.String</span></span>

## <span data-ttu-id="35861-126">출력</span><span class="sxs-lookup"><span data-stu-id="35861-126">OUTPUTS</span></span>

### <span data-ttu-id="35861-127">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="35861-127">System.Void</span></span>

## <span data-ttu-id="35861-128">상속자</span><span class="sxs-lookup"><span data-stu-id="35861-128">NOTES</span></span>

## <span data-ttu-id="35861-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35861-129">RELATED LINKS</span></span>

[<span data-ttu-id="35861-130">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="35861-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="35861-131">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="35861-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="35861-132">이력서-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="35861-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="35861-133">일시 중단-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="35861-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)



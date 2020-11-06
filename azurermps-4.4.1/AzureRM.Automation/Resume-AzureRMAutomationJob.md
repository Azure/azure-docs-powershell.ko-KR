---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
ms.openlocfilehash: 6d23fe3728b569cbb1a2aee498d560672ee75877
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531205"
---
# <span data-ttu-id="31f7b-101">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="31f7b-101">Resume-AzureRmAutomationJob</span></span>

## <span data-ttu-id="31f7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="31f7b-103">일시 중단 된 자동화 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="31f7b-103">Resumes a suspended Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31f7b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31f7b-104">SYNTAX</span></span>

```
Resume-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31f7b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="31f7b-105">DESCRIPTION</span></span>
<span data-ttu-id="31f7b-106">**AzureRmAutomationJob** cmdlet은 일시 중단 된 Azure 자동화 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="31f7b-106">The **Resume-AzureRmAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="31f7b-107">일시 중단 된 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31f7b-107">Specify the suspended job.</span></span>

<span data-ttu-id="31f7b-108">작업을 일시 중단 하려면 Suspend-AzureRmAutomationJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31f7b-108">To suspend a job, use the Suspend-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="31f7b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="31f7b-109">EXAMPLES</span></span>

### <span data-ttu-id="31f7b-110">예제 1: 일시 중단 된 작업 다시 시작</span><span class="sxs-lookup"><span data-stu-id="31f7b-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="31f7b-111">이 명령은 지정 된 ID를 가진 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="31f7b-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="31f7b-112">변수</span><span class="sxs-lookup"><span data-stu-id="31f7b-112">PARAMETERS</span></span>

### <span data-ttu-id="31f7b-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="31f7b-113">-AutomationAccountName</span></span>
<span data-ttu-id="31f7b-114">이 cmdlet이 작업을 다시 시작 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31f7b-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="31f7b-115">-Id</span><span class="sxs-lookup"><span data-stu-id="31f7b-115">-Id</span></span>
<span data-ttu-id="31f7b-116">이 cmdlet이 다시 시작 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31f7b-116">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="31f7b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f7b-117">-ResourceGroupName</span></span>
<span data-ttu-id="31f7b-118">이 cmdlet이 작업을 다시 시작할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31f7b-118">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="31f7b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f7b-119">-DefaultProfile</span></span>
<span data-ttu-id="31f7b-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31f7b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f7b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f7b-121">CommonParameters</span></span>
<span data-ttu-id="31f7b-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31f7b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f7b-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31f7b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f7b-124">입력</span><span class="sxs-lookup"><span data-stu-id="31f7b-124">INPUTS</span></span>

## <span data-ttu-id="31f7b-125">출력</span><span class="sxs-lookup"><span data-stu-id="31f7b-125">OUTPUTS</span></span>

## <span data-ttu-id="31f7b-126">상속자</span><span class="sxs-lookup"><span data-stu-id="31f7b-126">NOTES</span></span>

## <span data-ttu-id="31f7b-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31f7b-127">RELATED LINKS</span></span>

[<span data-ttu-id="31f7b-128">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="31f7b-128">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="31f7b-129">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="31f7b-129">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="31f7b-130">중지-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="31f7b-130">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="31f7b-131">일시 중단-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="31f7b-131">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)



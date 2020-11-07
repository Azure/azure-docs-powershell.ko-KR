---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
ms.openlocfilehash: cc9f402400b0290d8cf36dc38d59a45e29ce770c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710991"
---
# <span data-ttu-id="b6d84-101">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b6d84-101">Suspend-AzureRmAutomationJob</span></span>

## <span data-ttu-id="b6d84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6d84-102">SYNOPSIS</span></span>
<span data-ttu-id="b6d84-103">자동화 작업을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6d84-103">Suspends an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6d84-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b6d84-104">SYNTAX</span></span>

```
Suspend-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6d84-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b6d84-105">DESCRIPTION</span></span>
<span data-ttu-id="b6d84-106">**AzureRmAutomationJob** Cmdlet은 Azure Automation 작업을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6d84-106">The **Suspend-AzureRmAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="b6d84-107">실행 중인 자동화 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6d84-107">Specify a running Automation job.</span></span>

<span data-ttu-id="b6d84-108">일시 중단 된 작업을 다시 시작 하려면 Resume-AzureRmAutomationJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6d84-108">To resume a suspended job, use the Resume-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="b6d84-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b6d84-109">EXAMPLES</span></span>

### <span data-ttu-id="b6d84-110">예제 1: 작업 일시 중단</span><span class="sxs-lookup"><span data-stu-id="b6d84-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b6d84-111">이 명령은 지정 된 ID를 가진 작업을 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6d84-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="b6d84-112">변수</span><span class="sxs-lookup"><span data-stu-id="b6d84-112">PARAMETERS</span></span>

### <span data-ttu-id="b6d84-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b6d84-113">-AutomationAccountName</span></span>
<span data-ttu-id="b6d84-114">이 cmdlet이 작업을 일시 중단 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6d84-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="b6d84-115">-Id</span><span class="sxs-lookup"><span data-stu-id="b6d84-115">-Id</span></span>
<span data-ttu-id="b6d84-116">이 cmdlet이 일시 중단 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6d84-116">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="b6d84-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6d84-117">-ResourceGroupName</span></span>
<span data-ttu-id="b6d84-118">이 cmdlet이 일시 중단 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6d84-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="b6d84-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6d84-119">-DefaultProfile</span></span>
<span data-ttu-id="b6d84-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6d84-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6d84-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6d84-121">CommonParameters</span></span>
<span data-ttu-id="b6d84-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6d84-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6d84-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6d84-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6d84-124">입력</span><span class="sxs-lookup"><span data-stu-id="b6d84-124">INPUTS</span></span>

## <span data-ttu-id="b6d84-125">출력</span><span class="sxs-lookup"><span data-stu-id="b6d84-125">OUTPUTS</span></span>

## <span data-ttu-id="b6d84-126">상속자</span><span class="sxs-lookup"><span data-stu-id="b6d84-126">NOTES</span></span>

## <span data-ttu-id="b6d84-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6d84-127">RELATED LINKS</span></span>

[<span data-ttu-id="b6d84-128">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b6d84-128">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="b6d84-129">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="b6d84-129">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="b6d84-130">이력서-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b6d84-130">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="b6d84-131">중지-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="b6d84-131">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)



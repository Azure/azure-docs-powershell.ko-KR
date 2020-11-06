---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/stop-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
ms.openlocfilehash: 0eedf88ed078c3532eb60a00b87733937344bafa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529033"
---
# <span data-ttu-id="767ed-101">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="767ed-101">Stop-AzureRmAutomationJob</span></span>

## <span data-ttu-id="767ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="767ed-102">SYNOPSIS</span></span>
<span data-ttu-id="767ed-103">자동화 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="767ed-103">Stops an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="767ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="767ed-104">SYNTAX</span></span>

```
Stop-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="767ed-105">설명은</span><span class="sxs-lookup"><span data-stu-id="767ed-105">DESCRIPTION</span></span>
<span data-ttu-id="767ed-106">**AzureRmAutomationJob** Cmdlet은 Azure Automation 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="767ed-106">The **Stop-AzureRmAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="767ed-107">실행 중인 자동화 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="767ed-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="767ed-108">예제의</span><span class="sxs-lookup"><span data-stu-id="767ed-108">EXAMPLES</span></span>

### <span data-ttu-id="767ed-109">예제 1: 작업 중지</span><span class="sxs-lookup"><span data-stu-id="767ed-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="767ed-110">이 명령은 지정 된 ID를 가진 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="767ed-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="767ed-111">변수</span><span class="sxs-lookup"><span data-stu-id="767ed-111">PARAMETERS</span></span>

### <span data-ttu-id="767ed-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="767ed-112">-AutomationAccountName</span></span>
<span data-ttu-id="767ed-113">이 cmdlet이 작업을 중지 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="767ed-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="767ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="767ed-114">-DefaultProfile</span></span>
<span data-ttu-id="767ed-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="767ed-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="767ed-116">-Id</span><span class="sxs-lookup"><span data-stu-id="767ed-116">-Id</span></span>
<span data-ttu-id="767ed-117">이 cmdlet이 중지 하는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="767ed-117">Specifies the ID of a job that this cmdlet stops.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="767ed-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="767ed-118">-ResourceGroupName</span></span>
<span data-ttu-id="767ed-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="767ed-119">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="767ed-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="767ed-120">CommonParameters</span></span>
<span data-ttu-id="767ed-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="767ed-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="767ed-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="767ed-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="767ed-123">입력</span><span class="sxs-lookup"><span data-stu-id="767ed-123">INPUTS</span></span>

### <span data-ttu-id="767ed-124">않아야</span><span class="sxs-lookup"><span data-stu-id="767ed-124">None</span></span>
<span data-ttu-id="767ed-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="767ed-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="767ed-126">출력</span><span class="sxs-lookup"><span data-stu-id="767ed-126">OUTPUTS</span></span>

## <span data-ttu-id="767ed-127">상속자</span><span class="sxs-lookup"><span data-stu-id="767ed-127">NOTES</span></span>

## <span data-ttu-id="767ed-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="767ed-128">RELATED LINKS</span></span>

[<span data-ttu-id="767ed-129">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="767ed-129">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="767ed-130">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="767ed-130">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="767ed-131">이력서-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="767ed-131">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="767ed-132">일시 중단-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="767ed-132">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)



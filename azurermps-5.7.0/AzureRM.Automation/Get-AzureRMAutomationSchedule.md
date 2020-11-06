---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationSchedule.md
ms.openlocfilehash: 2b35281cd276be9149f2d4c4e17cb38f48eadc25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535351"
---
# <span data-ttu-id="ff7b2-101">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ff7b2-101">Get-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="ff7b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff7b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ff7b2-103">자동화 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ff7b2-103">Gets an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff7b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff7b2-104">SYNTAX</span></span>

### <span data-ttu-id="ff7b2-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="ff7b2-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff7b2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ff7b2-106">ByName</span></span>
```
Get-AzureRmAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff7b2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ff7b2-107">DESCRIPTION</span></span>
<span data-ttu-id="ff7b2-108">**Get-AzureRmAutomationSchedule** Cmdlet은 Azure Automation 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ff7b2-108">The **Get-AzureRmAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="ff7b2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ff7b2-109">EXAMPLES</span></span>

### <span data-ttu-id="ff7b2-110">예제 1: 일정 가져오기</span><span class="sxs-lookup"><span data-stu-id="ff7b2-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ff7b2-111">이 명령은 DailySchedule08 라는 일정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ff7b2-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="ff7b2-112">변수</span><span class="sxs-lookup"><span data-stu-id="ff7b2-112">PARAMETERS</span></span>

### <span data-ttu-id="ff7b2-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ff7b2-113">-AutomationAccountName</span></span>
<span data-ttu-id="ff7b2-114">이 cmdlet에서 일정을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff7b2-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="ff7b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff7b2-115">-DefaultProfile</span></span>
<span data-ttu-id="ff7b2-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ff7b2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff7b2-117">-이름</span><span class="sxs-lookup"><span data-stu-id="ff7b2-117">-Name</span></span>
<span data-ttu-id="ff7b2-118">이 cmdlet이 가져오는 일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff7b2-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7b2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff7b2-119">-ResourceGroupName</span></span>
<span data-ttu-id="ff7b2-120">이 cmdlet에서 일정을 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff7b2-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="ff7b2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff7b2-121">CommonParameters</span></span>
<span data-ttu-id="ff7b2-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff7b2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff7b2-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff7b2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff7b2-124">입력</span><span class="sxs-lookup"><span data-stu-id="ff7b2-124">INPUTS</span></span>

### <span data-ttu-id="ff7b2-125">않아야</span><span class="sxs-lookup"><span data-stu-id="ff7b2-125">None</span></span>
<span data-ttu-id="ff7b2-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff7b2-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ff7b2-127">출력</span><span class="sxs-lookup"><span data-stu-id="ff7b2-127">OUTPUTS</span></span>

### <span data-ttu-id="ff7b2-128">Microsoft Azure. 명령. 일정</span><span class="sxs-lookup"><span data-stu-id="ff7b2-128">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="ff7b2-129">상속자</span><span class="sxs-lookup"><span data-stu-id="ff7b2-129">NOTES</span></span>

## <span data-ttu-id="ff7b2-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff7b2-130">RELATED LINKS</span></span>

[<span data-ttu-id="ff7b2-131">새로운 AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ff7b2-131">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="ff7b2-132">제거-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ff7b2-132">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="ff7b2-133">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ff7b2-133">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)



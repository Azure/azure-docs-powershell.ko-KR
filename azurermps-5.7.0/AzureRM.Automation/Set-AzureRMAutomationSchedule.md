---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationSchedule.md
ms.openlocfilehash: b311554fa5aeeae67829055506b85766fd6f9670
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531785"
---
# <span data-ttu-id="e4f62-101">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e4f62-101">Set-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="e4f62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4f62-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f62-103">자동화 일정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f62-103">Modifies an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4f62-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e4f62-104">SYNTAX</span></span>

```
Set-AzureRmAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4f62-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e4f62-105">DESCRIPTION</span></span>
<span data-ttu-id="e4f62-106">**Set-AzureRmAutomationSchedule** Cmdlet은 Azure Automation의 일정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f62-106">The **Set-AzureRmAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="e4f62-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e4f62-107">EXAMPLES</span></span>

### <span data-ttu-id="e4f62-108">예제 1: 일정 수정</span><span class="sxs-lookup"><span data-stu-id="e4f62-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e4f62-109">이 명령은 Schedule01 이라는 일정에 대 한 설명을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f62-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="e4f62-110">변수</span><span class="sxs-lookup"><span data-stu-id="e4f62-110">PARAMETERS</span></span>

### <span data-ttu-id="e4f62-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e4f62-111">-AutomationAccountName</span></span>
<span data-ttu-id="e4f62-112">이 cmdlet이 일정을 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f62-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="e4f62-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4f62-113">-DefaultProfile</span></span>
<span data-ttu-id="e4f62-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e4f62-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4f62-115">-설명</span><span class="sxs-lookup"><span data-stu-id="e4f62-115">-Description</span></span>
<span data-ttu-id="e4f62-116">일정에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f62-116">Specifies a description for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f62-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="e4f62-117">-IsEnabled</span></span>
<span data-ttu-id="e4f62-118">이 cmdlet이 일정을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f62-118">Specifies whether this cmdlet enables the schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f62-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e4f62-119">-Name</span></span>
<span data-ttu-id="e4f62-120">이 cmdlet이 수정 하는 일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f62-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f62-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4f62-121">-ResourceGroupName</span></span>
<span data-ttu-id="e4f62-122">이 cmdlet이 일정을 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f62-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="e4f62-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f62-123">CommonParameters</span></span>
<span data-ttu-id="e4f62-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4f62-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f62-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4f62-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f62-126">입력</span><span class="sxs-lookup"><span data-stu-id="e4f62-126">INPUTS</span></span>

### <span data-ttu-id="e4f62-127">않아야</span><span class="sxs-lookup"><span data-stu-id="e4f62-127">None</span></span>
<span data-ttu-id="e4f62-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4f62-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4f62-129">출력</span><span class="sxs-lookup"><span data-stu-id="e4f62-129">OUTPUTS</span></span>

### <span data-ttu-id="e4f62-130">Microsoft Azure. 명령. 일정</span><span class="sxs-lookup"><span data-stu-id="e4f62-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="e4f62-131">상속자</span><span class="sxs-lookup"><span data-stu-id="e4f62-131">NOTES</span></span>

## <span data-ttu-id="e4f62-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4f62-132">RELATED LINKS</span></span>

[<span data-ttu-id="e4f62-133">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e4f62-133">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="e4f62-134">새로운 AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e4f62-134">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="e4f62-135">제거-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e4f62-135">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)



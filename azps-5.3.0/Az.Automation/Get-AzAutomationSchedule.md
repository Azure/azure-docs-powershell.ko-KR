---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a07208db434a43730b75542bb0f8959ae68423d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494319"
---
# <span data-ttu-id="b2b25-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="b2b25-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="b2b25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2b25-102">SYNOPSIS</span></span>
<span data-ttu-id="b2b25-103">Automation 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b2b25-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="b2b25-104">구문</span><span class="sxs-lookup"><span data-stu-id="b2b25-104">SYNTAX</span></span>

### <span data-ttu-id="b2b25-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="b2b25-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2b25-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b2b25-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2b25-107">설명</span><span class="sxs-lookup"><span data-stu-id="b2b25-107">DESCRIPTION</span></span>
<span data-ttu-id="b2b25-108">**Get-AzAutomationSchedule** cmdlet은 Azure Automation 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b2b25-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="b2b25-109">예제</span><span class="sxs-lookup"><span data-stu-id="b2b25-109">EXAMPLES</span></span>

### <span data-ttu-id="b2b25-110">예제 1: 일정 얻기</span><span class="sxs-lookup"><span data-stu-id="b2b25-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b2b25-111">이 명령은 DailySchedule08이라는 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b2b25-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="b2b25-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2b25-112">PARAMETERS</span></span>

### <span data-ttu-id="b2b25-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b2b25-113">-AutomationAccountName</span></span>
<span data-ttu-id="b2b25-114">이 cmdlet이 일정을 받을 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2b25-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="b2b25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2b25-115">-DefaultProfile</span></span>
<span data-ttu-id="b2b25-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b2b25-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2b25-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b2b25-117">-Name</span></span>
<span data-ttu-id="b2b25-118">이 cmdlet이 얻을 일정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2b25-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2b25-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2b25-119">-ResourceGroupName</span></span>
<span data-ttu-id="b2b25-120">이 cmdlet이 일정을 얻을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2b25-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="b2b25-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2b25-121">CommonParameters</span></span>
<span data-ttu-id="b2b25-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b2b25-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2b25-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b2b25-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2b25-124">입력</span><span class="sxs-lookup"><span data-stu-id="b2b25-124">INPUTS</span></span>

### <span data-ttu-id="b2b25-125">System.String</span><span class="sxs-lookup"><span data-stu-id="b2b25-125">System.String</span></span>

## <span data-ttu-id="b2b25-126">출력</span><span class="sxs-lookup"><span data-stu-id="b2b25-126">OUTPUTS</span></span>

### <span data-ttu-id="b2b25-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="b2b25-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="b2b25-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b2b25-128">NOTES</span></span>

## <span data-ttu-id="b2b25-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2b25-129">RELATED LINKS</span></span>

[<span data-ttu-id="b2b25-130">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="b2b25-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="b2b25-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="b2b25-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="b2b25-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="b2b25-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)



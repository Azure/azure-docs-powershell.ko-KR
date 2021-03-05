---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2908890B-7A46-41B7-931F-AE94638D1EDF
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSchedule.md
ms.openlocfilehash: a32b86ce308f18537ec1acda62c2694e7b621d5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014219"
---
# <span data-ttu-id="ff487-101">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ff487-101">Get-AzAutomationSchedule</span></span>

## <span data-ttu-id="ff487-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff487-102">SYNOPSIS</span></span>
<span data-ttu-id="ff487-103">Automation 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ff487-103">Gets an Automation schedule.</span></span>

## <span data-ttu-id="ff487-104">구문</span><span class="sxs-lookup"><span data-stu-id="ff487-104">SYNTAX</span></span>

### <span data-ttu-id="ff487-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="ff487-105">ByAll (Default)</span></span>
```
Get-AzAutomationSchedule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff487-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ff487-106">ByName</span></span>
```
Get-AzAutomationSchedule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff487-107">설명</span><span class="sxs-lookup"><span data-stu-id="ff487-107">DESCRIPTION</span></span>
<span data-ttu-id="ff487-108">**Get-AzAutomationSchedule** cmdlet은 Azure Automation 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ff487-108">The **Get-AzAutomationSchedule** cmdlet gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="ff487-109">예제</span><span class="sxs-lookup"><span data-stu-id="ff487-109">EXAMPLES</span></span>

### <span data-ttu-id="ff487-110">예제 1: 일정을 얻다</span><span class="sxs-lookup"><span data-stu-id="ff487-110">Example 1: Get a schedule</span></span>
```
PS C:\>Get-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ff487-111">이 명령은 DailySchedule08이라는 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ff487-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="ff487-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ff487-112">PARAMETERS</span></span>

### <span data-ttu-id="ff487-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ff487-113">-AutomationAccountName</span></span>
<span data-ttu-id="ff487-114">이 cmdlet에서 일정을 얻을 수 있는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff487-114">Specifies the name of an Automation account for which this cmdlet get a schedule.</span></span>

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

### <span data-ttu-id="ff487-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff487-115">-DefaultProfile</span></span>
<span data-ttu-id="ff487-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ff487-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff487-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ff487-117">-Name</span></span>
<span data-ttu-id="ff487-118">이 cmdlet이 도착하는 일정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff487-118">Specifies the name of a schedule that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ff487-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff487-119">-ResourceGroupName</span></span>
<span data-ttu-id="ff487-120">이 cmdlet에서 일정을 얻을 수 있는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ff487-120">Specifies the name of a resource group for which this cmdlet gets a schedule.</span></span>

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

### <span data-ttu-id="ff487-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff487-121">CommonParameters</span></span>
<span data-ttu-id="ff487-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ff487-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff487-123">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ff487-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff487-124">입력</span><span class="sxs-lookup"><span data-stu-id="ff487-124">INPUTS</span></span>

### <span data-ttu-id="ff487-125">System.String</span><span class="sxs-lookup"><span data-stu-id="ff487-125">System.String</span></span>

## <span data-ttu-id="ff487-126">출력</span><span class="sxs-lookup"><span data-stu-id="ff487-126">OUTPUTS</span></span>

### <span data-ttu-id="ff487-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="ff487-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="ff487-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ff487-128">NOTES</span></span>

## <span data-ttu-id="ff487-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff487-129">RELATED LINKS</span></span>

[<span data-ttu-id="ff487-130">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ff487-130">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="ff487-131">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ff487-131">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="ff487-132">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ff487-132">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)



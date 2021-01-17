---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
ms.openlocfilehash: 3de9658011bd781d98e16c1ba996a6951c548975
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373045"
---
# <span data-ttu-id="aaab1-101">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="aaab1-101">Set-AzAutomationSchedule</span></span>

## <span data-ttu-id="aaab1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaab1-102">SYNOPSIS</span></span>
<span data-ttu-id="aaab1-103">Automation 일정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaab1-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="aaab1-104">구문</span><span class="sxs-lookup"><span data-stu-id="aaab1-104">SYNTAX</span></span>

```
Set-AzAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aaab1-105">설명</span><span class="sxs-lookup"><span data-stu-id="aaab1-105">DESCRIPTION</span></span>
<span data-ttu-id="aaab1-106">**Set-AzAutomationSchedule** cmdlet은 Azure Automation에서 일정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaab1-106">The **Set-AzAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="aaab1-107">예제</span><span class="sxs-lookup"><span data-stu-id="aaab1-107">EXAMPLES</span></span>

### <span data-ttu-id="aaab1-108">예제 1: 일정 수정</span><span class="sxs-lookup"><span data-stu-id="aaab1-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="aaab1-109">이 명령은 Schedule01이라는 일정에 대한 설명을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaab1-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="aaab1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaab1-110">PARAMETERS</span></span>

### <span data-ttu-id="aaab1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aaab1-111">-AutomationAccountName</span></span>
<span data-ttu-id="aaab1-112">이 cmdlet이 일정을 수정하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaab1-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="aaab1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaab1-113">-DefaultProfile</span></span>
<span data-ttu-id="aaab1-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="aaab1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aaab1-115">-Description</span><span class="sxs-lookup"><span data-stu-id="aaab1-115">-Description</span></span>
<span data-ttu-id="aaab1-116">일정에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaab1-116">Specifies a description for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaab1-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="aaab1-117">-IsEnabled</span></span>
<span data-ttu-id="aaab1-118">이 cmdlet이 일정을 가능하게 하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaab1-118">Specifies whether this cmdlet enables the schedule.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaab1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="aaab1-119">-Name</span></span>
<span data-ttu-id="aaab1-120">이 cmdlet이 수정하는 일정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaab1-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaab1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaab1-121">-ResourceGroupName</span></span>
<span data-ttu-id="aaab1-122">이 cmdlet이 일정을 수정하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaab1-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="aaab1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaab1-123">CommonParameters</span></span>
<span data-ttu-id="aaab1-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aaab1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaab1-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="aaab1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaab1-126">입력</span><span class="sxs-lookup"><span data-stu-id="aaab1-126">INPUTS</span></span>

### <span data-ttu-id="aaab1-127">System.String</span><span class="sxs-lookup"><span data-stu-id="aaab1-127">System.String</span></span>

### <span data-ttu-id="aaab1-128">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="aaab1-128">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="aaab1-129">출력</span><span class="sxs-lookup"><span data-stu-id="aaab1-129">OUTPUTS</span></span>

### <span data-ttu-id="aaab1-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="aaab1-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="aaab1-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aaab1-131">NOTES</span></span>

## <span data-ttu-id="aaab1-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aaab1-132">RELATED LINKS</span></span>

[<span data-ttu-id="aaab1-133">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="aaab1-133">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="aaab1-134">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="aaab1-134">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="aaab1-135">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="aaab1-135">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)



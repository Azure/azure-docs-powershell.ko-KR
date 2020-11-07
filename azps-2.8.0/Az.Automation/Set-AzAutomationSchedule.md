---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6429C564-1995-4D9B-BF9B-963B4F5FB3BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationSchedule.md
ms.openlocfilehash: c5f7348d59b18a3e0cedfcf52c22c4328c28944a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697726"
---
# <span data-ttu-id="70e1d-101">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="70e1d-101">Set-AzAutomationSchedule</span></span>

## <span data-ttu-id="70e1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70e1d-102">SYNOPSIS</span></span>
<span data-ttu-id="70e1d-103">자동화 일정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e1d-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="70e1d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70e1d-104">SYNTAX</span></span>

```
Set-AzAutomationSchedule [-Name] <String> [-IsEnabled <Boolean>] [-Description <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70e1d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="70e1d-105">DESCRIPTION</span></span>
<span data-ttu-id="70e1d-106">**Set-AzAutomationSchedule** Cmdlet은 Azure Automation의 일정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e1d-106">The **Set-AzAutomationSchedule** cmdlet modifies a schedule in Azure Automation.</span></span>

## <span data-ttu-id="70e1d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="70e1d-107">EXAMPLES</span></span>

### <span data-ttu-id="70e1d-108">예제 1: 일정 수정</span><span class="sxs-lookup"><span data-stu-id="70e1d-108">Example 1: Modify a schedule</span></span>
```
PS C:\>Set-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="70e1d-109">이 명령은 Schedule01 이라는 일정에 대 한 설명을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e1d-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="70e1d-110">변수</span><span class="sxs-lookup"><span data-stu-id="70e1d-110">PARAMETERS</span></span>

### <span data-ttu-id="70e1d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="70e1d-111">-AutomationAccountName</span></span>
<span data-ttu-id="70e1d-112">이 cmdlet이 일정을 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e1d-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="70e1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70e1d-113">-DefaultProfile</span></span>
<span data-ttu-id="70e1d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="70e1d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70e1d-115">-설명</span><span class="sxs-lookup"><span data-stu-id="70e1d-115">-Description</span></span>
<span data-ttu-id="70e1d-116">일정에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e1d-116">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="70e1d-117">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="70e1d-117">-IsEnabled</span></span>
<span data-ttu-id="70e1d-118">이 cmdlet이 일정을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e1d-118">Specifies whether this cmdlet enables the schedule.</span></span>

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

### <span data-ttu-id="70e1d-119">-이름</span><span class="sxs-lookup"><span data-stu-id="70e1d-119">-Name</span></span>
<span data-ttu-id="70e1d-120">이 cmdlet이 수정 하는 일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e1d-120">Specifies the name for the schedule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="70e1d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70e1d-121">-ResourceGroupName</span></span>
<span data-ttu-id="70e1d-122">이 cmdlet이 일정을 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e1d-122">Specifies the name of a resource group for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="70e1d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70e1d-123">CommonParameters</span></span>
<span data-ttu-id="70e1d-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70e1d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70e1d-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70e1d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70e1d-126">입력</span><span class="sxs-lookup"><span data-stu-id="70e1d-126">INPUTS</span></span>

### <span data-ttu-id="70e1d-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="70e1d-127">System.String</span></span>

### <span data-ttu-id="70e1d-128">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="70e1d-128">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="70e1d-129">출력</span><span class="sxs-lookup"><span data-stu-id="70e1d-129">OUTPUTS</span></span>

### <span data-ttu-id="70e1d-130">Microsoft Azure. 명령. 일정</span><span class="sxs-lookup"><span data-stu-id="70e1d-130">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="70e1d-131">상속자</span><span class="sxs-lookup"><span data-stu-id="70e1d-131">NOTES</span></span>

## <span data-ttu-id="70e1d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70e1d-132">RELATED LINKS</span></span>

[<span data-ttu-id="70e1d-133">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="70e1d-133">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="70e1d-134">새로운 AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="70e1d-134">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="70e1d-135">제거-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="70e1d-135">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)


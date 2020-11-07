---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
ms.openlocfilehash: d56b631f106ef4984a81a8911af26288f720cac7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697756"
---
# <span data-ttu-id="2bed8-101">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2bed8-101">Remove-AzAutomationSchedule</span></span>

## <span data-ttu-id="2bed8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bed8-102">SYNOPSIS</span></span>
<span data-ttu-id="2bed8-103">Automation 일정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bed8-103">Deletes an Automation schedule.</span></span>

## <span data-ttu-id="2bed8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2bed8-104">SYNTAX</span></span>

```
Remove-AzAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2bed8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2bed8-105">DESCRIPTION</span></span>
<span data-ttu-id="2bed8-106">**AzAutomationSchedule** Cmdlet은 Azure 자동화에서 일정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bed8-106">The **Remove-AzAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="2bed8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2bed8-107">EXAMPLES</span></span>

### <span data-ttu-id="2bed8-108">예제 1: 일정 제거</span><span class="sxs-lookup"><span data-stu-id="2bed8-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2bed8-109">이 명령은 리소스 그룹 ResourceGroup01의 automation 계정 Contoso17에서 Schedule01 이라는 일정을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bed8-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="2bed8-110">변수</span><span class="sxs-lookup"><span data-stu-id="2bed8-110">PARAMETERS</span></span>

### <span data-ttu-id="2bed8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2bed8-111">-AutomationAccountName</span></span>
<span data-ttu-id="2bed8-112">이 cmdlet이 일정을 제거 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bed8-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="2bed8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bed8-113">-DefaultProfile</span></span>
<span data-ttu-id="2bed8-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2bed8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2bed8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2bed8-115">-Force</span></span>
<span data-ttu-id="2bed8-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="2bed8-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bed8-117">-이름</span><span class="sxs-lookup"><span data-stu-id="2bed8-117">-Name</span></span>
<span data-ttu-id="2bed8-118">이 cmdlet이 제거 하는 일정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bed8-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2bed8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bed8-119">-ResourceGroupName</span></span>
<span data-ttu-id="2bed8-120">이 cmdlet이 일정을 제거할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bed8-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="2bed8-121">-확인</span><span class="sxs-lookup"><span data-stu-id="2bed8-121">-Confirm</span></span>
<span data-ttu-id="2bed8-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bed8-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bed8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bed8-123">-WhatIf</span></span>
<span data-ttu-id="2bed8-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2bed8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bed8-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2bed8-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bed8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bed8-126">CommonParameters</span></span>
<span data-ttu-id="2bed8-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bed8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bed8-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bed8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bed8-129">입력</span><span class="sxs-lookup"><span data-stu-id="2bed8-129">INPUTS</span></span>

### <span data-ttu-id="2bed8-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2bed8-130">System.String</span></span>

## <span data-ttu-id="2bed8-131">출력</span><span class="sxs-lookup"><span data-stu-id="2bed8-131">OUTPUTS</span></span>

### <span data-ttu-id="2bed8-132">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="2bed8-132">System.Void</span></span>

## <span data-ttu-id="2bed8-133">상속자</span><span class="sxs-lookup"><span data-stu-id="2bed8-133">NOTES</span></span>

## <span data-ttu-id="2bed8-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2bed8-134">RELATED LINKS</span></span>

[<span data-ttu-id="2bed8-135">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2bed8-135">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="2bed8-136">새로운 AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2bed8-136">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="2bed8-137">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="2bed8-137">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)



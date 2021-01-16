---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: d3f76fe1e1c482c8d2913266e9c40dc5b41c62f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373388"
---
# <span data-ttu-id="59d87-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="59d87-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="59d87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59d87-102">SYNOPSIS</span></span>
<span data-ttu-id="59d87-103">Automation 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="59d87-103">Removes an Automation account.</span></span>

## <span data-ttu-id="59d87-104">구문</span><span class="sxs-lookup"><span data-stu-id="59d87-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59d87-105">설명</span><span class="sxs-lookup"><span data-stu-id="59d87-105">DESCRIPTION</span></span>
<span data-ttu-id="59d87-106">**Remove-AzAutomationAccount** cmdlet은 리소스 그룹에서 Azure Automation 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="59d87-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="59d87-107">Automation 계정에 대한 자세한 내용은 다음 cmdlet을 New-AzAutomationAccount 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="59d87-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="59d87-108">예제</span><span class="sxs-lookup"><span data-stu-id="59d87-108">EXAMPLES</span></span>

### <span data-ttu-id="59d87-109">예제 1: 자동화 계정 제거</span><span class="sxs-lookup"><span data-stu-id="59d87-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="59d87-110">이 명령은 사용자 유효성 검사를 요청하지 않고 ContosoAutomationAccount라는 자동화 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="59d87-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="59d87-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59d87-111">PARAMETERS</span></span>

### <span data-ttu-id="59d87-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d87-112">-DefaultProfile</span></span>
<span data-ttu-id="59d87-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="59d87-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59d87-114">-Force</span><span class="sxs-lookup"><span data-stu-id="59d87-114">-Force</span></span>
<span data-ttu-id="59d87-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="59d87-115">ps_force</span></span>

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

### <span data-ttu-id="59d87-116">-Name</span><span class="sxs-lookup"><span data-stu-id="59d87-116">-Name</span></span>
<span data-ttu-id="59d87-117">이 cmdlet이 제거하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="59d87-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d87-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59d87-118">-ResourceGroupName</span></span>
<span data-ttu-id="59d87-119">이 cmdlet이 Automation 계정을 제거하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="59d87-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="59d87-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59d87-120">-Confirm</span></span>
<span data-ttu-id="59d87-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="59d87-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59d87-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59d87-122">-WhatIf</span></span>
<span data-ttu-id="59d87-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="59d87-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59d87-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59d87-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59d87-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d87-125">CommonParameters</span></span>
<span data-ttu-id="59d87-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="59d87-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d87-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="59d87-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d87-128">입력</span><span class="sxs-lookup"><span data-stu-id="59d87-128">INPUTS</span></span>

### <span data-ttu-id="59d87-129">System.String</span><span class="sxs-lookup"><span data-stu-id="59d87-129">System.String</span></span>

## <span data-ttu-id="59d87-130">출력</span><span class="sxs-lookup"><span data-stu-id="59d87-130">OUTPUTS</span></span>

### <span data-ttu-id="59d87-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="59d87-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="59d87-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="59d87-132">NOTES</span></span>

## <span data-ttu-id="59d87-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59d87-133">RELATED LINKS</span></span>

[<span data-ttu-id="59d87-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="59d87-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="59d87-135">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="59d87-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="59d87-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="59d87-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)



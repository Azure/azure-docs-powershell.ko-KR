---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: 49b4a02210105529dff2aae2b895d4059ced97f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009995"
---
# <span data-ttu-id="f15b2-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f15b2-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="f15b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f15b2-102">SYNOPSIS</span></span>
<span data-ttu-id="f15b2-103">Automation 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f15b2-103">Removes an Automation account.</span></span>

## <span data-ttu-id="f15b2-104">구문</span><span class="sxs-lookup"><span data-stu-id="f15b2-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f15b2-105">설명</span><span class="sxs-lookup"><span data-stu-id="f15b2-105">DESCRIPTION</span></span>
<span data-ttu-id="f15b2-106">**Remove-AzAutomationAccount** cmdlet은 리소스 그룹에서 Azure Automation 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f15b2-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="f15b2-107">Automation 계정에 대한 자세한 내용은 New-AzAutomationAccount cmdlet을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f15b2-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="f15b2-108">예제</span><span class="sxs-lookup"><span data-stu-id="f15b2-108">EXAMPLES</span></span>

### <span data-ttu-id="f15b2-109">예제 1: 자동화 계정 제거</span><span class="sxs-lookup"><span data-stu-id="f15b2-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f15b2-110">이 명령은 사용자 유효성 검사를 요청하지 않고 ContosoAutomationAccount라는 자동화 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f15b2-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="f15b2-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f15b2-111">PARAMETERS</span></span>

### <span data-ttu-id="f15b2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f15b2-112">-DefaultProfile</span></span>
<span data-ttu-id="f15b2-113">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f15b2-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f15b2-114">-Force</span><span class="sxs-lookup"><span data-stu-id="f15b2-114">-Force</span></span>
<span data-ttu-id="f15b2-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="f15b2-115">ps_force</span></span>

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

### <span data-ttu-id="f15b2-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f15b2-116">-Name</span></span>
<span data-ttu-id="f15b2-117">이 cmdlet이 제거한 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f15b2-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f15b2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f15b2-118">-ResourceGroupName</span></span>
<span data-ttu-id="f15b2-119">이 cmdlet에서 Automation 계정을 제거하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f15b2-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="f15b2-120">-확인</span><span class="sxs-lookup"><span data-stu-id="f15b2-120">-Confirm</span></span>
<span data-ttu-id="f15b2-121">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f15b2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f15b2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f15b2-122">-WhatIf</span></span>
<span data-ttu-id="f15b2-123">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f15b2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f15b2-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f15b2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f15b2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f15b2-125">CommonParameters</span></span>
<span data-ttu-id="f15b2-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f15b2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f15b2-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f15b2-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f15b2-128">입력</span><span class="sxs-lookup"><span data-stu-id="f15b2-128">INPUTS</span></span>

### <span data-ttu-id="f15b2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f15b2-129">System.String</span></span>

## <span data-ttu-id="f15b2-130">출력</span><span class="sxs-lookup"><span data-stu-id="f15b2-130">OUTPUTS</span></span>

### <span data-ttu-id="f15b2-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f15b2-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="f15b2-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f15b2-132">NOTES</span></span>

## <span data-ttu-id="f15b2-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f15b2-133">RELATED LINKS</span></span>

[<span data-ttu-id="f15b2-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f15b2-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="f15b2-135">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f15b2-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="f15b2-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="f15b2-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)



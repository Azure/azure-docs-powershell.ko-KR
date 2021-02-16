---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: edb55424b16c0cdb6636f715ce6755a317e6f396
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199617"
---
# <span data-ttu-id="98631-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="98631-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="98631-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98631-102">SYNOPSIS</span></span>
<span data-ttu-id="98631-103">Automation 변수를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="98631-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="98631-104">구문</span><span class="sxs-lookup"><span data-stu-id="98631-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98631-105">설명</span><span class="sxs-lookup"><span data-stu-id="98631-105">DESCRIPTION</span></span>
<span data-ttu-id="98631-106">**Remove-AzAutomationVariable** cmdlet은 Azure Automation에서 변수를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="98631-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="98631-107">예제</span><span class="sxs-lookup"><span data-stu-id="98631-107">EXAMPLES</span></span>

### <span data-ttu-id="98631-108">예제 1: 변수 제거</span><span class="sxs-lookup"><span data-stu-id="98631-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="98631-109">이 명령은 Contoso17이라는 Automation 계정에서 StringVariable22라는 변수를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="98631-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="98631-110">이 명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="98631-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="98631-111">따라서 확인을 묻는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98631-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="98631-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98631-112">PARAMETERS</span></span>

### <span data-ttu-id="98631-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="98631-113">-AutomationAccountName</span></span>
<span data-ttu-id="98631-114">이 cmdlet이 삭제하는 변수를 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="98631-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="98631-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98631-115">-DefaultProfile</span></span>
<span data-ttu-id="98631-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="98631-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98631-117">-Name</span><span class="sxs-lookup"><span data-stu-id="98631-117">-Name</span></span>
<span data-ttu-id="98631-118">이 cmdlet이 삭제하는 변수의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="98631-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="98631-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98631-119">-ResourceGroupName</span></span>
<span data-ttu-id="98631-120">이 cmdlet이 변수를 삭제하는 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="98631-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="98631-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98631-121">-Confirm</span></span>
<span data-ttu-id="98631-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="98631-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98631-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98631-123">-WhatIf</span></span>
<span data-ttu-id="98631-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="98631-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98631-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98631-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98631-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98631-126">CommonParameters</span></span>
<span data-ttu-id="98631-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="98631-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98631-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="98631-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98631-129">입력</span><span class="sxs-lookup"><span data-stu-id="98631-129">INPUTS</span></span>

### <span data-ttu-id="98631-130">System.String</span><span class="sxs-lookup"><span data-stu-id="98631-130">System.String</span></span>

## <span data-ttu-id="98631-131">출력</span><span class="sxs-lookup"><span data-stu-id="98631-131">OUTPUTS</span></span>

### <span data-ttu-id="98631-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="98631-132">System.Void</span></span>

## <span data-ttu-id="98631-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="98631-133">NOTES</span></span>

## <span data-ttu-id="98631-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98631-134">RELATED LINKS</span></span>

[<span data-ttu-id="98631-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="98631-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="98631-136">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="98631-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="98631-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="98631-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)



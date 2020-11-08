---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: d6ce3a737063763d77ed408072d275c52ee5884c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044925"
---
# <span data-ttu-id="201e9-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="201e9-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="201e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="201e9-102">SYNOPSIS</span></span>
<span data-ttu-id="201e9-103">Runbook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="201e9-103">Removes a runbook.</span></span>

## <span data-ttu-id="201e9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="201e9-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="201e9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="201e9-105">DESCRIPTION</span></span>
<span data-ttu-id="201e9-106">**AzAutomationRunbook** Cmdlet은 Azure 자동화에서 runbook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="201e9-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="201e9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="201e9-107">EXAMPLES</span></span>

### <span data-ttu-id="201e9-108">예제 1: runbook 제거</span><span class="sxs-lookup"><span data-stu-id="201e9-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="201e9-109">이 명령은 Contoso17 이라는 Azure Automation 계정에서 Runbook03 라는 runbook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="201e9-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="201e9-110">변수</span><span class="sxs-lookup"><span data-stu-id="201e9-110">PARAMETERS</span></span>

### <span data-ttu-id="201e9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="201e9-111">-AutomationAccountName</span></span>
<span data-ttu-id="201e9-112">이 cmdlet이 runbook을 제거 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="201e9-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="201e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="201e9-113">-DefaultProfile</span></span>
<span data-ttu-id="201e9-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="201e9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="201e9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="201e9-115">-Force</span></span>
<span data-ttu-id="201e9-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="201e9-116">ps_force</span></span>

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

### <span data-ttu-id="201e9-117">-이름</span><span class="sxs-lookup"><span data-stu-id="201e9-117">-Name</span></span>
<span data-ttu-id="201e9-118">이 cmdlet이 제거 하는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="201e9-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="201e9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="201e9-119">-ResourceGroupName</span></span>
<span data-ttu-id="201e9-120">이 cmdlet이 runbook을 게시할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="201e9-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="201e9-121">-확인</span><span class="sxs-lookup"><span data-stu-id="201e9-121">-Confirm</span></span>
<span data-ttu-id="201e9-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="201e9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="201e9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="201e9-123">-WhatIf</span></span>
<span data-ttu-id="201e9-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="201e9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="201e9-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="201e9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="201e9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="201e9-126">CommonParameters</span></span>
<span data-ttu-id="201e9-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="201e9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="201e9-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="201e9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="201e9-129">입력</span><span class="sxs-lookup"><span data-stu-id="201e9-129">INPUTS</span></span>

### <span data-ttu-id="201e9-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="201e9-130">System.String</span></span>

## <span data-ttu-id="201e9-131">출력</span><span class="sxs-lookup"><span data-stu-id="201e9-131">OUTPUTS</span></span>

### <span data-ttu-id="201e9-132">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="201e9-132">System.Void</span></span>

## <span data-ttu-id="201e9-133">상속자</span><span class="sxs-lookup"><span data-stu-id="201e9-133">NOTES</span></span>

## <span data-ttu-id="201e9-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="201e9-134">RELATED LINKS</span></span>

[<span data-ttu-id="201e9-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="201e9-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="201e9-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="201e9-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="201e9-137">가져오기-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="201e9-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="201e9-138">새로운 AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="201e9-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="201e9-139">새로운 AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="201e9-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="201e9-140">게시-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="201e9-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="201e9-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="201e9-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="201e9-142">시작-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="201e9-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


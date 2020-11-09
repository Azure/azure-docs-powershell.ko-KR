---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: edb55424b16c0cdb6636f715ce6755a317e6f396
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309718"
---
# <span data-ttu-id="600be-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="600be-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="600be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="600be-102">SYNOPSIS</span></span>
<span data-ttu-id="600be-103">자동화 변수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="600be-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="600be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="600be-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="600be-105">설명은</span><span class="sxs-lookup"><span data-stu-id="600be-105">DESCRIPTION</span></span>
<span data-ttu-id="600be-106">**AzAutomationVariable** Cmdlet은 Azure 자동화에서 변수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="600be-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="600be-107">예제의</span><span class="sxs-lookup"><span data-stu-id="600be-107">EXAMPLES</span></span>

### <span data-ttu-id="600be-108">예제 1: 변수 제거</span><span class="sxs-lookup"><span data-stu-id="600be-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="600be-109">이 명령은 Contoso17 이라는 Automation 계정에서 StringVariable22 이라는 변수를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="600be-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="600be-110">이 명령은 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="600be-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="600be-111">따라서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="600be-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="600be-112">변수</span><span class="sxs-lookup"><span data-stu-id="600be-112">PARAMETERS</span></span>

### <span data-ttu-id="600be-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="600be-113">-AutomationAccountName</span></span>
<span data-ttu-id="600be-114">이 cmdlet이 삭제 하는 변수를 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="600be-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="600be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="600be-115">-DefaultProfile</span></span>
<span data-ttu-id="600be-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="600be-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="600be-117">-이름</span><span class="sxs-lookup"><span data-stu-id="600be-117">-Name</span></span>
<span data-ttu-id="600be-118">이 cmdlet이 삭제 하는 변수의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="600be-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="600be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="600be-119">-ResourceGroupName</span></span>
<span data-ttu-id="600be-120">이 cmdlet이 변수를 삭제할 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="600be-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="600be-121">-확인</span><span class="sxs-lookup"><span data-stu-id="600be-121">-Confirm</span></span>
<span data-ttu-id="600be-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="600be-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="600be-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="600be-123">-WhatIf</span></span>
<span data-ttu-id="600be-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="600be-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="600be-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="600be-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="600be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="600be-126">CommonParameters</span></span>
<span data-ttu-id="600be-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="600be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="600be-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="600be-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="600be-129">입력</span><span class="sxs-lookup"><span data-stu-id="600be-129">INPUTS</span></span>

### <span data-ttu-id="600be-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="600be-130">System.String</span></span>

## <span data-ttu-id="600be-131">출력</span><span class="sxs-lookup"><span data-stu-id="600be-131">OUTPUTS</span></span>

### <span data-ttu-id="600be-132">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="600be-132">System.Void</span></span>

## <span data-ttu-id="600be-133">상속자</span><span class="sxs-lookup"><span data-stu-id="600be-133">NOTES</span></span>

## <span data-ttu-id="600be-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="600be-134">RELATED LINKS</span></span>

[<span data-ttu-id="600be-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="600be-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="600be-136">새로운 AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="600be-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="600be-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="600be-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)



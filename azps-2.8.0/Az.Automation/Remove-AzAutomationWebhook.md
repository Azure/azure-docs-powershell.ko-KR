---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 5f3ba7d2bdc573e7a08976e575e86dcf05ae3400
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697745"
---
# <span data-ttu-id="d92f1-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="d92f1-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="d92f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d92f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d92f1-103">자동화 runbook에서 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d92f1-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="d92f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d92f1-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d92f1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d92f1-105">DESCRIPTION</span></span>
<span data-ttu-id="d92f1-106">**AzAutomationWebhook** Cmdlet은 Azure Automation runbook에서 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d92f1-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="d92f1-107">Webhook이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d92f1-107">The webhook is deleted.</span></span>

## <span data-ttu-id="d92f1-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d92f1-108">EXAMPLES</span></span>

### <span data-ttu-id="d92f1-109">예제 1: webhook 제거</span><span class="sxs-lookup"><span data-stu-id="d92f1-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="d92f1-110">이 명령은 AutomationAccount01 이라는 Automation 계정에서 Webhook11 이라는 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d92f1-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="d92f1-111">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d92f1-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="d92f1-112">따라서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d92f1-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="d92f1-113">변수</span><span class="sxs-lookup"><span data-stu-id="d92f1-113">PARAMETERS</span></span>

### <span data-ttu-id="d92f1-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d92f1-114">-AutomationAccountName</span></span>
<span data-ttu-id="d92f1-115">이 cmdlet이 webhook을 제거 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d92f1-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="d92f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d92f1-116">-DefaultProfile</span></span>
<span data-ttu-id="d92f1-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d92f1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d92f1-118">-이름</span><span class="sxs-lookup"><span data-stu-id="d92f1-118">-Name</span></span>
<span data-ttu-id="d92f1-119">이 cmdlet이 제거 하는 webhook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d92f1-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d92f1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d92f1-120">-ResourceGroupName</span></span>
<span data-ttu-id="d92f1-121">이 cmdlet이 webhook을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d92f1-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="d92f1-122">-확인</span><span class="sxs-lookup"><span data-stu-id="d92f1-122">-Confirm</span></span>
<span data-ttu-id="d92f1-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d92f1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d92f1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d92f1-124">-WhatIf</span></span>
<span data-ttu-id="d92f1-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d92f1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d92f1-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d92f1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d92f1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d92f1-127">CommonParameters</span></span>
<span data-ttu-id="d92f1-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d92f1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d92f1-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d92f1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d92f1-130">입력</span><span class="sxs-lookup"><span data-stu-id="d92f1-130">INPUTS</span></span>

### <span data-ttu-id="d92f1-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d92f1-131">System.String</span></span>

## <span data-ttu-id="d92f1-132">출력</span><span class="sxs-lookup"><span data-stu-id="d92f1-132">OUTPUTS</span></span>

### <span data-ttu-id="d92f1-133">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="d92f1-133">System.Void</span></span>

## <span data-ttu-id="d92f1-134">상속자</span><span class="sxs-lookup"><span data-stu-id="d92f1-134">NOTES</span></span>

## <span data-ttu-id="d92f1-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d92f1-135">RELATED LINKS</span></span>

[<span data-ttu-id="d92f1-136">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="d92f1-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="d92f1-137">새로운 AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="d92f1-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="d92f1-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="d92f1-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)



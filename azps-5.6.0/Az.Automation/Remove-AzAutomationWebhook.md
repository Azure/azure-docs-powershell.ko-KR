---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 93c370eaefa83c5e1be4692cb41ea0793b8f4681
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009840"
---
# <span data-ttu-id="7b2f7-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7b2f7-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="7b2f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b2f7-102">SYNOPSIS</span></span>
<span data-ttu-id="7b2f7-103">Automation Runbook에서 웹후크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7b2f7-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="7b2f7-104">구문</span><span class="sxs-lookup"><span data-stu-id="7b2f7-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b2f7-105">설명</span><span class="sxs-lookup"><span data-stu-id="7b2f7-105">DESCRIPTION</span></span>
<span data-ttu-id="7b2f7-106">**Remove-AzAutomationWebhook** cmdlet은 Azure Automation Runbook에서 웹후크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7b2f7-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="7b2f7-107">웹후크가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b2f7-107">The webhook is deleted.</span></span>

## <span data-ttu-id="7b2f7-108">예제</span><span class="sxs-lookup"><span data-stu-id="7b2f7-108">EXAMPLES</span></span>

### <span data-ttu-id="7b2f7-109">예제 1: 웹후크 제거</span><span class="sxs-lookup"><span data-stu-id="7b2f7-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="7b2f7-110">이 명령은 AutomationAccount01이라는 Automation 계정에서 Webhook11이라는 웹후크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7b2f7-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="7b2f7-111">명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="7b2f7-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7b2f7-112">따라서 확인을 묻는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b2f7-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7b2f7-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7b2f7-113">PARAMETERS</span></span>

### <span data-ttu-id="7b2f7-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7b2f7-114">-AutomationAccountName</span></span>
<span data-ttu-id="7b2f7-115">이 cmdlet에서 웹후크를 제거하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b2f7-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="7b2f7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b2f7-116">-DefaultProfile</span></span>
<span data-ttu-id="7b2f7-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7b2f7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b2f7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7b2f7-118">-Name</span></span>
<span data-ttu-id="7b2f7-119">이 cmdlet이 제거한 웹후크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b2f7-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7b2f7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b2f7-120">-ResourceGroupName</span></span>
<span data-ttu-id="7b2f7-121">이 cmdlet에서 웹후크를 제거하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b2f7-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="7b2f7-122">-확인</span><span class="sxs-lookup"><span data-stu-id="7b2f7-122">-Confirm</span></span>
<span data-ttu-id="7b2f7-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b2f7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b2f7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b2f7-124">-WhatIf</span></span>
<span data-ttu-id="7b2f7-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b2f7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b2f7-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b2f7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b2f7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b2f7-127">CommonParameters</span></span>
<span data-ttu-id="7b2f7-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7b2f7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b2f7-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7b2f7-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b2f7-130">입력</span><span class="sxs-lookup"><span data-stu-id="7b2f7-130">INPUTS</span></span>

### <span data-ttu-id="7b2f7-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7b2f7-131">System.String</span></span>

## <span data-ttu-id="7b2f7-132">출력</span><span class="sxs-lookup"><span data-stu-id="7b2f7-132">OUTPUTS</span></span>

### <span data-ttu-id="7b2f7-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="7b2f7-133">System.Void</span></span>

## <span data-ttu-id="7b2f7-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7b2f7-134">NOTES</span></span>

## <span data-ttu-id="7b2f7-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b2f7-135">RELATED LINKS</span></span>

[<span data-ttu-id="7b2f7-136">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7b2f7-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="7b2f7-137">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7b2f7-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="7b2f7-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="7b2f7-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)



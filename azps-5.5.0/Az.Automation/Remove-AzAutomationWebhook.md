---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 13eeb70905225b89cfc362a13425ec77e0ef9521
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205432"
---
# <span data-ttu-id="631f0-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="631f0-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="631f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="631f0-102">SYNOPSIS</span></span>
<span data-ttu-id="631f0-103">Automation Runbook에서 웹후크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="631f0-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="631f0-104">구문</span><span class="sxs-lookup"><span data-stu-id="631f0-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="631f0-105">설명</span><span class="sxs-lookup"><span data-stu-id="631f0-105">DESCRIPTION</span></span>
<span data-ttu-id="631f0-106">**Remove-AzAutomationWebhook** cmdlet은 Azure Automation Runbook에서 웹후크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="631f0-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="631f0-107">웹후크가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="631f0-107">The webhook is deleted.</span></span>

## <span data-ttu-id="631f0-108">예제</span><span class="sxs-lookup"><span data-stu-id="631f0-108">EXAMPLES</span></span>

### <span data-ttu-id="631f0-109">예제 1: 웹후크 제거</span><span class="sxs-lookup"><span data-stu-id="631f0-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="631f0-110">이 명령은 AutomationAccount01이라는 Automation 계정에서 Webhook11이라는 웹후크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="631f0-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="631f0-111">이 명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="631f0-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="631f0-112">따라서 확인을 묻는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="631f0-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="631f0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="631f0-113">PARAMETERS</span></span>

### <span data-ttu-id="631f0-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="631f0-114">-AutomationAccountName</span></span>
<span data-ttu-id="631f0-115">이 cmdlet이 웹후크를 제거하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="631f0-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="631f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="631f0-116">-DefaultProfile</span></span>
<span data-ttu-id="631f0-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="631f0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="631f0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="631f0-118">-Name</span></span>
<span data-ttu-id="631f0-119">이 cmdlet이 제거하는 웹후크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="631f0-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="631f0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="631f0-120">-ResourceGroupName</span></span>
<span data-ttu-id="631f0-121">이 cmdlet이 웹후크를 제거하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="631f0-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="631f0-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="631f0-122">-Confirm</span></span>
<span data-ttu-id="631f0-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="631f0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="631f0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="631f0-124">-WhatIf</span></span>
<span data-ttu-id="631f0-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="631f0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="631f0-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="631f0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="631f0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="631f0-127">CommonParameters</span></span>
<span data-ttu-id="631f0-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="631f0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="631f0-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="631f0-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="631f0-130">입력</span><span class="sxs-lookup"><span data-stu-id="631f0-130">INPUTS</span></span>

### <span data-ttu-id="631f0-131">System.String</span><span class="sxs-lookup"><span data-stu-id="631f0-131">System.String</span></span>

## <span data-ttu-id="631f0-132">출력</span><span class="sxs-lookup"><span data-stu-id="631f0-132">OUTPUTS</span></span>

### <span data-ttu-id="631f0-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="631f0-133">System.Void</span></span>

## <span data-ttu-id="631f0-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="631f0-134">NOTES</span></span>

## <span data-ttu-id="631f0-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="631f0-135">RELATED LINKS</span></span>

[<span data-ttu-id="631f0-136">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="631f0-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="631f0-137">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="631f0-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="631f0-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="631f0-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)



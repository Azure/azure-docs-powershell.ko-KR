---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 0c1f2e5135596dd0911b02414d35b15c824b7936
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373003"
---
# <span data-ttu-id="bda3b-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="bda3b-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="bda3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bda3b-102">SYNOPSIS</span></span>
<span data-ttu-id="bda3b-103">Automation Runbook에 대한 웹후크를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3b-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="bda3b-104">구문</span><span class="sxs-lookup"><span data-stu-id="bda3b-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bda3b-105">설명</span><span class="sxs-lookup"><span data-stu-id="bda3b-105">DESCRIPTION</span></span>
<span data-ttu-id="bda3b-106">**Set-AzAutomationWebhook** cmdlet은 Azure Automation Runbook에 대한 웹후크를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3b-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="bda3b-107">예제</span><span class="sxs-lookup"><span data-stu-id="bda3b-107">EXAMPLES</span></span>

### <span data-ttu-id="bda3b-108">예제 1: 웹후크 비활성화</span><span class="sxs-lookup"><span data-stu-id="bda3b-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="bda3b-109">이 명령은 AutomationAccount01이라는 Automation 계정에서 Webhook01이라는 웹후크를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3b-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="bda3b-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="bda3b-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="bda3b-111">이 명령은 웹후크에 대한 실행 값을 설정하고 Runbook을 Windows라는 Hybrid Worker 그룹에서 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3b-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="bda3b-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="bda3b-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="bda3b-113">이 명령은 웹후크에 대한 실행 값을 업데이트하고 Runbook을 Azure Runbook Worker에서 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3b-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="bda3b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bda3b-114">PARAMETERS</span></span>

### <span data-ttu-id="bda3b-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bda3b-115">-AutomationAccountName</span></span>
<span data-ttu-id="bda3b-116">이 cmdlet이 웹후크를 수정하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3b-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="bda3b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bda3b-117">-DefaultProfile</span></span>
<span data-ttu-id="bda3b-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bda3b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bda3b-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="bda3b-119">-IsEnabled</span></span>
<span data-ttu-id="bda3b-120">웹후크를 사용하도록 설정하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3b-120">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda3b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bda3b-121">-Name</span></span>
<span data-ttu-id="bda3b-122">이 cmdlet이 수정하는 웹후크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3b-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="bda3b-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="bda3b-123">-Parameters</span></span>
<span data-ttu-id="bda3b-124">키/값 쌍의 사전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3b-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="bda3b-125">키는 Runbook 매개 변수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bda3b-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="bda3b-126">값은 Runbook 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="bda3b-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="bda3b-127">웹후크에 대한 응답으로 Runbook이 시작되면 이러한 매개 변수가 Runbook에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="bda3b-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda3b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bda3b-128">-ResourceGroupName</span></span>
<span data-ttu-id="bda3b-129">이 cmdlet이 웹후크를 수정하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3b-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="bda3b-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="bda3b-130">-RunOn</span></span>
<span data-ttu-id="bda3b-131">Runbook을 실행해야 하는 하이브리드 에이전트의 선택적 이름</span><span class="sxs-lookup"><span data-stu-id="bda3b-131">Optional name of the hybrid agent which should execute the runbook</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda3b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda3b-132">CommonParameters</span></span>
<span data-ttu-id="bda3b-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda3b-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bda3b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda3b-135">입력</span><span class="sxs-lookup"><span data-stu-id="bda3b-135">INPUTS</span></span>

### <span data-ttu-id="bda3b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bda3b-136">System.String</span></span>

### <span data-ttu-id="bda3b-137">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bda3b-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bda3b-138">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="bda3b-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="bda3b-139">출력</span><span class="sxs-lookup"><span data-stu-id="bda3b-139">OUTPUTS</span></span>

### <span data-ttu-id="bda3b-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="bda3b-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="bda3b-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bda3b-141">NOTES</span></span>

## <span data-ttu-id="bda3b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bda3b-142">RELATED LINKS</span></span>

[<span data-ttu-id="bda3b-143">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="bda3b-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="bda3b-144">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="bda3b-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="bda3b-145">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="bda3b-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)



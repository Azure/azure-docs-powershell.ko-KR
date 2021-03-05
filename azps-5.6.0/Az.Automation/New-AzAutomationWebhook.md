---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 520efcb6cccc3c3d4c0afc3b532d528c11c305c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995736"
---
# <span data-ttu-id="54447-101">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="54447-101">New-AzAutomationWebhook</span></span>

## <span data-ttu-id="54447-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54447-102">SYNOPSIS</span></span>
<span data-ttu-id="54447-103">Automation Runbook에 대한 웹후크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54447-103">Creates a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="54447-104">구문</span><span class="sxs-lookup"><span data-stu-id="54447-104">SYNTAX</span></span>

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54447-105">설명</span><span class="sxs-lookup"><span data-stu-id="54447-105">DESCRIPTION</span></span>
<span data-ttu-id="54447-106">**New-AzAutomationWebhook** cmdlet은 Azure Automation Runbook에 대한 웹후크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54447-106">The **New-AzAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>
<span data-ttu-id="54447-107">다시 검색할 수 없습니다. 이 cmdlet이 반환하는 웹후크 URL을 저장해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="54447-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="54447-108">예제</span><span class="sxs-lookup"><span data-stu-id="54447-108">EXAMPLES</span></span>

### <span data-ttu-id="54447-109">예제 1: 웹후크 만들기</span><span class="sxs-lookup"><span data-stu-id="54447-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="54447-110">이 명령은 AutomationAccount01이라는 Automation 계정에서 ContosoRunbook이라는 Runbook에 Webhook06이라는 웹후크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54447-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="54447-111">명령은 웹후크를 $Webhook 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="54447-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="54447-112">웹후크가 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54447-112">The webhook is enabled.</span></span>
<span data-ttu-id="54447-113">웹후크가 지정된 시간으로 만료됩니다.</span><span class="sxs-lookup"><span data-stu-id="54447-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="54447-114">이 명령은 웹후크 매개 변수에 대한 값을 제공하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54447-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="54447-115">이 명령은 Force 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="54447-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="54447-116">따라서 확인을 묻는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54447-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="54447-117">예제 2: 매개 변수를 사용하여 웹후크 만들기</span><span class="sxs-lookup"><span data-stu-id="54447-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="54447-118">첫 번째 명령은 매개 변수의 사전을 만들고 매개 변수에 $Params 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="54447-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="54447-119">두 번째 명령은 AutomationAccount01이라는 Automation 계정에서 ContosoRunbook이라는 Runbook에 Webhook11이라는 웹후크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="54447-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="54447-120">명령은 웹후크에 $Params 매개 변수를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="54447-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="54447-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="54447-121">PARAMETERS</span></span>

### <span data-ttu-id="54447-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="54447-122">-AutomationAccountName</span></span>
<span data-ttu-id="54447-123">이 cmdlet에서 웹후크를 만드는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="54447-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="54447-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54447-124">-DefaultProfile</span></span>
<span data-ttu-id="54447-125">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="54447-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54447-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="54447-126">-ExpiryTime</span></span>
<span data-ttu-id="54447-127">웹후크의 만료 시간을 **DateTimeOffset 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="54447-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="54447-128">유효한 **DateTimeOffset로** 변환할 수 있는 문자열 또는 **DateTime을** 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="54447-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54447-129">-Force</span><span class="sxs-lookup"><span data-stu-id="54447-129">-Force</span></span>
<span data-ttu-id="54447-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="54447-130">ps_force</span></span>

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

### <span data-ttu-id="54447-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="54447-131">-IsEnabled</span></span>
<span data-ttu-id="54447-132">웹후크를 사용하도록 설정하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="54447-132">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54447-133">-Name</span><span class="sxs-lookup"><span data-stu-id="54447-133">-Name</span></span>
<span data-ttu-id="54447-134">웹후크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="54447-134">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="54447-135">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="54447-135">-Parameters</span></span>
<span data-ttu-id="54447-136">키/값 쌍의 사전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="54447-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="54447-137">키는 Runbook 매개 변수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54447-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="54447-138">값은 Runbook 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="54447-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="54447-139">웹후크에 대한 응답으로 Runbook이 시작되면 이러한 매개 변수가 Runbook에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="54447-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54447-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54447-140">-ResourceGroupName</span></span>
<span data-ttu-id="54447-141">이 cmdlet에서 웹후크를 만드는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="54447-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="54447-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="54447-142">-RunbookName</span></span>
<span data-ttu-id="54447-143">웹후크에 연결할 Runbook의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="54447-143">Specifies the name of the runbook to associate to the webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54447-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="54447-144">-RunOn</span></span>
<span data-ttu-id="54447-145">Runbook을 실행해야 하는 하이브리드 작업 그룹의 선택적 이름</span><span class="sxs-lookup"><span data-stu-id="54447-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

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

### <span data-ttu-id="54447-146">-확인</span><span class="sxs-lookup"><span data-stu-id="54447-146">-Confirm</span></span>
<span data-ttu-id="54447-147">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="54447-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54447-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54447-148">-WhatIf</span></span>
<span data-ttu-id="54447-149">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="54447-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54447-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54447-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54447-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54447-151">CommonParameters</span></span>
<span data-ttu-id="54447-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="54447-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54447-153">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="54447-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54447-154">입력</span><span class="sxs-lookup"><span data-stu-id="54447-154">INPUTS</span></span>

### <span data-ttu-id="54447-155">System.String</span><span class="sxs-lookup"><span data-stu-id="54447-155">System.String</span></span>

### <span data-ttu-id="54447-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="54447-156">System.Boolean</span></span>

### <span data-ttu-id="54447-157">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="54447-157">System.DateTimeOffset</span></span>

## <span data-ttu-id="54447-158">출력</span><span class="sxs-lookup"><span data-stu-id="54447-158">OUTPUTS</span></span>

### <span data-ttu-id="54447-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="54447-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="54447-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="54447-160">NOTES</span></span>

## <span data-ttu-id="54447-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54447-161">RELATED LINKS</span></span>

[<span data-ttu-id="54447-162">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="54447-162">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="54447-163">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="54447-163">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="54447-164">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="54447-164">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)



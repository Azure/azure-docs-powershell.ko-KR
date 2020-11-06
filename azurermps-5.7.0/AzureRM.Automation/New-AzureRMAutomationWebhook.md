---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
ms.openlocfilehash: 417ab3f7f787a76041caceebbfcf32f9733717b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536836"
---
# <span data-ttu-id="9a12f-101">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9a12f-101">New-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="9a12f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a12f-102">SYNOPSIS</span></span>
<span data-ttu-id="9a12f-103">자동화 runbook에 대 한 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-103">Creates a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a12f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a12f-104">SYNTAX</span></span>

```
New-AzureRmAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a12f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9a12f-105">DESCRIPTION</span></span>
<span data-ttu-id="9a12f-106">**AzureRmAutomationWebhook** Cmdlet은 Azure Automation runbook에 대 한 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-106">The **New-AzureRmAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>

<span data-ttu-id="9a12f-107">다시 검색할 수 없기 때문에이 cmdlet이 반환 하는 webhook URL을 저장 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="9a12f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9a12f-108">EXAMPLES</span></span>

### <span data-ttu-id="9a12f-109">예제 1: webhook 만들기</span><span class="sxs-lookup"><span data-stu-id="9a12f-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzureRmAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="9a12f-110">이 명령은 AutomationAccount01 이라는 Automation 계정에서 ContosoRunbook 라는 runbook에 대 한 Webhook06 이라는 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="9a12f-111">명령이 $Webhook 변수에 webhook을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="9a12f-112">Webhook을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-112">The webhook is enabled.</span></span>
<span data-ttu-id="9a12f-113">지정 된 시간에 webhook이 만료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="9a12f-114">이 명령은 webhook 매개 변수에 대 한 값을 제공 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="9a12f-115">이 명령은 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="9a12f-116">따라서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="9a12f-117">예제 2: 매개 변수를 사용 하 여 webhook 만들기</span><span class="sxs-lookup"><span data-stu-id="9a12f-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzureRmAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="9a12f-118">첫 번째 명령은 매개 변수 사전을 만들어 $Params 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="9a12f-119">두 번째 명령은 AutomationAccount01 이라는 Automation 계정에서 ContosoRunbook 라는 runbook에 대 한 Webhook11 이라는 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="9a12f-120">이 명령은 $Params에서 매개 변수를 webhook에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="9a12f-121">변수</span><span class="sxs-lookup"><span data-stu-id="9a12f-121">PARAMETERS</span></span>

### <span data-ttu-id="9a12f-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9a12f-122">-AutomationAccountName</span></span>
<span data-ttu-id="9a12f-123">이 cmdlet이 webhook을 만드는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a12f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a12f-124">-DefaultProfile</span></span>
<span data-ttu-id="9a12f-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9a12f-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a12f-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="9a12f-126">-ExpiryTime</span></span>
<span data-ttu-id="9a12f-127">Webhook에 대 한 만료 시간을 **DateTimeOffset** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="9a12f-128">유효한 **DateTimeOffset** 으로 변환할 수 있는 문자열 또는 **DateTime** 을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a12f-129">-Force</span><span class="sxs-lookup"><span data-stu-id="9a12f-129">-Force</span></span>
<span data-ttu-id="9a12f-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="9a12f-130">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a12f-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="9a12f-131">-IsEnabled</span></span>
<span data-ttu-id="9a12f-132">Webhook을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-132">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a12f-133">-이름</span><span class="sxs-lookup"><span data-stu-id="9a12f-133">-Name</span></span>
<span data-ttu-id="9a12f-134">Webhook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-134">Specifies a name for the webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a12f-135">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="9a12f-135">-Parameters</span></span>
<span data-ttu-id="9a12f-136">키/값 쌍의 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="9a12f-137">키는 runbook 매개 변수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="9a12f-138">값은 runbook 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="9a12f-139">Webhook에 대 한 응답으로 runbook이 시작 되 면 이러한 매개 변수는 runbook으로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a12f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a12f-140">-ResourceGroupName</span></span>
<span data-ttu-id="9a12f-141">이 cmdlet이 webhook을 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a12f-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="9a12f-142">-RunbookName</span></span>
<span data-ttu-id="9a12f-143">Webhook에 연결할 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-143">Specifies the name of the runbook to associate to the webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a12f-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="9a12f-144">-RunOn</span></span>
<span data-ttu-id="9a12f-145">Runbook을 실행 해야 하는 하이브리드 작업자 그룹의 이름 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="9a12f-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a12f-146">-확인</span><span class="sxs-lookup"><span data-stu-id="9a12f-146">-Confirm</span></span>
<span data-ttu-id="9a12f-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a12f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a12f-148">-WhatIf</span></span>
<span data-ttu-id="9a12f-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a12f-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a12f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a12f-151">CommonParameters</span></span>
<span data-ttu-id="9a12f-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a12f-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a12f-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a12f-154">입력</span><span class="sxs-lookup"><span data-stu-id="9a12f-154">INPUTS</span></span>

### <span data-ttu-id="9a12f-155">않아야</span><span class="sxs-lookup"><span data-stu-id="9a12f-155">None</span></span>
<span data-ttu-id="9a12f-156">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a12f-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9a12f-157">출력</span><span class="sxs-lookup"><span data-stu-id="9a12f-157">OUTPUTS</span></span>

### <span data-ttu-id="9a12f-158">Microsoft Azure. a \*. Webhook</span><span class="sxs-lookup"><span data-stu-id="9a12f-158">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="9a12f-159">상속자</span><span class="sxs-lookup"><span data-stu-id="9a12f-159">NOTES</span></span>

## <span data-ttu-id="9a12f-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a12f-160">RELATED LINKS</span></span>

[<span data-ttu-id="9a12f-161">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9a12f-161">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="9a12f-162">제거-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9a12f-162">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="9a12f-163">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="9a12f-163">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)



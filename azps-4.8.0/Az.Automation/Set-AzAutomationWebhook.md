---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 0c1f2e5135596dd0911b02414d35b15c824b7936
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213720"
---
# <span data-ttu-id="e3cc2-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e3cc2-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="e3cc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="e3cc2-103">자동화 runbook에 대 한 webhook을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3cc2-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="e3cc2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3cc2-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3cc2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e3cc2-105">DESCRIPTION</span></span>
<span data-ttu-id="e3cc2-106">**AzAutomationWebhook** Cmdlet은 Azure Automation runbook에 대 한 webhook을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3cc2-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="e3cc2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e3cc2-107">EXAMPLES</span></span>

### <span data-ttu-id="e3cc2-108">예제 1: webhook 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="e3cc2-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="e3cc2-109">이 명령은 AutomationAccount01 이라는 Automation 계정에서 Webhook01 이라는 webhook을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3cc2-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="e3cc2-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="e3cc2-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="e3cc2-111">이 명령은 webhook에 대해 run on 값을 설정 하 고 Windows 라는 하이브리드 작업자 그룹에서 runbook을 실행 하도록 강제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3cc2-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="e3cc2-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="e3cc2-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="e3cc2-113">이 명령은 webhook에 대 한 실행 대상 값을 업데이트 하 고 Azure runbook worker에서 runbook을 실행 하도록 강제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3cc2-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="e3cc2-114">변수</span><span class="sxs-lookup"><span data-stu-id="e3cc2-114">PARAMETERS</span></span>

### <span data-ttu-id="e3cc2-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e3cc2-115">-AutomationAccountName</span></span>
<span data-ttu-id="e3cc2-116">이 cmdlet이 webhook을 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3cc2-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="e3cc2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3cc2-117">-DefaultProfile</span></span>
<span data-ttu-id="e3cc2-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e3cc2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3cc2-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="e3cc2-119">-IsEnabled</span></span>
<span data-ttu-id="e3cc2-120">Webhook을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3cc2-120">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="e3cc2-121">-이름</span><span class="sxs-lookup"><span data-stu-id="e3cc2-121">-Name</span></span>
<span data-ttu-id="e3cc2-122">이 cmdlet이 수정 하는 webhook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3cc2-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e3cc2-123">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="e3cc2-123">-Parameters</span></span>
<span data-ttu-id="e3cc2-124">키/값 쌍의 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3cc2-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="e3cc2-125">키는 runbook 매개 변수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3cc2-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="e3cc2-126">값은 runbook 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e3cc2-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="e3cc2-127">Webhook에 대 한 응답으로 runbook이 시작 되 면 이러한 매개 변수는 runbook으로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3cc2-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="e3cc2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3cc2-128">-ResourceGroupName</span></span>
<span data-ttu-id="e3cc2-129">이 cmdlet이 webhook을 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3cc2-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="e3cc2-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="e3cc2-130">-RunOn</span></span>
<span data-ttu-id="e3cc2-131">Runbook을 실행 해야 하는 하이브리드 에이전트의 이름 (선택 사항)</span><span class="sxs-lookup"><span data-stu-id="e3cc2-131">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="e3cc2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3cc2-132">CommonParameters</span></span>
<span data-ttu-id="e3cc2-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3cc2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3cc2-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e3cc2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3cc2-135">입력</span><span class="sxs-lookup"><span data-stu-id="e3cc2-135">INPUTS</span></span>

### <span data-ttu-id="e3cc2-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e3cc2-136">System.String</span></span>

### <span data-ttu-id="e3cc2-137">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e3cc2-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e3cc2-138">컬렉션. IDictionary</span><span class="sxs-lookup"><span data-stu-id="e3cc2-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="e3cc2-139">출력</span><span class="sxs-lookup"><span data-stu-id="e3cc2-139">OUTPUTS</span></span>

### <span data-ttu-id="e3cc2-140">Microsoft Azure. a \*. Webhook</span><span class="sxs-lookup"><span data-stu-id="e3cc2-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="e3cc2-141">상속자</span><span class="sxs-lookup"><span data-stu-id="e3cc2-141">NOTES</span></span>

## <span data-ttu-id="e3cc2-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3cc2-142">RELATED LINKS</span></span>

[<span data-ttu-id="e3cc2-143">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e3cc2-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="e3cc2-144">새로운 AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e3cc2-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="e3cc2-145">제거-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e3cc2-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)



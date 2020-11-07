---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 39e0fda02eb41ed591562d9cfc1f7902fa43c38a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701492"
---
# <span data-ttu-id="39f4b-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="39f4b-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="39f4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="39f4b-103">자동화 runbook에 대 한 webhook을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f4b-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="39f4b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39f4b-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39f4b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="39f4b-105">DESCRIPTION</span></span>
<span data-ttu-id="39f4b-106">**AzAutomationWebhook** Cmdlet은 Azure Automation runbook에 대 한 webhook을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f4b-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="39f4b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="39f4b-107">EXAMPLES</span></span>

### <span data-ttu-id="39f4b-108">예제 1: webhook 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="39f4b-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="39f4b-109">이 명령은 AutomationAccount01 이라는 Automation 계정에서 Webhook01 이라는 webhook을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f4b-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="39f4b-110">변수</span><span class="sxs-lookup"><span data-stu-id="39f4b-110">PARAMETERS</span></span>

### <span data-ttu-id="39f4b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="39f4b-111">-AutomationAccountName</span></span>
<span data-ttu-id="39f4b-112">이 cmdlet이 webhook을 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f4b-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="39f4b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39f4b-113">-DefaultProfile</span></span>
<span data-ttu-id="39f4b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="39f4b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39f4b-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="39f4b-115">-IsEnabled</span></span>
<span data-ttu-id="39f4b-116">Webhook을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f4b-116">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="39f4b-117">-이름</span><span class="sxs-lookup"><span data-stu-id="39f4b-117">-Name</span></span>
<span data-ttu-id="39f4b-118">이 cmdlet이 수정 하는 webhook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f4b-118">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="39f4b-119">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="39f4b-119">-Parameters</span></span>
<span data-ttu-id="39f4b-120">키/값 쌍의 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f4b-120">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="39f4b-121">키는 runbook 매개 변수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="39f4b-121">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="39f4b-122">값은 runbook 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="39f4b-122">The values are the runbook parameter values.</span></span>
<span data-ttu-id="39f4b-123">Webhook에 대 한 응답으로 runbook이 시작 되 면 이러한 매개 변수는 runbook으로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39f4b-123">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="39f4b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39f4b-124">-ResourceGroupName</span></span>
<span data-ttu-id="39f4b-125">이 cmdlet이 webhook을 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f4b-125">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="39f4b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f4b-126">CommonParameters</span></span>
<span data-ttu-id="39f4b-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39f4b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f4b-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39f4b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f4b-129">입력</span><span class="sxs-lookup"><span data-stu-id="39f4b-129">INPUTS</span></span>

### <span data-ttu-id="39f4b-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="39f4b-130">System.String</span></span>

### <span data-ttu-id="39f4b-131">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="39f4b-131">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="39f4b-132">컬렉션. IDictionary</span><span class="sxs-lookup"><span data-stu-id="39f4b-132">System.Collections.IDictionary</span></span>

## <span data-ttu-id="39f4b-133">출력</span><span class="sxs-lookup"><span data-stu-id="39f4b-133">OUTPUTS</span></span>

### <span data-ttu-id="39f4b-134">Microsoft Azure. a \*. Webhook</span><span class="sxs-lookup"><span data-stu-id="39f4b-134">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="39f4b-135">상속자</span><span class="sxs-lookup"><span data-stu-id="39f4b-135">NOTES</span></span>

## <span data-ttu-id="39f4b-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39f4b-136">RELATED LINKS</span></span>

[<span data-ttu-id="39f4b-137">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="39f4b-137">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="39f4b-138">새로운 AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="39f4b-138">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="39f4b-139">제거-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="39f4b-139">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)



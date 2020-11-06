---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
ms.openlocfilehash: b889a3b061556fc6c5ad4be1dfd118dac49f1f62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528320"
---
# <span data-ttu-id="fe317-101">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="fe317-101">Set-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="fe317-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe317-102">SYNOPSIS</span></span>
<span data-ttu-id="fe317-103">자동화 runbook에 대 한 webhook을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe317-103">Modifies a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe317-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fe317-104">SYNTAX</span></span>

```
Set-AzureRmAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe317-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fe317-105">DESCRIPTION</span></span>
<span data-ttu-id="fe317-106">**AzureRmAutomationWebhook** Cmdlet은 Azure Automation runbook에 대 한 webhook을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe317-106">The **Set-AzureRmAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="fe317-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fe317-107">EXAMPLES</span></span>

### <span data-ttu-id="fe317-108">예제 1: webhook 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="fe317-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzureAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="fe317-109">이 명령은 AutomationAccount01 이라는 Automation 계정에서 Webhook01 이라는 webhook을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe317-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="fe317-110">변수</span><span class="sxs-lookup"><span data-stu-id="fe317-110">PARAMETERS</span></span>

### <span data-ttu-id="fe317-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fe317-111">-AutomationAccountName</span></span>
<span data-ttu-id="fe317-112">이 cmdlet이 webhook을 수정 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe317-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="fe317-113">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="fe317-113">-IsEnabled</span></span>
<span data-ttu-id="fe317-114">Webhook을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe317-114">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="fe317-115">-이름</span><span class="sxs-lookup"><span data-stu-id="fe317-115">-Name</span></span>
<span data-ttu-id="fe317-116">이 cmdlet이 수정 하는 webhook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe317-116">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fe317-117">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="fe317-117">-Parameters</span></span>
<span data-ttu-id="fe317-118">키/값 쌍의 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe317-118">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="fe317-119">키는 runbook 매개 변수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fe317-119">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="fe317-120">값은 runbook 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="fe317-120">The values are the runbook parameter values.</span></span>
<span data-ttu-id="fe317-121">Webhook에 대 한 응답으로 runbook이 시작 되 면 이러한 매개 변수는 runbook으로 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe317-121">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="fe317-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe317-122">-ResourceGroupName</span></span>
<span data-ttu-id="fe317-123">이 cmdlet이 webhook을 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe317-123">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="fe317-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe317-124">-DefaultProfile</span></span>
<span data-ttu-id="fe317-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fe317-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe317-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe317-126">CommonParameters</span></span>
<span data-ttu-id="fe317-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe317-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe317-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe317-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe317-129">입력</span><span class="sxs-lookup"><span data-stu-id="fe317-129">INPUTS</span></span>

## <span data-ttu-id="fe317-130">출력</span><span class="sxs-lookup"><span data-stu-id="fe317-130">OUTPUTS</span></span>

### <span data-ttu-id="fe317-131">Microsoft Azure. a \*. Webhook</span><span class="sxs-lookup"><span data-stu-id="fe317-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="fe317-132">상속자</span><span class="sxs-lookup"><span data-stu-id="fe317-132">NOTES</span></span>

## <span data-ttu-id="fe317-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe317-133">RELATED LINKS</span></span>

[<span data-ttu-id="fe317-134">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="fe317-134">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="fe317-135">새로운 AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="fe317-135">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="fe317-136">제거-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="fe317-136">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)



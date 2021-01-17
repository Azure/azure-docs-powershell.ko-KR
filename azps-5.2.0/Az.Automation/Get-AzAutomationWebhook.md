---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: ceca8c13b2cac0cc8685b1fa9fa3b26ab6017856
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373661"
---
# <span data-ttu-id="6dbc9-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="6dbc9-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="6dbc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dbc9-102">SYNOPSIS</span></span>
<span data-ttu-id="6dbc9-103">Automation에서 웹후크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6dbc9-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="6dbc9-104">구문</span><span class="sxs-lookup"><span data-stu-id="6dbc9-104">SYNTAX</span></span>

### <span data-ttu-id="6dbc9-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="6dbc9-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dbc9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6dbc9-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dbc9-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="6dbc9-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dbc9-108">설명</span><span class="sxs-lookup"><span data-stu-id="6dbc9-108">DESCRIPTION</span></span>
<span data-ttu-id="6dbc9-109">**Get-AzAutomationWebhook** cmdlet은 웹후크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6dbc9-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="6dbc9-110">특정 웹후크를 얻습니다. 웹후크 이름을 지정하거나 Azure Automation Runbook의 이름을 지정하여 웹후크를 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="6dbc9-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="6dbc9-111">예제</span><span class="sxs-lookup"><span data-stu-id="6dbc9-111">EXAMPLES</span></span>

### <span data-ttu-id="6dbc9-112">예제 1: Runbook에 대한 모든 웹후크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6dbc9-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="6dbc9-113">이 명령은 ResourceGroup01이라는 리소스 그룹의 AutomationAccount01 Automation 계정에서 Runbook03이라는 Runbook에 대한 모든 웹후크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6dbc9-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="6dbc9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6dbc9-114">PARAMETERS</span></span>

### <span data-ttu-id="6dbc9-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6dbc9-115">-AutomationAccountName</span></span>
<span data-ttu-id="6dbc9-116">이 cmdlet이 웹후크를 얻을 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6dbc9-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="6dbc9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dbc9-117">-DefaultProfile</span></span>
<span data-ttu-id="6dbc9-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6dbc9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6dbc9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6dbc9-119">-Name</span></span>
<span data-ttu-id="6dbc9-120">이 cmdlet이 얻을 웹후크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6dbc9-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: WebhookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dbc9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dbc9-121">-ResourceGroupName</span></span>
<span data-ttu-id="6dbc9-122">이 cmdlet이 웹후크를 얻을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6dbc9-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="6dbc9-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="6dbc9-123">-RunbookName</span></span>
<span data-ttu-id="6dbc9-124">이 cmdlet이 웹후크를 얻을 Runbook의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6dbc9-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dbc9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dbc9-125">CommonParameters</span></span>
<span data-ttu-id="6dbc9-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6dbc9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dbc9-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6dbc9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dbc9-128">입력</span><span class="sxs-lookup"><span data-stu-id="6dbc9-128">INPUTS</span></span>

### <span data-ttu-id="6dbc9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6dbc9-129">System.String</span></span>

## <span data-ttu-id="6dbc9-130">출력</span><span class="sxs-lookup"><span data-stu-id="6dbc9-130">OUTPUTS</span></span>

### <span data-ttu-id="6dbc9-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="6dbc9-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="6dbc9-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6dbc9-132">NOTES</span></span>

## <span data-ttu-id="6dbc9-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6dbc9-133">RELATED LINKS</span></span>

[<span data-ttu-id="6dbc9-134">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="6dbc9-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="6dbc9-135">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="6dbc9-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="6dbc9-136">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="6dbc9-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: 00125a7ad3d74d3e710b782d0be7fdb20004ef4a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014112"
---
# <span data-ttu-id="0ca08-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0ca08-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="0ca08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ca08-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca08-103">Automation에서 웹후크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0ca08-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="0ca08-104">구문</span><span class="sxs-lookup"><span data-stu-id="0ca08-104">SYNTAX</span></span>

### <span data-ttu-id="0ca08-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="0ca08-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ca08-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0ca08-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ca08-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="0ca08-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ca08-108">설명</span><span class="sxs-lookup"><span data-stu-id="0ca08-108">DESCRIPTION</span></span>
<span data-ttu-id="0ca08-109">**Get-AzAutomationWebhook** cmdlet은 웹후크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0ca08-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="0ca08-110">특정 웹후크를 얻게하려면 웹후크 이름을 지정하거나 Azure Automation Runbook의 이름을 지정하여 웹후크를 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="0ca08-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span><br>
<span data-ttu-id="0ca08-111">**참고:** WebhookUri는 보안 문제로 인해 빈 문자열로 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ca08-111">**Note:** The WebhookUri is returned as empty string due to security concerns.</span></span> <span data-ttu-id="0ca08-112">**Get-AzAutomationWebhook를** 사용하여 검색할 수 없습니다. **New-AzAutomationWebhook** cmdlet이 반환하는 웹후크 URL을 저장해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ca08-112">Please make sure to save the webhook URL that **New-AzAutomationWebhook** cmdlet returns, because it cannot be retrieved by using **Get-AzAutomationWebhook**.</span></span>

## <span data-ttu-id="0ca08-113">예제</span><span class="sxs-lookup"><span data-stu-id="0ca08-113">EXAMPLES</span></span>

### <span data-ttu-id="0ca08-114">예제 1: Runbook에 대한 모든 웹후크 다운로드</span><span class="sxs-lookup"><span data-stu-id="0ca08-114">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="0ca08-115">이 명령은 ResourceGroup01이라는 리소스 그룹의 AutomationAccount01이라는 Automation 계정에서 Runbook03이라는 Runbook의 모든 웹후크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0ca08-115">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="0ca08-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0ca08-116">PARAMETERS</span></span>

### <span data-ttu-id="0ca08-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0ca08-117">-AutomationAccountName</span></span>
<span data-ttu-id="0ca08-118">이 cmdlet에서 웹후크를 얻을 수 있는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0ca08-118">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="0ca08-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ca08-119">-DefaultProfile</span></span>
<span data-ttu-id="0ca08-120">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0ca08-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ca08-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0ca08-121">-Name</span></span>
<span data-ttu-id="0ca08-122">이 cmdlet이 얻을 웹후크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0ca08-122">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0ca08-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ca08-123">-ResourceGroupName</span></span>
<span data-ttu-id="0ca08-124">이 cmdlet에서 웹후크를 얻을 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0ca08-124">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="0ca08-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="0ca08-125">-RunbookName</span></span>
<span data-ttu-id="0ca08-126">이 cmdlet에서 웹후크를 얻을 Runbook의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0ca08-126">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="0ca08-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca08-127">CommonParameters</span></span>
<span data-ttu-id="0ca08-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0ca08-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca08-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0ca08-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca08-130">입력</span><span class="sxs-lookup"><span data-stu-id="0ca08-130">INPUTS</span></span>

### <span data-ttu-id="0ca08-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0ca08-131">System.String</span></span>

## <span data-ttu-id="0ca08-132">출력</span><span class="sxs-lookup"><span data-stu-id="0ca08-132">OUTPUTS</span></span>

### <span data-ttu-id="0ca08-133">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="0ca08-133">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="0ca08-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0ca08-134">NOTES</span></span>

## <span data-ttu-id="0ca08-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ca08-135">RELATED LINKS</span></span>

[<span data-ttu-id="0ca08-136">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0ca08-136">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="0ca08-137">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0ca08-137">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="0ca08-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0ca08-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: ceca8c13b2cac0cc8685b1fa9fa3b26ab6017856
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044988"
---
# <span data-ttu-id="e1f87-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e1f87-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="e1f87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1f87-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f87-103">자동화에서 webhooks를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e1f87-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="e1f87-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e1f87-104">SYNTAX</span></span>

### <span data-ttu-id="e1f87-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="e1f87-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1f87-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e1f87-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1f87-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="e1f87-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1f87-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e1f87-108">DESCRIPTION</span></span>
<span data-ttu-id="e1f87-109">**Get-AzAutomationWebhook** cmdlet은 webhooks를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e1f87-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="e1f87-110">특정 webhooks를 가져오려면 webhook 이름을 지정 하거나 Azure Automation runbook의 이름을 지정 하 여 연결 된 webhooks를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e1f87-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="e1f87-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e1f87-111">EXAMPLES</span></span>

### <span data-ttu-id="e1f87-112">예제 1: runbook에 대 한 모든 webhooks 가져오기</span><span class="sxs-lookup"><span data-stu-id="e1f87-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="e1f87-113">이 명령은 ResourceGroup01 이라는 리소스 그룹에서 AutomationAccount01 이라는 Automation 계정의 Runbook03 이라는 이름의 runbook에 대 한 모든 webhooks를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e1f87-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="e1f87-114">변수</span><span class="sxs-lookup"><span data-stu-id="e1f87-114">PARAMETERS</span></span>

### <span data-ttu-id="e1f87-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e1f87-115">-AutomationAccountName</span></span>
<span data-ttu-id="e1f87-116">이 cmdlet이 webhook을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1f87-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="e1f87-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f87-117">-DefaultProfile</span></span>
<span data-ttu-id="e1f87-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e1f87-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1f87-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e1f87-119">-Name</span></span>
<span data-ttu-id="e1f87-120">이 cmdlet이 가져오는 webhook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1f87-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e1f87-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1f87-121">-ResourceGroupName</span></span>
<span data-ttu-id="e1f87-122">이 cmdlet이 webhooks를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1f87-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="e1f87-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="e1f87-123">-RunbookName</span></span>
<span data-ttu-id="e1f87-124">이 cmdlet이 webhooks를 가져오는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1f87-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="e1f87-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f87-125">CommonParameters</span></span>
<span data-ttu-id="e1f87-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1f87-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f87-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1f87-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f87-128">입력</span><span class="sxs-lookup"><span data-stu-id="e1f87-128">INPUTS</span></span>

### <span data-ttu-id="e1f87-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e1f87-129">System.String</span></span>

## <span data-ttu-id="e1f87-130">출력</span><span class="sxs-lookup"><span data-stu-id="e1f87-130">OUTPUTS</span></span>

### <span data-ttu-id="e1f87-131">Microsoft Azure. a \*. Webhook</span><span class="sxs-lookup"><span data-stu-id="e1f87-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="e1f87-132">상속자</span><span class="sxs-lookup"><span data-stu-id="e1f87-132">NOTES</span></span>

## <span data-ttu-id="e1f87-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1f87-133">RELATED LINKS</span></span>

[<span data-ttu-id="e1f87-134">새로운 AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e1f87-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="e1f87-135">제거-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e1f87-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="e1f87-136">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e1f87-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)



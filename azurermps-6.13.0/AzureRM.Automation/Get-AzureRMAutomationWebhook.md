---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
ms.openlocfilehash: a384753d6407eff7864cea6972ac03ab5bd12515
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703185"
---
# <span data-ttu-id="fb23b-101">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="fb23b-101">Get-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="fb23b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb23b-102">SYNOPSIS</span></span>
<span data-ttu-id="fb23b-103">자동화에서 webhooks를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb23b-103">Gets webhooks from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb23b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb23b-104">SYNTAX</span></span>

### <span data-ttu-id="fb23b-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="fb23b-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb23b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fb23b-106">ByName</span></span>
```
Get-AzureRmAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb23b-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="fb23b-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb23b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fb23b-108">DESCRIPTION</span></span>
<span data-ttu-id="fb23b-109">**Get-AzureRmAutomationWebhook** cmdlet은 webhooks를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb23b-109">The **Get-AzureRmAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="fb23b-110">특정 webhooks를 가져오려면 webhook 이름을 지정 하거나 Azure Automation runbook의 이름을 지정 하 여 연결 된 webhooks를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb23b-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="fb23b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="fb23b-111">EXAMPLES</span></span>

### <span data-ttu-id="fb23b-112">예제 1: runbook에 대 한 모든 webhooks 가져오기</span><span class="sxs-lookup"><span data-stu-id="fb23b-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="fb23b-113">이 명령은 ResourceGroup01 이라는 리소스 그룹에서 AutomationAccount01 이라는 Automation 계정의 Runbook03 이라는 이름의 runbook에 대 한 모든 webhooks를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb23b-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="fb23b-114">변수</span><span class="sxs-lookup"><span data-stu-id="fb23b-114">PARAMETERS</span></span>

### <span data-ttu-id="fb23b-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fb23b-115">-AutomationAccountName</span></span>
<span data-ttu-id="fb23b-116">이 cmdlet이 webhook을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb23b-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="fb23b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb23b-117">-DefaultProfile</span></span>
<span data-ttu-id="fb23b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fb23b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb23b-119">-이름</span><span class="sxs-lookup"><span data-stu-id="fb23b-119">-Name</span></span>
<span data-ttu-id="fb23b-120">이 cmdlet이 가져오는 webhook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb23b-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fb23b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb23b-121">-ResourceGroupName</span></span>
<span data-ttu-id="fb23b-122">이 cmdlet이 webhooks를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb23b-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="fb23b-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="fb23b-123">-RunbookName</span></span>
<span data-ttu-id="fb23b-124">이 cmdlet이 webhooks를 가져오는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb23b-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="fb23b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb23b-125">CommonParameters</span></span>
<span data-ttu-id="fb23b-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb23b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb23b-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb23b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb23b-128">입력</span><span class="sxs-lookup"><span data-stu-id="fb23b-128">INPUTS</span></span>

### <span data-ttu-id="fb23b-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fb23b-129">System.String</span></span>

## <span data-ttu-id="fb23b-130">출력</span><span class="sxs-lookup"><span data-stu-id="fb23b-130">OUTPUTS</span></span>

### <span data-ttu-id="fb23b-131">Microsoft Azure. a \*. Webhook</span><span class="sxs-lookup"><span data-stu-id="fb23b-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="fb23b-132">상속자</span><span class="sxs-lookup"><span data-stu-id="fb23b-132">NOTES</span></span>

## <span data-ttu-id="fb23b-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb23b-133">RELATED LINKS</span></span>

[<span data-ttu-id="fb23b-134">새로운 AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="fb23b-134">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="fb23b-135">제거-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="fb23b-135">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="fb23b-136">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="fb23b-136">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)



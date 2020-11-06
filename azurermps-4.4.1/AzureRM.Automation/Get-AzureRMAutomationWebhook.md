---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
ms.openlocfilehash: 1868f7995a8e3f426f8e4657f9e6df638f06662e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533195"
---
# <span data-ttu-id="d1584-101">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="d1584-101">Get-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="d1584-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1584-102">SYNOPSIS</span></span>
<span data-ttu-id="d1584-103">자동화에서 webhooks를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1584-103">Gets webhooks from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1584-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1584-104">SYNTAX</span></span>

### <span data-ttu-id="d1584-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="d1584-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1584-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d1584-106">ByName</span></span>
```
Get-AzureRmAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1584-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="d1584-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1584-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d1584-108">DESCRIPTION</span></span>
<span data-ttu-id="d1584-109">**Get-AzureRmAutomationWebhook** cmdlet은 webhooks를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1584-109">The **Get-AzureRmAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="d1584-110">특정 webhooks를 가져오려면 webhook 이름을 지정 하거나 Azure Automation runbook의 이름을 지정 하 여 연결 된 webhooks를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1584-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="d1584-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d1584-111">EXAMPLES</span></span>

### <span data-ttu-id="d1584-112">예제 1: runbook에 대 한 모든 webhooks 가져오기</span><span class="sxs-lookup"><span data-stu-id="d1584-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="d1584-113">이 명령은 ResourceGroup01 이라는 리소스 그룹에서 AutomationAccount01 이라는 Automation 계정의 Runbook03 이라는 이름의 runbook에 대 한 모든 webhooks를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d1584-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="d1584-114">변수</span><span class="sxs-lookup"><span data-stu-id="d1584-114">PARAMETERS</span></span>

### <span data-ttu-id="d1584-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d1584-115">-AutomationAccountName</span></span>
<span data-ttu-id="d1584-116">이 cmdlet이 webhook을 가져오는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1584-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="d1584-117">-이름</span><span class="sxs-lookup"><span data-stu-id="d1584-117">-Name</span></span>
<span data-ttu-id="d1584-118">이 cmdlet이 가져오는 webhook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1584-118">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d1584-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1584-119">-ResourceGroupName</span></span>
<span data-ttu-id="d1584-120">이 cmdlet이 webhooks를 가져오는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1584-120">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="d1584-121">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="d1584-121">-RunbookName</span></span>
<span data-ttu-id="d1584-122">이 cmdlet이 webhooks를 가져오는 runbook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1584-122">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="d1584-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1584-123">-DefaultProfile</span></span>
<span data-ttu-id="d1584-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1584-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1584-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1584-125">CommonParameters</span></span>
<span data-ttu-id="d1584-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1584-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1584-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1584-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1584-128">입력</span><span class="sxs-lookup"><span data-stu-id="d1584-128">INPUTS</span></span>

## <span data-ttu-id="d1584-129">출력</span><span class="sxs-lookup"><span data-stu-id="d1584-129">OUTPUTS</span></span>

### <span data-ttu-id="d1584-130">Microsoft Azure. a \*. Webhook</span><span class="sxs-lookup"><span data-stu-id="d1584-130">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="d1584-131">상속자</span><span class="sxs-lookup"><span data-stu-id="d1584-131">NOTES</span></span>

## <span data-ttu-id="d1584-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1584-132">RELATED LINKS</span></span>

[<span data-ttu-id="d1584-133">새로운 AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="d1584-133">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="d1584-134">제거-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="d1584-134">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="d1584-135">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="d1584-135">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)



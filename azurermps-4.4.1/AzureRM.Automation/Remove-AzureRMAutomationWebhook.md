---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
ms.openlocfilehash: f191176433a5ac12507d2b29a6d52c73a1d61e88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531853"
---
# <span data-ttu-id="38238-101">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="38238-101">Remove-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="38238-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38238-102">SYNOPSIS</span></span>
<span data-ttu-id="38238-103">자동화 runbook에서 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="38238-103">Removes a webhook from an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38238-104">구문과</span><span class="sxs-lookup"><span data-stu-id="38238-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationWebhook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38238-105">설명은</span><span class="sxs-lookup"><span data-stu-id="38238-105">DESCRIPTION</span></span>
<span data-ttu-id="38238-106">**AzureRmAutomationWebhook** Cmdlet은 Azure Automation runbook에서 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="38238-106">The **Remove-AzureRmAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="38238-107">Webhook이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="38238-107">The webhook is deleted.</span></span>

## <span data-ttu-id="38238-108">예제의</span><span class="sxs-lookup"><span data-stu-id="38238-108">EXAMPLES</span></span>

### <span data-ttu-id="38238-109">예제 1: webhook 제거</span><span class="sxs-lookup"><span data-stu-id="38238-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzureRmAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="38238-110">이 명령은 AutomationAccount01 이라는 Automation 계정에서 Webhook11 이라는 webhook을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="38238-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="38238-111">명령에서 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38238-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="38238-112">따라서 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38238-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="38238-113">변수</span><span class="sxs-lookup"><span data-stu-id="38238-113">PARAMETERS</span></span>

### <span data-ttu-id="38238-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="38238-114">-AutomationAccountName</span></span>
<span data-ttu-id="38238-115">이 cmdlet이 webhook을 제거 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38238-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="38238-116">-이름</span><span class="sxs-lookup"><span data-stu-id="38238-116">-Name</span></span>
<span data-ttu-id="38238-117">이 cmdlet이 제거 하는 webhook의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38238-117">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="38238-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38238-118">-ResourceGroupName</span></span>
<span data-ttu-id="38238-119">이 cmdlet이 webhook을 제거 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38238-119">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="38238-120">-확인</span><span class="sxs-lookup"><span data-stu-id="38238-120">-Confirm</span></span>
<span data-ttu-id="38238-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="38238-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38238-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38238-122">-WhatIf</span></span>
<span data-ttu-id="38238-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="38238-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38238-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38238-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38238-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38238-125">-DefaultProfile</span></span>
<span data-ttu-id="38238-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38238-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38238-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38238-127">CommonParameters</span></span>
<span data-ttu-id="38238-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="38238-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38238-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38238-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38238-130">입력</span><span class="sxs-lookup"><span data-stu-id="38238-130">INPUTS</span></span>

## <span data-ttu-id="38238-131">출력</span><span class="sxs-lookup"><span data-stu-id="38238-131">OUTPUTS</span></span>

## <span data-ttu-id="38238-132">상속자</span><span class="sxs-lookup"><span data-stu-id="38238-132">NOTES</span></span>

## <span data-ttu-id="38238-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38238-133">RELATED LINKS</span></span>

[<span data-ttu-id="38238-134">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="38238-134">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="38238-135">새로운 AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="38238-135">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="38238-136">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="38238-136">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)



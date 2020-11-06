---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: b3484b410ef885567010c05660590808f3995308
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530516"
---
# <span data-ttu-id="1448b-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="1448b-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="1448b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1448b-102">SYNOPSIS</span></span>
<span data-ttu-id="1448b-103">경고 규칙에 대 한 전자 메일 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1448b-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1448b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1448b-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1448b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1448b-105">DESCRIPTION</span></span>
<span data-ttu-id="1448b-106">**AzureRmAlertRuleEmail** cmdlet은 경고 규칙에 대 한 전자 메일 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1448b-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="1448b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1448b-107">EXAMPLES</span></span>

### <span data-ttu-id="1448b-108">예제 1: 서비스 소유자를 위한 알림 규칙 만들기 전자 메일 작업</span><span class="sxs-lookup"><span data-stu-id="1448b-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="1448b-109">이 명령은 경고 규칙이 발생 했을 때 해당 서비스 소유자에 게 보낼 알림 규칙 전자 메일 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1448b-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="1448b-110">예제 2: 서비스를 지원 하지 않는 소유자를 위한 알림 규칙 만들기 전자 메일 작업</span><span class="sxs-lookup"><span data-stu-id="1448b-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="1448b-111">이 명령은 지정 된 전자 메일 주소에 대 한 알림 규칙 전자 메일 작업을 만들지만 서비스 소유자에 게는 해당 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1448b-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="1448b-112">예제 3: 서비스 소유자 및 비 서비스 소유자에 대 한 알림 규칙 만들기 전자 메일 작업</span><span class="sxs-lookup"><span data-stu-id="1448b-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="1448b-113">이 명령은 지정 된 주소와 해당 서비스 소유자에 대 한 알림 규칙 전자 메일 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1448b-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="1448b-114">변수</span><span class="sxs-lookup"><span data-stu-id="1448b-114">PARAMETERS</span></span>

### <span data-ttu-id="1448b-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="1448b-115">-CustomEmail</span></span>
<span data-ttu-id="1448b-116">쉼표로 구분 된 전자 메일 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1448b-116">Specifies a list of comma-separated e-mail addresses.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CustomEmails

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1448b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1448b-117">-DefaultProfile</span></span>
<span data-ttu-id="1448b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1448b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1448b-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="1448b-119">-SendToServiceOwner</span></span>
<span data-ttu-id="1448b-120">이 작업이 규칙이 실행 될 때 서비스 소유자에 게 전자 메일을 보내도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1448b-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: SendToServiceOwners

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1448b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1448b-121">CommonParameters</span></span>
<span data-ttu-id="1448b-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1448b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1448b-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1448b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1448b-124">입력</span><span class="sxs-lookup"><span data-stu-id="1448b-124">INPUTS</span></span>

### <span data-ttu-id="1448b-125">않아야</span><span class="sxs-lookup"><span data-stu-id="1448b-125">None</span></span>
<span data-ttu-id="1448b-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1448b-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1448b-127">출력</span><span class="sxs-lookup"><span data-stu-id="1448b-127">OUTPUTS</span></span>

### <span data-ttu-id="1448b-128">Microsoft. 경영진. 관리자. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="1448b-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="1448b-129">상속자</span><span class="sxs-lookup"><span data-stu-id="1448b-129">NOTES</span></span>

## <span data-ttu-id="1448b-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1448b-130">RELATED LINKS</span></span>

[<span data-ttu-id="1448b-131">추가-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="1448b-131">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="1448b-132">추가-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="1448b-132">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="1448b-133">추가-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="1448b-133">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="1448b-134">새로운 AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="1448b-134">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)



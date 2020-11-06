---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: 85479695efee536aac054751fdd5a48d4b5de5ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532248"
---
# <span data-ttu-id="7b7ab-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="7b7ab-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="7b7ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b7ab-102">SYNOPSIS</span></span>
<span data-ttu-id="7b7ab-103">경고 규칙에 대 한 전자 메일 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7b7ab-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b7ab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7b7ab-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmails] <String[]>] [-SendToServiceOwners]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b7ab-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7b7ab-105">DESCRIPTION</span></span>
<span data-ttu-id="7b7ab-106">**AzureRmAlertRuleEmail** cmdlet은 경고 규칙에 대 한 전자 메일 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7b7ab-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="7b7ab-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7b7ab-107">EXAMPLES</span></span>

### <span data-ttu-id="7b7ab-108">예제 1: 서비스 소유자를 위한 알림 규칙 만들기 전자 메일 작업</span><span class="sxs-lookup"><span data-stu-id="7b7ab-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="7b7ab-109">이 명령은 경고 규칙이 발생 했을 때 해당 서비스 소유자에 게 보낼 알림 규칙 전자 메일 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7b7ab-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="7b7ab-110">예제 2: 서비스를 지원 하지 않는 소유자를 위한 알림 규칙 만들기 전자 메일 작업</span><span class="sxs-lookup"><span data-stu-id="7b7ab-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="7b7ab-111">이 명령은 지정 된 전자 메일 주소에 대 한 알림 규칙 전자 메일 작업을 만들지만 서비스 소유자에 게는 해당 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b7ab-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="7b7ab-112">예제 3: 서비스 소유자 및 비 서비스 소유자에 대 한 알림 규칙 만들기 전자 메일 작업</span><span class="sxs-lookup"><span data-stu-id="7b7ab-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.net" -SendToServiceOwners
```

<span data-ttu-id="7b7ab-113">이 명령은 지정 된 주소와 해당 서비스 소유자에 대 한 알림 규칙 전자 메일 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7b7ab-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="7b7ab-114">변수</span><span class="sxs-lookup"><span data-stu-id="7b7ab-114">PARAMETERS</span></span>

### <span data-ttu-id="7b7ab-115">-CustomEmails</span><span class="sxs-lookup"><span data-stu-id="7b7ab-115">-CustomEmails</span></span>
<span data-ttu-id="7b7ab-116">쉼표로 구분 된 전자 메일 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b7ab-116">Specifies a list of comma-separated e-mail addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b7ab-117">-SendToServiceOwners</span><span class="sxs-lookup"><span data-stu-id="7b7ab-117">-SendToServiceOwners</span></span>
<span data-ttu-id="7b7ab-118">이 작업이 규칙이 실행 될 때 서비스 소유자에 게 전자 메일을 보내도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b7ab-118">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b7ab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b7ab-119">-DefaultProfile</span></span>
<span data-ttu-id="7b7ab-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b7ab-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b7ab-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b7ab-121">CommonParameters</span></span>
<span data-ttu-id="7b7ab-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b7ab-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b7ab-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b7ab-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b7ab-124">입력</span><span class="sxs-lookup"><span data-stu-id="7b7ab-124">INPUTS</span></span>

## <span data-ttu-id="7b7ab-125">출력</span><span class="sxs-lookup"><span data-stu-id="7b7ab-125">OUTPUTS</span></span>

### <span data-ttu-id="7b7ab-126">Microsoft. 경영진. 관리자. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="7b7ab-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="7b7ab-127">상속자</span><span class="sxs-lookup"><span data-stu-id="7b7ab-127">NOTES</span></span>

## <span data-ttu-id="7b7ab-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b7ab-128">RELATED LINKS</span></span>

[<span data-ttu-id="7b7ab-129">추가-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="7b7ab-129">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="7b7ab-130">추가-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="7b7ab-130">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="7b7ab-131">추가-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="7b7ab-131">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="7b7ab-132">새로운 AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="7b7ab-132">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)



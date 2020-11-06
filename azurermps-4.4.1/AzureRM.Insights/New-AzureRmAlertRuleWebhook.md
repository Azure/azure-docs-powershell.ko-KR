---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
ms.openlocfilehash: ed8b8fe18e6320a297635b09089ff95bd52fe1e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536391"
---
# <span data-ttu-id="aeb9b-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="aeb9b-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="aeb9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeb9b-102">SYNOPSIS</span></span>
<span data-ttu-id="aeb9b-103">알림 규칙 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aeb9b-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aeb9b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aeb9b-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Properties] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aeb9b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aeb9b-105">DESCRIPTION</span></span>
<span data-ttu-id="aeb9b-106">**AzureRmAlertRuleWebhook** cmdlet은 알림 규칙 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aeb9b-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="aeb9b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="aeb9b-107">EXAMPLES</span></span>

### <span data-ttu-id="aeb9b-108">예제 1: 알림 규칙 webhook 만들기</span><span class="sxs-lookup"><span data-stu-id="aeb9b-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="aeb9b-109">이 명령은 서비스 URI만 지정 하 여 알림 규칙 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aeb9b-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="aeb9b-110">예제 2: 하나의 속성을 사용 하 여 webhook 만들기</span><span class="sxs-lookup"><span data-stu-id="aeb9b-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="aeb9b-111">이 명령은 하나의 속성이 있는 Contoso.com에 대 한 알림 규칙 webhook을 만든 다음이를 $Actual 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeb9b-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="aeb9b-112">변수</span><span class="sxs-lookup"><span data-stu-id="aeb9b-112">PARAMETERS</span></span>

### <span data-ttu-id="aeb9b-113">-속성</span><span class="sxs-lookup"><span data-stu-id="aeb9b-113">-Properties</span></span>
<span data-ttu-id="aeb9b-114">@ (Property1 = ' value1 ',.... 형식으로 속성 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeb9b-114">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb9b-115">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="aeb9b-115">-ServiceUri</span></span>
<span data-ttu-id="aeb9b-116">서비스 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeb9b-116">Specifies the service URI.</span></span>

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

### <span data-ttu-id="aeb9b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeb9b-117">-DefaultProfile</span></span>
<span data-ttu-id="aeb9b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aeb9b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aeb9b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeb9b-119">CommonParameters</span></span>
<span data-ttu-id="aeb9b-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeb9b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeb9b-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeb9b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeb9b-122">입력</span><span class="sxs-lookup"><span data-stu-id="aeb9b-122">INPUTS</span></span>

## <span data-ttu-id="aeb9b-123">출력</span><span class="sxs-lookup"><span data-stu-id="aeb9b-123">OUTPUTS</span></span>

### <span data-ttu-id="aeb9b-124">RuleWebhookAction를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeb9b-124">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="aeb9b-125">상속자</span><span class="sxs-lookup"><span data-stu-id="aeb9b-125">NOTES</span></span>

## <span data-ttu-id="aeb9b-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aeb9b-126">RELATED LINKS</span></span>

[<span data-ttu-id="aeb9b-127">추가-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="aeb9b-127">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="aeb9b-128">추가-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="aeb9b-128">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="aeb9b-129">추가-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="aeb9b-129">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="aeb9b-130">새로운 AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="aeb9b-130">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="aeb9b-131">새로운 AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="aeb9b-131">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)



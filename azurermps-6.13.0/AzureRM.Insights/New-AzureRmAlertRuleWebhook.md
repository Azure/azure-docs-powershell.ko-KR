---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
ms.openlocfilehash: 619219a300bb1b7317ea4c8c5fce442d43b74ff1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529569"
---
# <span data-ttu-id="3d5d4-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="3d5d4-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="3d5d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="3d5d4-103">알림 규칙 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3d5d4-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d5d4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d5d4-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d5d4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3d5d4-105">DESCRIPTION</span></span>
<span data-ttu-id="3d5d4-106">**AzureRmAlertRuleWebhook** cmdlet은 알림 규칙 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3d5d4-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="3d5d4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3d5d4-107">EXAMPLES</span></span>

### <span data-ttu-id="3d5d4-108">예제 1: 알림 규칙 webhook 만들기</span><span class="sxs-lookup"><span data-stu-id="3d5d4-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="3d5d4-109">이 명령은 서비스 URI만 지정 하 여 알림 규칙 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3d5d4-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="3d5d4-110">예제 2: 하나의 속성을 사용 하 여 webhook 만들기</span><span class="sxs-lookup"><span data-stu-id="3d5d4-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="3d5d4-111">이 명령은 하나의 속성이 있는 Contoso.com에 대 한 알림 규칙 webhook을 만든 다음이를 $Actual 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5d4-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="3d5d4-112">변수</span><span class="sxs-lookup"><span data-stu-id="3d5d4-112">PARAMETERS</span></span>

### <span data-ttu-id="3d5d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d5d4-113">-DefaultProfile</span></span>
<span data-ttu-id="3d5d4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3d5d4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d5d4-115">-속성</span><span class="sxs-lookup"><span data-stu-id="3d5d4-115">-Property</span></span>
<span data-ttu-id="3d5d4-116">@ (Property1 = ' value1 ',.... 형식으로 속성 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5d4-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="3d5d4-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="3d5d4-117">-ServiceUri</span></span>
<span data-ttu-id="3d5d4-118">서비스 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5d4-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="3d5d4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d5d4-119">CommonParameters</span></span>
<span data-ttu-id="3d5d4-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5d4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d5d4-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d5d4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d5d4-122">입력</span><span class="sxs-lookup"><span data-stu-id="3d5d4-122">INPUTS</span></span>

### <span data-ttu-id="3d5d4-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3d5d4-123">System.String</span></span>

### <span data-ttu-id="3d5d4-124">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="3d5d4-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3d5d4-125">출력</span><span class="sxs-lookup"><span data-stu-id="3d5d4-125">OUTPUTS</span></span>

### <span data-ttu-id="3d5d4-126">RuleWebhookAction를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d5d4-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="3d5d4-127">상속자</span><span class="sxs-lookup"><span data-stu-id="3d5d4-127">NOTES</span></span>

## <span data-ttu-id="3d5d4-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d5d4-128">RELATED LINKS</span></span>

[<span data-ttu-id="3d5d4-129">추가-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="3d5d4-129">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="3d5d4-130">추가-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="3d5d4-130">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="3d5d4-131">추가-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="3d5d4-131">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="3d5d4-132">새로운 AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="3d5d4-132">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="3d5d4-133">새로운 AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="3d5d4-133">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 03459cedbebaeba46331edf7aeb9a7972711912a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034575"
---
# <span data-ttu-id="a0b13-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="a0b13-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="a0b13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0b13-102">SYNOPSIS</span></span>
<span data-ttu-id="a0b13-103">알림 규칙 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0b13-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="a0b13-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0b13-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0b13-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a0b13-105">DESCRIPTION</span></span>
<span data-ttu-id="a0b13-106">**AzAlertRuleWebhook** cmdlet은 알림 규칙 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0b13-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="a0b13-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a0b13-107">EXAMPLES</span></span>

### <span data-ttu-id="a0b13-108">예제 1: 알림 규칙 webhook 만들기</span><span class="sxs-lookup"><span data-stu-id="a0b13-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="a0b13-109">이 명령은 서비스 URI만 지정 하 여 알림 규칙 webhook을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a0b13-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="a0b13-110">예제 2: 하나의 속성을 사용 하 여 webhook 만들기</span><span class="sxs-lookup"><span data-stu-id="a0b13-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="a0b13-111">이 명령은 하나의 속성이 있는 Contoso.com에 대 한 알림 규칙 webhook을 만든 다음이를 $Actual 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0b13-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="a0b13-112">변수</span><span class="sxs-lookup"><span data-stu-id="a0b13-112">PARAMETERS</span></span>

### <span data-ttu-id="a0b13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0b13-113">-DefaultProfile</span></span>
<span data-ttu-id="a0b13-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a0b13-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0b13-115">-속성</span><span class="sxs-lookup"><span data-stu-id="a0b13-115">-Property</span></span>
<span data-ttu-id="a0b13-116">@ (Property1 = ' value1 ',.... 형식으로 속성 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0b13-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="a0b13-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="a0b13-117">-ServiceUri</span></span>
<span data-ttu-id="a0b13-118">서비스 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0b13-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="a0b13-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0b13-119">CommonParameters</span></span>
<span data-ttu-id="a0b13-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0b13-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0b13-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a0b13-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0b13-122">입력</span><span class="sxs-lookup"><span data-stu-id="a0b13-122">INPUTS</span></span>

### <span data-ttu-id="a0b13-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a0b13-123">System.String</span></span>

### <span data-ttu-id="a0b13-124">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="a0b13-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a0b13-125">출력</span><span class="sxs-lookup"><span data-stu-id="a0b13-125">OUTPUTS</span></span>

### <span data-ttu-id="a0b13-126">RuleWebhookAction를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0b13-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="a0b13-127">상속자</span><span class="sxs-lookup"><span data-stu-id="a0b13-127">NOTES</span></span>

## <span data-ttu-id="a0b13-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0b13-128">RELATED LINKS</span></span>

[<span data-ttu-id="a0b13-129">추가-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="a0b13-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="a0b13-130">추가-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="a0b13-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="a0b13-131">추가-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="a0b13-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="a0b13-132">새로운 AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="a0b13-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="a0b13-133">새로운 AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="a0b13-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)



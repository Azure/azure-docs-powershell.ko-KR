---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 8410ca475ed17376e01a526512d758c4712f2726
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411282"
---
# <span data-ttu-id="d8d02-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="d8d02-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="d8d02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8d02-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d02-103">경고 규칙 웹후크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8d02-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="d8d02-104">구문</span><span class="sxs-lookup"><span data-stu-id="d8d02-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8d02-105">설명</span><span class="sxs-lookup"><span data-stu-id="d8d02-105">DESCRIPTION</span></span>
<span data-ttu-id="d8d02-106">**New-AzAlertRuleWebhook** cmdlet은 경고 규칙 웹후크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8d02-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="d8d02-107">예제</span><span class="sxs-lookup"><span data-stu-id="d8d02-107">EXAMPLES</span></span>

### <span data-ttu-id="d8d02-108">예제 1: 경고 규칙 웹후크 만들기</span><span class="sxs-lookup"><span data-stu-id="d8d02-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="d8d02-109">이 명령은 서비스 URI만 지정하여 경고 규칙 웹후크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8d02-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="d8d02-110">예제 2: 하나의 속성으로 웹후크 만들기</span><span class="sxs-lookup"><span data-stu-id="d8d02-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="d8d02-111">이 명령은 하나의 속성이 있는 Contoso.com 대한 경고 규칙 웹후크를 만든 다음 $Actual 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d02-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="d8d02-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8d02-112">PARAMETERS</span></span>

### <span data-ttu-id="d8d02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d02-113">-DefaultProfile</span></span>
<span data-ttu-id="d8d02-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d8d02-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8d02-115">-Property</span><span class="sxs-lookup"><span data-stu-id="d8d02-115">-Property</span></span>
<span data-ttu-id="d8d02-116">@(property1 = 'value1',....) 형식의 속성 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d02-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="d8d02-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="d8d02-117">-ServiceUri</span></span>
<span data-ttu-id="d8d02-118">서비스 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d02-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="d8d02-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d02-119">CommonParameters</span></span>
<span data-ttu-id="d8d02-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d02-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d02-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d8d02-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d02-122">입력</span><span class="sxs-lookup"><span data-stu-id="d8d02-122">INPUTS</span></span>

### <span data-ttu-id="d8d02-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d8d02-123">System.String</span></span>

### <span data-ttu-id="d8d02-124">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d8d02-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d8d02-125">출력</span><span class="sxs-lookup"><span data-stu-id="d8d02-125">OUTPUTS</span></span>

### <span data-ttu-id="d8d02-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="d8d02-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="d8d02-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d8d02-127">NOTES</span></span>

## <span data-ttu-id="d8d02-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8d02-128">RELATED LINKS</span></span>


[<span data-ttu-id="d8d02-129">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="d8d02-129">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="d8d02-130">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="d8d02-130">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="d8d02-131">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="d8d02-131">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="d8d02-132">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="d8d02-132">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)



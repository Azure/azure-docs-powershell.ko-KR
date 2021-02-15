---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 7d9ed01346c04974fb43d7e3b233badb7a185dc2
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100396033"
---
# <span data-ttu-id="5e957-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="5e957-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="5e957-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e957-102">SYNOPSIS</span></span>
<span data-ttu-id="5e957-103">경고 규칙에 대한 전자 메일 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e957-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="5e957-104">구문</span><span class="sxs-lookup"><span data-stu-id="5e957-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e957-105">설명</span><span class="sxs-lookup"><span data-stu-id="5e957-105">DESCRIPTION</span></span>
<span data-ttu-id="5e957-106">**New-AzAlertRuleEmail** cmdlet은 경고 규칙에 대한 전자 메일 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e957-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="5e957-107">예제</span><span class="sxs-lookup"><span data-stu-id="5e957-107">EXAMPLES</span></span>

### <span data-ttu-id="5e957-108">예제 1: 서비스 소유자에 대한 경고 규칙 전자 메일 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="5e957-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="5e957-109">이 명령은 경고 규칙이 실행된 경우 해당 서비스 소유자에 대해 보낼 경고 규칙 전자 메일 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e957-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="5e957-110">예제 2: 비 서비스 소유자에 대한 경고 규칙 전자 메일 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="5e957-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="5e957-111">이 명령은 지정된 전자 메일 주소에 대한 경고 규칙 전자 메일 작업을 만들고 서비스 소유자에 대한 작업은 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e957-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="5e957-112">예제 3: 서비스 소유자 및 비 서비스 소유자에 대한 경고 규칙 전자 메일 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="5e957-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="5e957-113">이 명령은 지정된 주소 및 해당 서비스 소유자에 대한 경고 규칙 전자 메일 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e957-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="5e957-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e957-114">PARAMETERS</span></span>

### <span data-ttu-id="5e957-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="5e957-115">-CustomEmail</span></span>
<span data-ttu-id="5e957-116">콤마로 구분된 전자 메일 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e957-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="5e957-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e957-117">-DefaultProfile</span></span>
<span data-ttu-id="5e957-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5e957-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e957-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="5e957-119">-SendToServiceOwner</span></span>
<span data-ttu-id="5e957-120">규칙이 발생하면 이 작업이 서비스 소유자에게 전자 메일을 보내고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e957-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="5e957-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e957-121">CommonParameters</span></span>
<span data-ttu-id="5e957-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e957-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e957-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5e957-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e957-124">입력</span><span class="sxs-lookup"><span data-stu-id="5e957-124">INPUTS</span></span>

### <span data-ttu-id="5e957-125">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5e957-125">System.String[]</span></span>

### <span data-ttu-id="5e957-126">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5e957-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5e957-127">출력</span><span class="sxs-lookup"><span data-stu-id="5e957-127">OUTPUTS</span></span>

### <span data-ttu-id="5e957-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="5e957-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="5e957-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5e957-129">NOTES</span></span>

## <span data-ttu-id="5e957-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e957-130">RELATED LINKS</span></span>


[<span data-ttu-id="5e957-131">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="5e957-131">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="5e957-132">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="5e957-132">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="5e957-133">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="5e957-133">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)



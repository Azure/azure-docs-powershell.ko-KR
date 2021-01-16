---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 010698183dec206002c0966fb8f37d629d24794a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338133"
---
# <span data-ttu-id="8d282-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="8d282-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="8d282-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d282-102">SYNOPSIS</span></span>
<span data-ttu-id="8d282-103">자동 조정 전자 메일 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d282-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="8d282-104">구문</span><span class="sxs-lookup"><span data-stu-id="8d282-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d282-105">설명</span><span class="sxs-lookup"><span data-stu-id="8d282-105">DESCRIPTION</span></span>
<span data-ttu-id="8d282-106">**New-AzAutoscaleNotification** cmdlet은 자동 크기 조정에 대한 이메일 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d282-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="8d282-107">예제</span><span class="sxs-lookup"><span data-stu-id="8d282-107">EXAMPLES</span></span>

### <span data-ttu-id="8d282-108">예제 1: 자동 조정 전자 메일 알림 만들기</span><span class="sxs-lookup"><span data-stu-id="8d282-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="8d282-109">이 명령은 지정된 두 주소에 대한 자동 자동 조정 전자 메일 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d282-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="8d282-110">예제 2: 구독 관리자에 대한 자동 조정 전자 메일 알림 만들기</span><span class="sxs-lookup"><span data-stu-id="8d282-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="8d282-111">이 명령은 구독 관리자에 대한 자동 자동 조정 전자 메일 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d282-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="8d282-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d282-112">PARAMETERS</span></span>

### <span data-ttu-id="8d282-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="8d282-113">-CustomEmail</span></span>
<span data-ttu-id="8d282-114">콤마로 구분된 전자 메일 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8d282-114">Specifies a comma-separated list of email addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d282-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d282-115">-DefaultProfile</span></span>
<span data-ttu-id="8d282-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8d282-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d282-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="8d282-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="8d282-118">이 작업이 구독 관리자에게 전자 메일 알림을 보내고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d282-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="8d282-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="8d282-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="8d282-120">이 작업이 구독 공동 관리자에게 전자 메일 알림을 전송하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8d282-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="8d282-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="8d282-121">-Webhook</span></span>
<span data-ttu-id="8d282-122">자동 조정 웹후크의 콤마로 구분된 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8d282-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d282-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d282-123">CommonParameters</span></span>
<span data-ttu-id="8d282-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8d282-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d282-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8d282-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d282-126">입력</span><span class="sxs-lookup"><span data-stu-id="8d282-126">INPUTS</span></span>

### <span data-ttu-id="8d282-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span><span class="sxs-lookup"><span data-stu-id="8d282-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="8d282-128">System.String[]</span><span class="sxs-lookup"><span data-stu-id="8d282-128">System.String[]</span></span>

### <span data-ttu-id="8d282-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8d282-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8d282-130">출력</span><span class="sxs-lookup"><span data-stu-id="8d282-130">OUTPUTS</span></span>

### <span data-ttu-id="8d282-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="8d282-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="8d282-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8d282-132">NOTES</span></span>

## <span data-ttu-id="8d282-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d282-133">RELATED LINKS</span></span>

[<span data-ttu-id="8d282-134">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="8d282-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)



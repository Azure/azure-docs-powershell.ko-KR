---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 010698183dec206002c0966fb8f37d629d24794a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211804"
---
# <span data-ttu-id="b475c-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="b475c-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="b475c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b475c-102">SYNOPSIS</span></span>
<span data-ttu-id="b475c-103">자동 크기 조정 전자 메일 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b475c-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="b475c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b475c-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b475c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b475c-105">DESCRIPTION</span></span>
<span data-ttu-id="b475c-106">**AzAutoscaleNotification** Cmdlet은 자동 크기 조정에 대 한 전자 메일 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b475c-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="b475c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b475c-107">EXAMPLES</span></span>

### <span data-ttu-id="b475c-108">예제 1: 자동 크기 조정 전자 메일 알림 만들기</span><span class="sxs-lookup"><span data-stu-id="b475c-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="b475c-109">이 명령은 지정 된 두 주소에 대 한 Autosacale 전자 메일 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b475c-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="b475c-110">예제 2: 구독 관리자에 대 한 자동 크기 조정 전자 메일 알림 만들기</span><span class="sxs-lookup"><span data-stu-id="b475c-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="b475c-111">이 명령은 구독 관리자에 대 한 Autosacale 전자 메일 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b475c-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="b475c-112">변수</span><span class="sxs-lookup"><span data-stu-id="b475c-112">PARAMETERS</span></span>

### <span data-ttu-id="b475c-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="b475c-113">-CustomEmail</span></span>
<span data-ttu-id="b475c-114">쉼표로 구분 된 전자 메일 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b475c-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="b475c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b475c-115">-DefaultProfile</span></span>
<span data-ttu-id="b475c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b475c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b475c-117">-모든 기능 구독 관리자</span><span class="sxs-lookup"><span data-stu-id="b475c-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="b475c-118">이 작업이 구독 관리자에 게 전자 메일 알림을 보내도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b475c-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="b475c-119">-모든 권한</span><span class="sxs-lookup"><span data-stu-id="b475c-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="b475c-120">이 작업이 구독 공동 관리자에 게 전자 메일 알림을 보내도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b475c-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="b475c-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="b475c-121">-Webhook</span></span>
<span data-ttu-id="b475c-122">자동 크기 조정 webhooks 쉼표로 구분 된 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b475c-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="b475c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b475c-123">CommonParameters</span></span>
<span data-ttu-id="b475c-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b475c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b475c-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b475c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b475c-126">입력</span><span class="sxs-lookup"><span data-stu-id="b475c-126">INPUTS</span></span>

### <span data-ttu-id="b475c-127">WebhookNotification [] (으)로 보기</span><span class="sxs-lookup"><span data-stu-id="b475c-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="b475c-128">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="b475c-128">System.String[]</span></span>

### <span data-ttu-id="b475c-129">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b475c-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b475c-130">출력</span><span class="sxs-lookup"><span data-stu-id="b475c-130">OUTPUTS</span></span>

### <span data-ttu-id="b475c-131">AutoscaleNotification를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="b475c-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="b475c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="b475c-132">NOTES</span></span>

## <span data-ttu-id="b475c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b475c-133">RELATED LINKS</span></span>

[<span data-ttu-id="b475c-134">새로운 AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="b475c-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)



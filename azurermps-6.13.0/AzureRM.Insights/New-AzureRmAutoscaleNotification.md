---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: e550341d0bd5a5d2f4e26e4ac736fab9831b67c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529568"
---
# <span data-ttu-id="3aee4-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="3aee4-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="3aee4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3aee4-102">SYNOPSIS</span></span>
<span data-ttu-id="3aee4-103">자동 크기 조정 전자 메일 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3aee4-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3aee4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3aee4-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3aee4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3aee4-105">DESCRIPTION</span></span>
<span data-ttu-id="3aee4-106">**AzureRmAutoscaleNotification** Cmdlet은 자동 크기 조정에 대 한 전자 메일 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3aee4-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="3aee4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3aee4-107">EXAMPLES</span></span>

### <span data-ttu-id="3aee4-108">예제 1: 자동 크기 조정 전자 메일 알림 만들기</span><span class="sxs-lookup"><span data-stu-id="3aee4-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="3aee4-109">이 명령은 지정 된 두 주소에 대 한 Autosacale 전자 메일 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3aee4-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="3aee4-110">예제 2: 구독 관리자에 대 한 자동 크기 조정 전자 메일 알림 만들기</span><span class="sxs-lookup"><span data-stu-id="3aee4-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="3aee4-111">이 명령은 구독 관리자에 대 한 Autosacale 전자 메일 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3aee4-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="3aee4-112">변수</span><span class="sxs-lookup"><span data-stu-id="3aee4-112">PARAMETERS</span></span>

### <span data-ttu-id="3aee4-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="3aee4-113">-CustomEmail</span></span>
<span data-ttu-id="3aee4-114">쉼표로 구분 된 전자 메일 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aee4-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="3aee4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aee4-115">-DefaultProfile</span></span>
<span data-ttu-id="3aee4-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3aee4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3aee4-117">-모든 기능 구독 관리자</span><span class="sxs-lookup"><span data-stu-id="3aee4-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="3aee4-118">이 작업이 구독 관리자에 게 전자 메일 알림을 보내도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aee4-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="3aee4-119">-모든 권한</span><span class="sxs-lookup"><span data-stu-id="3aee4-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="3aee4-120">이 작업이 구독 공동 관리자에 게 전자 메일 알림을 보내도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aee4-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="3aee4-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="3aee4-121">-Webhook</span></span>
<span data-ttu-id="3aee4-122">자동 크기 조정 webhooks 쉼표로 구분 된 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aee4-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="3aee4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aee4-123">CommonParameters</span></span>
<span data-ttu-id="3aee4-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aee4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aee4-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3aee4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aee4-126">입력</span><span class="sxs-lookup"><span data-stu-id="3aee4-126">INPUTS</span></span>

### <span data-ttu-id="3aee4-127">WebhookNotification [] (으)로 보기</span><span class="sxs-lookup"><span data-stu-id="3aee4-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="3aee4-128">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="3aee4-128">System.String[]</span></span>

### <span data-ttu-id="3aee4-129">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="3aee4-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3aee4-130">출력</span><span class="sxs-lookup"><span data-stu-id="3aee4-130">OUTPUTS</span></span>

### <span data-ttu-id="3aee4-131">AutoscaleNotification를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="3aee4-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="3aee4-132">상속자</span><span class="sxs-lookup"><span data-stu-id="3aee4-132">NOTES</span></span>

## <span data-ttu-id="3aee4-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3aee4-133">RELATED LINKS</span></span>

[<span data-ttu-id="3aee4-134">새로운 AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="3aee4-134">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)



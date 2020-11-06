---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: f6791d2cc962f0bb0db038ad8c5391425c09bfbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536387"
---
# <span data-ttu-id="0e87e-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="0e87e-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="0e87e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e87e-102">SYNOPSIS</span></span>
<span data-ttu-id="0e87e-103">자동 크기 조정 전자 메일 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e87e-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e87e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e87e-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhooks] <WebhookNotification[]>] [[-CustomEmails] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e87e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0e87e-105">DESCRIPTION</span></span>
<span data-ttu-id="0e87e-106">**AzureRmAutoscaleNotification** Cmdlet은 자동 크기 조정에 대 한 전자 메일 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e87e-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="0e87e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0e87e-107">EXAMPLES</span></span>

### <span data-ttu-id="0e87e-108">예제 1: 자동 크기 조정 전자 메일 알림 만들기</span><span class="sxs-lookup"><span data-stu-id="0e87e-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="0e87e-109">이 명령은 지정 된 두 주소에 대 한 Autosacale 전자 메일 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e87e-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="0e87e-110">예제 2: 구독 관리자에 대 한 자동 크기 조정 전자 메일 알림 만들기</span><span class="sxs-lookup"><span data-stu-id="0e87e-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="0e87e-111">이 명령은 구독 관리자에 대 한 Autosacale 전자 메일 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e87e-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="0e87e-112">변수</span><span class="sxs-lookup"><span data-stu-id="0e87e-112">PARAMETERS</span></span>

### <span data-ttu-id="0e87e-113">-CustomEmails</span><span class="sxs-lookup"><span data-stu-id="0e87e-113">-CustomEmails</span></span>
<span data-ttu-id="0e87e-114">쉼표로 구분 된 전자 메일 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e87e-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="0e87e-115">-모든 기능 구독 관리자</span><span class="sxs-lookup"><span data-stu-id="0e87e-115">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="0e87e-116">이 작업이 구독 관리자에 게 전자 메일 알림을 보내도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e87e-116">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="0e87e-117">-모든 것이 공동 관리자</span><span class="sxs-lookup"><span data-stu-id="0e87e-117">-SendEmailToSubscriptionCoAdministrators</span></span>
<span data-ttu-id="0e87e-118">이 작업이 구독 공동 관리자에 게 전자 메일 알림을 보내도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e87e-118">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="0e87e-119">-Webhooks</span><span class="sxs-lookup"><span data-stu-id="0e87e-119">-Webhooks</span></span>
<span data-ttu-id="0e87e-120">자동 크기 조정 webhooks 쉼표로 구분 된 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e87e-120">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="0e87e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e87e-121">-DefaultProfile</span></span>
<span data-ttu-id="0e87e-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e87e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e87e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e87e-123">CommonParameters</span></span>
<span data-ttu-id="0e87e-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e87e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e87e-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e87e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e87e-126">입력</span><span class="sxs-lookup"><span data-stu-id="0e87e-126">INPUTS</span></span>

## <span data-ttu-id="0e87e-127">출력</span><span class="sxs-lookup"><span data-stu-id="0e87e-127">OUTPUTS</span></span>

### <span data-ttu-id="0e87e-128">AutoscaleNotification를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e87e-128">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="0e87e-129">상속자</span><span class="sxs-lookup"><span data-stu-id="0e87e-129">NOTES</span></span>

## <span data-ttu-id="0e87e-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e87e-130">RELATED LINKS</span></span>

[<span data-ttu-id="0e87e-131">새로운 AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="0e87e-131">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)



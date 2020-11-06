---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 70816649b33cd91c7d378b3588b443e4dd5b8fe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530115"
---
# <span data-ttu-id="a477b-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="a477b-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="a477b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a477b-102">SYNOPSIS</span></span>
<span data-ttu-id="a477b-103">자격 증명 모음에 대 한 Azure Site Recovery 알림 설정 (전자 메일 알림)을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a477b-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a477b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a477b-104">SYNTAX</span></span>

### <span data-ttu-id="a477b-105">Set (기본값)</span><span class="sxs-lookup"><span data-stu-id="a477b-105">Set (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a477b-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="a477b-106">EmailToSubscriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a477b-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="a477b-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a477b-108">설정할</span><span class="sxs-lookup"><span data-stu-id="a477b-108">Disable</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a477b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a477b-109">DESCRIPTION</span></span>
<span data-ttu-id="a477b-110">**AzureRmRecoveryServicesAsrNotificationSetting** cmdlet은 자격 증명 모음에 대 한 Azure Site Recovery 알림 설정 (전자 메일 알림)을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a477b-110">The **Set-AzureRmRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="a477b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a477b-111">EXAMPLES</span></span>

### <span data-ttu-id="a477b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a477b-112">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="a477b-113">알림을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a477b-113">Disable notification.</span></span>

### <span data-ttu-id="a477b-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="a477b-114">Example 2</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="a477b-115">사용자 지정 전자 메일 주소 및 구독 소유자에 대 한 알림을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a477b-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="a477b-116">변수</span><span class="sxs-lookup"><span data-stu-id="a477b-116">PARAMETERS</span></span>

### <span data-ttu-id="a477b-117">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="a477b-117">-CustomEmailAddress</span></span>
<span data-ttu-id="a477b-118">전자 메일로 전송 되는 알림/알림</span><span class="sxs-lookup"><span data-stu-id="a477b-118">Alert / Notification sent to emails.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a477b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a477b-119">-DefaultProfile</span></span>
<span data-ttu-id="a477b-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a477b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a477b-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="a477b-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="a477b-122">Switch 매개 변수 구독 소유자에 게 알림을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a477b-122">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEmailToSubcriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a477b-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="a477b-123">-DisableNotification</span></span>
<span data-ttu-id="a477b-124">모든 알림을 사용 하지 않도록 설정 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="a477b-124">Flag to disable all notification.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a477b-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="a477b-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="a477b-126">Switch 매개 변수 구독 소유자에 게 알림을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a477b-126">Switch paramter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmailToSubscriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a477b-127">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="a477b-127">-LocaleID</span></span>
<span data-ttu-id="a477b-128">사용자에 게/notifcation에 대 한 알림 전자 메일 언어 (microsoft에서 지원 되는 문화권 코드).</span><span class="sxs-lookup"><span data-stu-id="a477b-128">Email language of alert /notifcation to user(supported culture codes from microsoft).</span></span> 

```yaml
Type: System.String
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a477b-129">-확인</span><span class="sxs-lookup"><span data-stu-id="a477b-129">-Confirm</span></span>
<span data-ttu-id="a477b-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a477b-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a477b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a477b-131">-WhatIf</span></span>
<span data-ttu-id="a477b-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a477b-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a477b-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a477b-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a477b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a477b-134">CommonParameters</span></span>
<span data-ttu-id="a477b-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a477b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a477b-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a477b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a477b-137">입력</span><span class="sxs-lookup"><span data-stu-id="a477b-137">INPUTS</span></span>

### <span data-ttu-id="a477b-138">않아야</span><span class="sxs-lookup"><span data-stu-id="a477b-138">None</span></span>

## <span data-ttu-id="a477b-139">출력</span><span class="sxs-lookup"><span data-stu-id="a477b-139">OUTPUTS</span></span>

### <span data-ttu-id="a477b-140">System.webserver. t e r ' 1 [[SiteRecovery] Recoveryralertsetting, Microsoft Azure. SiteRecovery, Version = 0.1.1.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="a477b-140">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a477b-141">상속자</span><span class="sxs-lookup"><span data-stu-id="a477b-141">NOTES</span></span>

## <span data-ttu-id="a477b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a477b-142">RELATED LINKS</span></span>

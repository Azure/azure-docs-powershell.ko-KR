---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: c7821ddfd07b17a77c482a770b28672ccd664cb4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214699"
---
# <span data-ttu-id="6f92d-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="6f92d-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="6f92d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f92d-102">SYNOPSIS</span></span>
<span data-ttu-id="6f92d-103">자격 증명 모음에 대 한 Azure Site Recovery 알림 설정 (전자 메일 알림)을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f92d-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="6f92d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f92d-104">SYNTAX</span></span>

### <span data-ttu-id="6f92d-105">Set (기본값)</span><span class="sxs-lookup"><span data-stu-id="6f92d-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f92d-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="6f92d-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f92d-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="6f92d-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f92d-108">설정할</span><span class="sxs-lookup"><span data-stu-id="6f92d-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f92d-109">설명은</span><span class="sxs-lookup"><span data-stu-id="6f92d-109">DESCRIPTION</span></span>
<span data-ttu-id="6f92d-110">**AzRecoveryServicesAsrNotificationSetting** cmdlet은 자격 증명 모음에 대 한 Azure Site Recovery 알림 설정 (전자 메일 알림)을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f92d-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="6f92d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="6f92d-111">EXAMPLES</span></span>

### <span data-ttu-id="6f92d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="6f92d-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="6f92d-113">알림을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f92d-113">Disable notification.</span></span>

### <span data-ttu-id="6f92d-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="6f92d-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="6f92d-115">사용자 지정 전자 메일 주소 및 구독 소유자에 대 한 알림을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f92d-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="6f92d-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="6f92d-116">Example 3</span></span>

<span data-ttu-id="6f92d-117">자격 증명 모음에 대 한 Azure Site Recovery 알림 설정 (전자 메일 알림)을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f92d-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="6f92d-118">생성</span><span class="sxs-lookup"><span data-stu-id="6f92d-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="6f92d-119">변수</span><span class="sxs-lookup"><span data-stu-id="6f92d-119">PARAMETERS</span></span>

### <span data-ttu-id="6f92d-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="6f92d-120">-CustomEmailAddress</span></span>
<span data-ttu-id="6f92d-121">전자 메일로 전송 되는 알림/알림</span><span class="sxs-lookup"><span data-stu-id="6f92d-121">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="6f92d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f92d-122">-DefaultProfile</span></span>
<span data-ttu-id="6f92d-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f92d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f92d-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="6f92d-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="6f92d-125">Switch 매개 변수 구독 소유자에 게 알림을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f92d-125">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="6f92d-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="6f92d-126">-DisableNotification</span></span>
<span data-ttu-id="6f92d-127">모든 알림을 사용 하지 않도록 설정 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="6f92d-127">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="6f92d-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="6f92d-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="6f92d-129">Switch 매개 변수 구독 소유자에 게 알림을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f92d-129">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="6f92d-130">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="6f92d-130">-LocaleID</span></span>
<span data-ttu-id="6f92d-131">사용자에 게 알림/알림 전자 메일 언어 (microsoft에서 지원 되는 문화권 코드).</span><span class="sxs-lookup"><span data-stu-id="6f92d-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="6f92d-132">-확인</span><span class="sxs-lookup"><span data-stu-id="6f92d-132">-Confirm</span></span>
<span data-ttu-id="6f92d-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f92d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f92d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f92d-134">-WhatIf</span></span>
<span data-ttu-id="6f92d-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6f92d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f92d-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f92d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f92d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f92d-137">CommonParameters</span></span>
<span data-ttu-id="6f92d-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f92d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f92d-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6f92d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f92d-140">입력</span><span class="sxs-lookup"><span data-stu-id="6f92d-140">INPUTS</span></span>

### <span data-ttu-id="6f92d-141">않아야</span><span class="sxs-lookup"><span data-stu-id="6f92d-141">None</span></span>

## <span data-ttu-id="6f92d-142">출력</span><span class="sxs-lookup"><span data-stu-id="6f92d-142">OUTPUTS</span></span>

### <span data-ttu-id="6f92d-143">SiteRecovery를 통한 Recoveryralertsetting 설정</span><span class="sxs-lookup"><span data-stu-id="6f92d-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="6f92d-144">상속자</span><span class="sxs-lookup"><span data-stu-id="6f92d-144">NOTES</span></span>

## <span data-ttu-id="6f92d-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f92d-145">RELATED LINKS</span></span>

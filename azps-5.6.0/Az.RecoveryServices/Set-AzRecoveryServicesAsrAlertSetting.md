---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 049e1667fec5aef4f12a9912a4b9669364095b0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997472"
---
# <span data-ttu-id="b48de-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="b48de-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="b48de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b48de-102">SYNOPSIS</span></span>
<span data-ttu-id="b48de-103">자격 증명 모음에 대한 Azure Site Recovery 알림 설정(전자 메일 알림)을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="b48de-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="b48de-104">구문</span><span class="sxs-lookup"><span data-stu-id="b48de-104">SYNTAX</span></span>

### <span data-ttu-id="b48de-105">설정(기본값)</span><span class="sxs-lookup"><span data-stu-id="b48de-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b48de-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="b48de-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b48de-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="b48de-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b48de-108">사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="b48de-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b48de-109">설명</span><span class="sxs-lookup"><span data-stu-id="b48de-109">DESCRIPTION</span></span>
<span data-ttu-id="b48de-110">**Set-AzRecoveryServicesAsrNotificationSetting** cmdlet은 자격 증명 모음에 대한 Azure Site Recovery 알림 설정(전자 메일 알림)을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="b48de-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="b48de-111">예제</span><span class="sxs-lookup"><span data-stu-id="b48de-111">EXAMPLES</span></span>

### <span data-ttu-id="b48de-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="b48de-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="b48de-113">알림을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b48de-113">Disable notification.</span></span>

### <span data-ttu-id="b48de-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="b48de-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="b48de-115">사용자 지정 전자 메일 주소 및 구독 소유자에 대한 알림을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b48de-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="b48de-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="b48de-116">Example 3</span></span>

<span data-ttu-id="b48de-117">자격 증명 모음에 대한 Azure Site Recovery 알림 설정(전자 메일 알림)을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="b48de-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="b48de-118">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="b48de-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="b48de-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b48de-119">PARAMETERS</span></span>

### <span data-ttu-id="b48de-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="b48de-120">-CustomEmailAddress</span></span>
<span data-ttu-id="b48de-121">전자 메일로 전송된 경고/알림입니다.</span><span class="sxs-lookup"><span data-stu-id="b48de-121">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="b48de-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b48de-122">-DefaultProfile</span></span>
<span data-ttu-id="b48de-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b48de-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b48de-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="b48de-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="b48de-125">스위치 매개 변수는 구독 소유자에게 알림을 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b48de-125">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="b48de-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="b48de-126">-DisableNotification</span></span>
<span data-ttu-id="b48de-127">플래그를 지정하여 모든 알림을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b48de-127">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="b48de-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="b48de-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="b48de-129">스위치 매개 변수는 구독 소유자에게 알림을 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b48de-129">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="b48de-130">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="b48de-130">-LocaleID</span></span>
<span data-ttu-id="b48de-131">사용자에게 경고/알림의 전자 메일 언어(Microsoft에서 지원되는 문화권 코드).</span><span class="sxs-lookup"><span data-stu-id="b48de-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="b48de-132">-확인</span><span class="sxs-lookup"><span data-stu-id="b48de-132">-Confirm</span></span>
<span data-ttu-id="b48de-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b48de-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b48de-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b48de-134">-WhatIf</span></span>
<span data-ttu-id="b48de-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b48de-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b48de-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b48de-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b48de-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b48de-137">CommonParameters</span></span>
<span data-ttu-id="b48de-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b48de-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b48de-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b48de-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b48de-140">입력</span><span class="sxs-lookup"><span data-stu-id="b48de-140">INPUTS</span></span>

### <span data-ttu-id="b48de-141">없음</span><span class="sxs-lookup"><span data-stu-id="b48de-141">None</span></span>

## <span data-ttu-id="b48de-142">출력</span><span class="sxs-lookup"><span data-stu-id="b48de-142">OUTPUTS</span></span>

### <span data-ttu-id="b48de-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="b48de-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="b48de-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b48de-144">NOTES</span></span>

## <span data-ttu-id="b48de-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b48de-145">RELATED LINKS</span></span>

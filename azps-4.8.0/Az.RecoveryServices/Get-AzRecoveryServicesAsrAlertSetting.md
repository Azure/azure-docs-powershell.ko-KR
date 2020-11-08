---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 2c1d5254d8705d6511d25038e64107a8199496fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047703"
---
# <span data-ttu-id="8303e-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="8303e-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="8303e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8303e-102">SYNOPSIS</span></span>
<span data-ttu-id="8303e-103">자격 증명 모음에 대 한 구성 된 Azure Site Recovery 알림 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8303e-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="8303e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8303e-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8303e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8303e-105">DESCRIPTION</span></span>
<span data-ttu-id="8303e-106">**AzRecoveryServicesAsrAlertSetting** cmdlet은 자격 증명 모음에 대 한 구성 된 Azure Site Recovery 알림 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8303e-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="8303e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8303e-107">EXAMPLES</span></span>

### <span data-ttu-id="8303e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8303e-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="8303e-109">Azure Site Recovery에 대 한 알림/알림 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8303e-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="8303e-110">변수</span><span class="sxs-lookup"><span data-stu-id="8303e-110">PARAMETERS</span></span>

### <span data-ttu-id="8303e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8303e-111">-DefaultProfile</span></span>
<span data-ttu-id="8303e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8303e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8303e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8303e-113">CommonParameters</span></span>
<span data-ttu-id="8303e-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8303e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8303e-115">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8303e-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8303e-116">입력</span><span class="sxs-lookup"><span data-stu-id="8303e-116">INPUTS</span></span>

### <span data-ttu-id="8303e-117">않아야</span><span class="sxs-lookup"><span data-stu-id="8303e-117">None</span></span>

## <span data-ttu-id="8303e-118">출력</span><span class="sxs-lookup"><span data-stu-id="8303e-118">OUTPUTS</span></span>

### <span data-ttu-id="8303e-119">SiteRecovery를 통한 Recoveryralertsetting 설정</span><span class="sxs-lookup"><span data-stu-id="8303e-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="8303e-120">상속자</span><span class="sxs-lookup"><span data-stu-id="8303e-120">NOTES</span></span>

## <span data-ttu-id="8303e-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8303e-121">RELATED LINKS</span></span>

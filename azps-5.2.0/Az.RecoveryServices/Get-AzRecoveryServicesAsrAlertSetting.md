---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 2c1d5254d8705d6511d25038e64107a8199496fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345110"
---
# <span data-ttu-id="6149b-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="6149b-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="6149b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6149b-102">SYNOPSIS</span></span>
<span data-ttu-id="6149b-103">자격 증명 모음에 대해 구성된 Azure Site Recovery 알림 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6149b-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="6149b-104">구문</span><span class="sxs-lookup"><span data-stu-id="6149b-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6149b-105">설명</span><span class="sxs-lookup"><span data-stu-id="6149b-105">DESCRIPTION</span></span>
<span data-ttu-id="6149b-106">**Get-AzRecoveryServicesAsrAlertSetting** cmdlet은 자격 증명 모음에 대해 구성된 Azure Site Recovery 알림 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6149b-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="6149b-107">예제</span><span class="sxs-lookup"><span data-stu-id="6149b-107">EXAMPLES</span></span>

### <span data-ttu-id="6149b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6149b-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="6149b-109">Azure Site Recovery에 대한 경고/알림 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6149b-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="6149b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6149b-110">PARAMETERS</span></span>

### <span data-ttu-id="6149b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6149b-111">-DefaultProfile</span></span>
<span data-ttu-id="6149b-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6149b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6149b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6149b-113">CommonParameters</span></span>
<span data-ttu-id="6149b-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6149b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6149b-115">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6149b-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6149b-116">입력</span><span class="sxs-lookup"><span data-stu-id="6149b-116">INPUTS</span></span>

### <span data-ttu-id="6149b-117">없음</span><span class="sxs-lookup"><span data-stu-id="6149b-117">None</span></span>

## <span data-ttu-id="6149b-118">출력</span><span class="sxs-lookup"><span data-stu-id="6149b-118">OUTPUTS</span></span>

### <span data-ttu-id="6149b-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="6149b-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="6149b-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6149b-120">NOTES</span></span>

## <span data-ttu-id="6149b-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6149b-121">RELATED LINKS</span></span>

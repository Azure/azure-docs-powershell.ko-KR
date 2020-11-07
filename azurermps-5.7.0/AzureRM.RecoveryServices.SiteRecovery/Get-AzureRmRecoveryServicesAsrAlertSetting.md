---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: d1da03455fad47d889269c0d961def70df6837e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703247"
---
# <span data-ttu-id="56f6f-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="56f6f-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="56f6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="56f6f-103">자격 증명 모음에 대 한 구성 된 Azure Site Recovery 알림 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56f6f-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56f6f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56f6f-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56f6f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="56f6f-105">DESCRIPTION</span></span>
<span data-ttu-id="56f6f-106">**AzureRmRecoveryServicesAsrAlertSetting** cmdlet은 자격 증명 모음에 대 한 구성 된 Azure Site Recovery 알림 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56f6f-106">The **Get-AzureRmRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="56f6f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="56f6f-107">EXAMPLES</span></span>

### <span data-ttu-id="56f6f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="56f6f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="56f6f-109">Azure Site Recovery에 대 한 알림/알림 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56f6f-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="56f6f-110">변수</span><span class="sxs-lookup"><span data-stu-id="56f6f-110">PARAMETERS</span></span>

### <span data-ttu-id="56f6f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f6f-111">-DefaultProfile</span></span>
<span data-ttu-id="56f6f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56f6f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f6f-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f6f-113">CommonParameters</span></span>
<span data-ttu-id="56f6f-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56f6f-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f6f-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56f6f-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f6f-116">입력</span><span class="sxs-lookup"><span data-stu-id="56f6f-116">INPUTS</span></span>

### <span data-ttu-id="56f6f-117">않아야</span><span class="sxs-lookup"><span data-stu-id="56f6f-117">None</span></span>

## <span data-ttu-id="56f6f-118">출력</span><span class="sxs-lookup"><span data-stu-id="56f6f-118">OUTPUTS</span></span>

### <span data-ttu-id="56f6f-119">System.webserver. t e r ' 1 [[SiteRecovery] Recoveryralertsetting, Microsoft Azure. SiteRecovery, Version = 0.1.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="56f6f-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="56f6f-120">상속자</span><span class="sxs-lookup"><span data-stu-id="56f6f-120">NOTES</span></span>

## <span data-ttu-id="56f6f-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56f6f-121">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: e7ce712102ffbb74fd8f19eed544642af5a6ebce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699745"
---
# <span data-ttu-id="53658-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="53658-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="53658-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53658-102">SYNOPSIS</span></span>
<span data-ttu-id="53658-103">자격 증명 모음에 대 한 구성 된 Azure Site Recovery 알림 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="53658-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="53658-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53658-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53658-105">설명은</span><span class="sxs-lookup"><span data-stu-id="53658-105">DESCRIPTION</span></span>
<span data-ttu-id="53658-106">**AzRecoveryServicesAsrAlertSetting** cmdlet은 자격 증명 모음에 대 한 구성 된 Azure Site Recovery 알림 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="53658-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="53658-107">예제의</span><span class="sxs-lookup"><span data-stu-id="53658-107">EXAMPLES</span></span>

### <span data-ttu-id="53658-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="53658-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="53658-109">Azure Site Recovery에 대 한 알림/알림 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="53658-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="53658-110">변수</span><span class="sxs-lookup"><span data-stu-id="53658-110">PARAMETERS</span></span>

### <span data-ttu-id="53658-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53658-111">-DefaultProfile</span></span>
<span data-ttu-id="53658-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53658-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53658-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53658-113">CommonParameters</span></span>
<span data-ttu-id="53658-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53658-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53658-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53658-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53658-116">입력</span><span class="sxs-lookup"><span data-stu-id="53658-116">INPUTS</span></span>

### <span data-ttu-id="53658-117">않아야</span><span class="sxs-lookup"><span data-stu-id="53658-117">None</span></span>

## <span data-ttu-id="53658-118">출력</span><span class="sxs-lookup"><span data-stu-id="53658-118">OUTPUTS</span></span>

### <span data-ttu-id="53658-119">SiteRecovery를 통한 Recoveryralertsetting 설정</span><span class="sxs-lookup"><span data-stu-id="53658-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="53658-120">상속자</span><span class="sxs-lookup"><span data-stu-id="53658-120">NOTES</span></span>

## <span data-ttu-id="53658-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53658-121">RELATED LINKS</span></span>

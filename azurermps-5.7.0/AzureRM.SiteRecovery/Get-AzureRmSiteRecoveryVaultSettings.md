---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 56F63287-0247-4921-9C99-E581E075F4D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvaultsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettings.md
ms.openlocfilehash: ef0ee9f4b2c068f5484932fa74da73e6f2a99585
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534619"
---
# <span data-ttu-id="5043a-101">Get-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="5043a-101">Get-AzureRmSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="5043a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5043a-102">SYNOPSIS</span></span>
<span data-ttu-id="5043a-103">현재 사이트 복구 자격 증명 모음에 대 한 설정 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5043a-103">Gets settings information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5043a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5043a-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVaultSettings [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5043a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5043a-105">DESCRIPTION</span></span>
<span data-ttu-id="5043a-106">**AzureRmSiteRecoveryVaultSettings** cmdlet은 현재 Azure Site Recovery 자격 증명 모음과 관련 된 설정 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5043a-106">The **Get-AzureRmSiteRecoveryVaultSettings** cmdlet gets settings information related to the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="5043a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5043a-107">EXAMPLES</span></span>

## <span data-ttu-id="5043a-108">변수</span><span class="sxs-lookup"><span data-stu-id="5043a-108">PARAMETERS</span></span>

### <span data-ttu-id="5043a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5043a-109">-DefaultProfile</span></span>
<span data-ttu-id="5043a-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5043a-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5043a-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5043a-111">CommonParameters</span></span>
<span data-ttu-id="5043a-112">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5043a-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5043a-113">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5043a-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5043a-114">입력</span><span class="sxs-lookup"><span data-stu-id="5043a-114">INPUTS</span></span>

### <span data-ttu-id="5043a-115">않아야</span><span class="sxs-lookup"><span data-stu-id="5043a-115">None</span></span>
<span data-ttu-id="5043a-116">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5043a-116">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5043a-117">출력</span><span class="sxs-lookup"><span data-stu-id="5043a-117">OUTPUTS</span></span>

### <span data-ttu-id="5043a-118">SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="5043a-118">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="5043a-119">상속자</span><span class="sxs-lookup"><span data-stu-id="5043a-119">NOTES</span></span>

## <span data-ttu-id="5043a-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5043a-120">RELATED LINKS</span></span>

[<span data-ttu-id="5043a-121">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="5043a-121">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)

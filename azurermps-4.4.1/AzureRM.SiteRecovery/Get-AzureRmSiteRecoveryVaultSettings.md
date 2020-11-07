---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 56F63287-0247-4921-9C99-E581E075F4D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVaultSettings.md
ms.openlocfilehash: e17b5cea1c26ccf63c6c9347b19ef0f8dc0be1b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703617"
---
# <span data-ttu-id="c444c-101">Get-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="c444c-101">Get-AzureRmSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="c444c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c444c-102">SYNOPSIS</span></span>
<span data-ttu-id="c444c-103">현재 사이트 복구 자격 증명 모음에 대 한 설정 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c444c-103">Gets settings information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c444c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c444c-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVaultSettings [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c444c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c444c-105">DESCRIPTION</span></span>
<span data-ttu-id="c444c-106">**AzureRmSiteRecoveryVaultSettings** cmdlet은 현재 Azure Site Recovery 자격 증명 모음과 관련 된 설정 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c444c-106">The **Get-AzureRmSiteRecoveryVaultSettings** cmdlet gets settings information related to the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="c444c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c444c-107">EXAMPLES</span></span>

## <span data-ttu-id="c444c-108">변수</span><span class="sxs-lookup"><span data-stu-id="c444c-108">PARAMETERS</span></span>

### <span data-ttu-id="c444c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c444c-109">-DefaultProfile</span></span>
<span data-ttu-id="c444c-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c444c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c444c-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c444c-111">CommonParameters</span></span>
<span data-ttu-id="c444c-112">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c444c-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c444c-113">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c444c-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c444c-114">입력</span><span class="sxs-lookup"><span data-stu-id="c444c-114">INPUTS</span></span>

## <span data-ttu-id="c444c-115">출력</span><span class="sxs-lookup"><span data-stu-id="c444c-115">OUTPUTS</span></span>

### <span data-ttu-id="c444c-116">SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="c444c-116">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="c444c-117">상속자</span><span class="sxs-lookup"><span data-stu-id="c444c-117">NOTES</span></span>

## <span data-ttu-id="c444c-118">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c444c-118">RELATED LINKS</span></span>

[<span data-ttu-id="c444c-119">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="c444c-119">Set-AzureRmSiteRecoveryVaultSettings</span></span>](./Set-AzureRmSiteRecoveryVaultSettings.md)

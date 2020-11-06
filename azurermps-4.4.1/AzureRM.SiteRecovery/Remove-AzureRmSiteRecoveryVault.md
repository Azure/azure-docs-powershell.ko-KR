---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 63E9894A-3AC5-4397-9B21-D0A72EBA5C4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: e5d85c6cdc30ff00d2a35bba6d1a79119cbaddd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532920"
---
# <span data-ttu-id="56bc7-101">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="56bc7-101">Remove-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="56bc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56bc7-102">SYNOPSIS</span></span>
<span data-ttu-id="56bc7-103">사이트 복구 자격 증명 모음을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="56bc7-103">Removes a Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56bc7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56bc7-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryVault -Vault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56bc7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="56bc7-105">DESCRIPTION</span></span>
<span data-ttu-id="56bc7-106">**AzureRmSiteRecoveryVault** Cmdlet은 Azure Site Recovery 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="56bc7-106">The **Remove-AzureRmSiteRecoveryVault** cmdlet deletes an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="56bc7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="56bc7-107">EXAMPLES</span></span>

## <span data-ttu-id="56bc7-108">변수</span><span class="sxs-lookup"><span data-stu-id="56bc7-108">PARAMETERS</span></span>

### <span data-ttu-id="56bc7-109">-저장실</span><span class="sxs-lookup"><span data-stu-id="56bc7-109">-Vault</span></span>
<span data-ttu-id="56bc7-110">사이트 복구 자격 증명 모음 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56bc7-110">Specifies the Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56bc7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56bc7-111">-DefaultProfile</span></span>
<span data-ttu-id="56bc7-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56bc7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56bc7-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56bc7-113">CommonParameters</span></span>
<span data-ttu-id="56bc7-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56bc7-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56bc7-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56bc7-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56bc7-116">입력</span><span class="sxs-lookup"><span data-stu-id="56bc7-116">INPUTS</span></span>

### <span data-ttu-id="56bc7-117">ASRVault</span><span class="sxs-lookup"><span data-stu-id="56bc7-117">ASRVault</span></span>
<span data-ttu-id="56bc7-118">' Vault ' 매개 변수는 파이프라인에서 ' ASRVault ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="56bc7-118">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="56bc7-119">출력</span><span class="sxs-lookup"><span data-stu-id="56bc7-119">OUTPUTS</span></span>

## <span data-ttu-id="56bc7-120">상속자</span><span class="sxs-lookup"><span data-stu-id="56bc7-120">NOTES</span></span>

## <span data-ttu-id="56bc7-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56bc7-121">RELATED LINKS</span></span>

[<span data-ttu-id="56bc7-122">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="56bc7-122">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="56bc7-123">새로운 AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="56bc7-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

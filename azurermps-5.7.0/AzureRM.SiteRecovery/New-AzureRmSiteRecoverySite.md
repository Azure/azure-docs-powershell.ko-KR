---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D0336AB5-019F-4EFD-88D2-63E12BA1ED95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 053cd7695768be44cf3cecc5964e037f12f0b84e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531631"
---
# <span data-ttu-id="d7ebd-101">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="d7ebd-101">New-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="d7ebd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ebd-103">사이트 복구 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d7ebd-103">Creates a Site Recovery site.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7ebd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d7ebd-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7ebd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d7ebd-105">DESCRIPTION</span></span>
<span data-ttu-id="d7ebd-106">**AzureRmSiteRecoverySite** cmdlet은 현재 자격 증명 모음에 Azure site Recovery 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d7ebd-106">The **New-AzureRmSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="d7ebd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d7ebd-107">EXAMPLES</span></span>

## <span data-ttu-id="d7ebd-108">변수</span><span class="sxs-lookup"><span data-stu-id="d7ebd-108">PARAMETERS</span></span>

### <span data-ttu-id="d7ebd-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7ebd-109">-DefaultProfile</span></span>
<span data-ttu-id="d7ebd-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7ebd-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7ebd-111">-이름</span><span class="sxs-lookup"><span data-stu-id="d7ebd-111">-Name</span></span>
<span data-ttu-id="d7ebd-112">사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7ebd-112">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ebd-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ebd-113">CommonParameters</span></span>
<span data-ttu-id="d7ebd-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d7ebd-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7ebd-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7ebd-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ebd-116">입력</span><span class="sxs-lookup"><span data-stu-id="d7ebd-116">INPUTS</span></span>

### <span data-ttu-id="d7ebd-117">않아야</span><span class="sxs-lookup"><span data-stu-id="d7ebd-117">None</span></span>
<span data-ttu-id="d7ebd-118">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7ebd-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7ebd-119">출력</span><span class="sxs-lookup"><span data-stu-id="d7ebd-119">OUTPUTS</span></span>

## <span data-ttu-id="d7ebd-120">상속자</span><span class="sxs-lookup"><span data-stu-id="d7ebd-120">NOTES</span></span>

## <span data-ttu-id="d7ebd-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7ebd-121">RELATED LINKS</span></span>

[<span data-ttu-id="d7ebd-122">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="d7ebd-122">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="d7ebd-123">제거-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="d7ebd-123">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)

---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: D0336AB5-019F-4EFD-88D2-63E12BA1ED95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 7f8dfed861abd9d426a72c5d66f7c41b4efc947e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527268"
---
# <span data-ttu-id="60cae-101">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="60cae-101">New-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="60cae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60cae-102">SYNOPSIS</span></span>
<span data-ttu-id="60cae-103">사이트 복구 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60cae-103">Creates a Site Recovery site.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60cae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60cae-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60cae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="60cae-105">DESCRIPTION</span></span>
<span data-ttu-id="60cae-106">**AzureRmSiteRecoverySite** cmdlet은 현재 자격 증명 모음에 Azure site Recovery 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60cae-106">The **New-AzureRmSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="60cae-107">예제의</span><span class="sxs-lookup"><span data-stu-id="60cae-107">EXAMPLES</span></span>

## <span data-ttu-id="60cae-108">변수</span><span class="sxs-lookup"><span data-stu-id="60cae-108">PARAMETERS</span></span>

### <span data-ttu-id="60cae-109">-이름</span><span class="sxs-lookup"><span data-stu-id="60cae-109">-Name</span></span>
<span data-ttu-id="60cae-110">사이트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60cae-110">Specifies the name of the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60cae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60cae-111">-DefaultProfile</span></span>
<span data-ttu-id="60cae-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="60cae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60cae-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60cae-113">CommonParameters</span></span>
<span data-ttu-id="60cae-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60cae-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60cae-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60cae-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60cae-116">입력</span><span class="sxs-lookup"><span data-stu-id="60cae-116">INPUTS</span></span>

## <span data-ttu-id="60cae-117">출력</span><span class="sxs-lookup"><span data-stu-id="60cae-117">OUTPUTS</span></span>

## <span data-ttu-id="60cae-118">상속자</span><span class="sxs-lookup"><span data-stu-id="60cae-118">NOTES</span></span>

## <span data-ttu-id="60cae-119">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60cae-119">RELATED LINKS</span></span>

[<span data-ttu-id="60cae-120">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="60cae-120">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="60cae-121">제거-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="60cae-121">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)

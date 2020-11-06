---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
ms.openlocfilehash: 3ad44ba1edcec844dcb542defb1baf294aeaa89b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526260"
---
# <span data-ttu-id="fb012-101">Get-AzureRmCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="fb012-101">Get-AzureRmCdnProfileSsoUrl</span></span>

## <span data-ttu-id="fb012-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb012-102">SYNOPSIS</span></span>
<span data-ttu-id="fb012-103">CDN 프로필의 single sign-on URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb012-103">Gets the single sign-on URL of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb012-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb012-104">SYNTAX</span></span>

### <span data-ttu-id="fb012-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fb012-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb012-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb012-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb012-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fb012-107">DESCRIPTION</span></span>
<span data-ttu-id="fb012-108">**AzureRmCdnProfileSsoUrl** CMDLET은 CDN (Content Delivery Network) 프로필의 SINGLE sign-on URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb012-108">The **Get-AzureRmCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="fb012-109">이 URL은 사용자가 보조 포털에 연결할 수 있도록 하 고 CDN의 추가 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb012-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="fb012-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fb012-110">EXAMPLES</span></span>

## <span data-ttu-id="fb012-111">변수</span><span class="sxs-lookup"><span data-stu-id="fb012-111">PARAMETERS</span></span>

### <span data-ttu-id="fb012-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="fb012-112">-CdnProfile</span></span>
<span data-ttu-id="fb012-113">CDN 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb012-113">Specifies the CDN profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb012-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb012-114">-DefaultProfile</span></span>
<span data-ttu-id="fb012-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fb012-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb012-116">-/Profile</span><span class="sxs-lookup"><span data-stu-id="fb012-116">-ProfileName</span></span>
<span data-ttu-id="fb012-117">CDN 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb012-117">Specifies the name of the CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb012-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb012-118">-ResourceGroupName</span></span>
<span data-ttu-id="fb012-119">프로필이 속한 리소스 그룹 이름의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb012-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb012-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb012-120">CommonParameters</span></span>
<span data-ttu-id="fb012-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb012-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb012-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb012-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb012-123">입력</span><span class="sxs-lookup"><span data-stu-id="fb012-123">INPUTS</span></span>

### <span data-ttu-id="fb012-124">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="fb012-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="fb012-125">매개 변수: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fb012-125">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="fb012-126">출력</span><span class="sxs-lookup"><span data-stu-id="fb012-126">OUTPUTS</span></span>

### <span data-ttu-id="fb012-127">PSSsoUri의. m m.</span><span class="sxs-lookup"><span data-stu-id="fb012-127">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="fb012-128">상속자</span><span class="sxs-lookup"><span data-stu-id="fb012-128">NOTES</span></span>

## <span data-ttu-id="fb012-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb012-129">RELATED LINKS</span></span>

[<span data-ttu-id="fb012-130">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fb012-130">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)



---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: 726e84e1fe43e90ebf16241a017dadb2af5584b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535483"
---
# <span data-ttu-id="5a692-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5a692-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="5a692-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a692-102">SYNOPSIS</span></span>
<span data-ttu-id="5a692-103">CDN 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a692-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a692-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a692-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a692-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5a692-105">DESCRIPTION</span></span>
<span data-ttu-id="5a692-106">**AzureRMCdnProfile** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 프로필 및 관련 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5a692-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="5a692-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5a692-107">EXAMPLES</span></span>

## <span data-ttu-id="5a692-108">변수</span><span class="sxs-lookup"><span data-stu-id="5a692-108">PARAMETERS</span></span>

### <span data-ttu-id="5a692-109">-/Profile</span><span class="sxs-lookup"><span data-stu-id="5a692-109">-ProfileName</span></span>
<span data-ttu-id="5a692-110">프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a692-110">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a692-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a692-111">-ResourceGroupName</span></span>
<span data-ttu-id="5a692-112">프로필이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a692-112">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a692-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a692-113">-DefaultProfile</span></span>
<span data-ttu-id="5a692-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a692-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a692-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a692-115">CommonParameters</span></span>
<span data-ttu-id="5a692-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a692-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a692-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a692-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a692-118">입력</span><span class="sxs-lookup"><span data-stu-id="5a692-118">INPUTS</span></span>

## <span data-ttu-id="5a692-119">출력</span><span class="sxs-lookup"><span data-stu-id="5a692-119">OUTPUTS</span></span>

###  
<span data-ttu-id="5a692-120">이 cmdlet은 profile 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a692-120">This cmdlet returns a profile object.</span></span>

## <span data-ttu-id="5a692-121">상속자</span><span class="sxs-lookup"><span data-stu-id="5a692-121">NOTES</span></span>

## <span data-ttu-id="5a692-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a692-122">RELATED LINKS</span></span>

[<span data-ttu-id="5a692-123">새로운 AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5a692-123">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="5a692-124">제거-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5a692-124">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="5a692-125">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5a692-125">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)



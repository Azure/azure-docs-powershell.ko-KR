---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043685"
---
# <span data-ttu-id="0d108-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0d108-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="0d108-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d108-102">SYNOPSIS</span></span>
<span data-ttu-id="0d108-103">CDN 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d108-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="0d108-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d108-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d108-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0d108-105">DESCRIPTION</span></span>
<span data-ttu-id="0d108-106">**AzCdnProfile** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 프로필 및 관련 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d108-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="0d108-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0d108-107">EXAMPLES</span></span>

## <span data-ttu-id="0d108-108">변수</span><span class="sxs-lookup"><span data-stu-id="0d108-108">PARAMETERS</span></span>

### <span data-ttu-id="0d108-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d108-109">-DefaultProfile</span></span>
<span data-ttu-id="0d108-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0d108-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d108-111">-/Profile</span><span class="sxs-lookup"><span data-stu-id="0d108-111">-ProfileName</span></span>
<span data-ttu-id="0d108-112">프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d108-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="0d108-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d108-113">-ResourceGroupName</span></span>
<span data-ttu-id="0d108-114">프로필이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d108-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="0d108-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d108-115">CommonParameters</span></span>
<span data-ttu-id="0d108-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d108-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d108-117">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0d108-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d108-118">입력</span><span class="sxs-lookup"><span data-stu-id="0d108-118">INPUTS</span></span>

### <span data-ttu-id="0d108-119">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0d108-119">System.String</span></span>

## <span data-ttu-id="0d108-120">출력</span><span class="sxs-lookup"><span data-stu-id="0d108-120">OUTPUTS</span></span>

### <span data-ttu-id="0d108-121">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="0d108-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="0d108-122">상속자</span><span class="sxs-lookup"><span data-stu-id="0d108-122">NOTES</span></span>

## <span data-ttu-id="0d108-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d108-123">RELATED LINKS</span></span>

[<span data-ttu-id="0d108-124">새로운 AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0d108-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="0d108-125">제거-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0d108-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="0d108-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="0d108-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


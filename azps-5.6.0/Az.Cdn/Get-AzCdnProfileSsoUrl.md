---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: c458973a5cff000cab13c4602e1a73234314c0d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963296"
---
# <span data-ttu-id="49676-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="49676-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="49676-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49676-102">SYNOPSIS</span></span>
<span data-ttu-id="49676-103">CDN 프로필의 Single Sign-On URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="49676-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="49676-104">구문</span><span class="sxs-lookup"><span data-stu-id="49676-104">SYNTAX</span></span>

### <span data-ttu-id="49676-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="49676-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49676-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49676-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49676-107">설명</span><span class="sxs-lookup"><span data-stu-id="49676-107">DESCRIPTION</span></span>
<span data-ttu-id="49676-108">**Get-AzCdnProfileSsoUrl** cmdlet은 CDN(Azure Content Delivery Network) 프로필의 Single Sign-On URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="49676-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="49676-109">이 URL을 사용하면 사용자가 보조 포털에 연결하고 CDN의 추가 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="49676-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="49676-110">예제</span><span class="sxs-lookup"><span data-stu-id="49676-110">EXAMPLES</span></span>

## <span data-ttu-id="49676-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="49676-111">PARAMETERS</span></span>

### <span data-ttu-id="49676-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="49676-112">-CdnProfile</span></span>
<span data-ttu-id="49676-113">CDN 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="49676-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="49676-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49676-114">-DefaultProfile</span></span>
<span data-ttu-id="49676-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="49676-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49676-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="49676-116">-ProfileName</span></span>
<span data-ttu-id="49676-117">CDN 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="49676-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="49676-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49676-118">-ResourceGroupName</span></span>
<span data-ttu-id="49676-119">프로필이 속한 리소스 그룹 이름의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="49676-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="49676-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49676-120">CommonParameters</span></span>
<span data-ttu-id="49676-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="49676-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49676-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49676-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49676-123">입력</span><span class="sxs-lookup"><span data-stu-id="49676-123">INPUTS</span></span>

### <span data-ttu-id="49676-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="49676-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="49676-125">출력</span><span class="sxs-lookup"><span data-stu-id="49676-125">OUTPUTS</span></span>

### <span data-ttu-id="49676-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="49676-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="49676-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="49676-127">NOTES</span></span>

## <span data-ttu-id="49676-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49676-128">RELATED LINKS</span></span>

[<span data-ttu-id="49676-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="49676-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)



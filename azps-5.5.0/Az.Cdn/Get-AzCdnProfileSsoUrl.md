---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: 74bc4fae4dd55a85c4aca811819a0348f5df5f2c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181849"
---
# <span data-ttu-id="5678c-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="5678c-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="5678c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5678c-102">SYNOPSIS</span></span>
<span data-ttu-id="5678c-103">CDN 프로필의 Single Sign-On URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5678c-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="5678c-104">구문</span><span class="sxs-lookup"><span data-stu-id="5678c-104">SYNTAX</span></span>

### <span data-ttu-id="5678c-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5678c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5678c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5678c-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5678c-107">설명</span><span class="sxs-lookup"><span data-stu-id="5678c-107">DESCRIPTION</span></span>
<span data-ttu-id="5678c-108">**Get-AzCdnProfileSsoUrl** cmdlet은 Azure CDN(Content Delivery Network) 프로필의 Single Sign-On URL을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5678c-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="5678c-109">이 URL을 사용하면 사용자가 보조 포털에 연결하고 CDN의 추가 기능을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5678c-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="5678c-110">예제</span><span class="sxs-lookup"><span data-stu-id="5678c-110">EXAMPLES</span></span>

## <span data-ttu-id="5678c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5678c-111">PARAMETERS</span></span>

### <span data-ttu-id="5678c-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="5678c-112">-CdnProfile</span></span>
<span data-ttu-id="5678c-113">CDN 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5678c-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="5678c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5678c-114">-DefaultProfile</span></span>
<span data-ttu-id="5678c-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5678c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5678c-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5678c-116">-ProfileName</span></span>
<span data-ttu-id="5678c-117">CDN 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5678c-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="5678c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5678c-118">-ResourceGroupName</span></span>
<span data-ttu-id="5678c-119">프로필이 속한 리소스 그룹 이름의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5678c-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="5678c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5678c-120">CommonParameters</span></span>
<span data-ttu-id="5678c-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5678c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5678c-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5678c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5678c-123">입력</span><span class="sxs-lookup"><span data-stu-id="5678c-123">INPUTS</span></span>

### <span data-ttu-id="5678c-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="5678c-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="5678c-125">출력</span><span class="sxs-lookup"><span data-stu-id="5678c-125">OUTPUTS</span></span>

### <span data-ttu-id="5678c-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="5678c-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="5678c-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5678c-127">NOTES</span></span>

## <span data-ttu-id="5678c-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5678c-128">RELATED LINKS</span></span>

[<span data-ttu-id="5678c-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="5678c-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: 64e9c4bc8f279858c4c889c00eee058aab0cad4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869225"
---
# <span data-ttu-id="d5030-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="d5030-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="d5030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5030-102">SYNOPSIS</span></span>
<span data-ttu-id="d5030-103">CDN 프로필의 single sign-on URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d5030-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="d5030-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5030-104">SYNTAX</span></span>

### <span data-ttu-id="d5030-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d5030-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5030-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5030-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5030-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d5030-107">DESCRIPTION</span></span>
<span data-ttu-id="d5030-108">**AzCdnProfileSsoUrl** CMDLET은 CDN (Content Delivery Network) 프로필의 SINGLE sign-on URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d5030-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="d5030-109">이 URL은 사용자가 보조 포털에 연결할 수 있도록 하 고 CDN의 추가 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5030-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="d5030-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d5030-110">EXAMPLES</span></span>

## <span data-ttu-id="d5030-111">변수</span><span class="sxs-lookup"><span data-stu-id="d5030-111">PARAMETERS</span></span>

### <span data-ttu-id="d5030-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="d5030-112">-CdnProfile</span></span>
<span data-ttu-id="d5030-113">CDN 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5030-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="d5030-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5030-114">-DefaultProfile</span></span>
<span data-ttu-id="d5030-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d5030-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5030-116">-/Profile</span><span class="sxs-lookup"><span data-stu-id="d5030-116">-ProfileName</span></span>
<span data-ttu-id="d5030-117">CDN 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5030-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="d5030-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5030-118">-ResourceGroupName</span></span>
<span data-ttu-id="d5030-119">프로필이 속한 리소스 그룹 이름의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5030-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="d5030-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5030-120">CommonParameters</span></span>
<span data-ttu-id="d5030-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5030-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5030-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5030-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5030-123">입력</span><span class="sxs-lookup"><span data-stu-id="d5030-123">INPUTS</span></span>

### <span data-ttu-id="d5030-124">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="d5030-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="d5030-125">출력</span><span class="sxs-lookup"><span data-stu-id="d5030-125">OUTPUTS</span></span>

### <span data-ttu-id="d5030-126">PSSsoUri의. m m.</span><span class="sxs-lookup"><span data-stu-id="d5030-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="d5030-127">상속자</span><span class="sxs-lookup"><span data-stu-id="d5030-127">NOTES</span></span>

## <span data-ttu-id="d5030-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5030-128">RELATED LINKS</span></span>

[<span data-ttu-id="d5030-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d5030-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)



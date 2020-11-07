---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
ms.openlocfilehash: 2365502bb681cafe8ed7fedb05a4a862e54a3cc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703404"
---
# <span data-ttu-id="e0261-101">Get-AzureRmCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="e0261-101">Get-AzureRmCdnProfileSsoUrl</span></span>

## <span data-ttu-id="e0261-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0261-102">SYNOPSIS</span></span>
<span data-ttu-id="e0261-103">CDN 프로필의 single sign-on URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0261-103">Gets the single sign-on URL of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0261-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e0261-104">SYNTAX</span></span>

### <span data-ttu-id="e0261-105">필드 매개 변수에 대해 설정 되는 매개 변수 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e0261-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0261-106">개체 매개 변수에 대해 설정 되는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e0261-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0261-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e0261-107">DESCRIPTION</span></span>
<span data-ttu-id="e0261-108">**AzureRmCdnProfileSsoUrl** CMDLET은 CDN (Content Delivery Network) 프로필의 SINGLE sign-on URL을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e0261-108">The **Get-AzureRmCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="e0261-109">이 URL은 사용자가 보조 포털에 연결할 수 있도록 하 고 CDN의 추가 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0261-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="e0261-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e0261-110">EXAMPLES</span></span>

## <span data-ttu-id="e0261-111">변수</span><span class="sxs-lookup"><span data-stu-id="e0261-111">PARAMETERS</span></span>

### <span data-ttu-id="e0261-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="e0261-112">-CdnProfile</span></span>
<span data-ttu-id="e0261-113">CDN 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0261-113">Specifies the CDN profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0261-114">-/Profile</span><span class="sxs-lookup"><span data-stu-id="e0261-114">-ProfileName</span></span>
<span data-ttu-id="e0261-115">CDN 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0261-115">Specifies the name of the CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0261-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0261-116">-ResourceGroupName</span></span>
<span data-ttu-id="e0261-117">프로필이 속한 리소스 그룹 이름의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0261-117">Specifies the name of the resource group name to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0261-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0261-118">-DefaultProfile</span></span>
<span data-ttu-id="e0261-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e0261-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0261-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0261-120">CommonParameters</span></span>
<span data-ttu-id="e0261-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0261-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0261-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0261-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0261-123">입력</span><span class="sxs-lookup"><span data-stu-id="e0261-123">INPUTS</span></span>

### <span data-ttu-id="e0261-124">PSProfile</span><span class="sxs-lookup"><span data-stu-id="e0261-124">PSProfile</span></span>
<span data-ttu-id="e0261-125">' CdnProfile ' 매개 변수는 파이프라인에서 ' PSProfile ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0261-125">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="e0261-126">출력</span><span class="sxs-lookup"><span data-stu-id="e0261-126">OUTPUTS</span></span>

###  
<span data-ttu-id="e0261-127">이 cmdlet은 URL을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e0261-127">This cmdlet returns a URL.</span></span>

## <span data-ttu-id="e0261-128">상속자</span><span class="sxs-lookup"><span data-stu-id="e0261-128">NOTES</span></span>

## <span data-ttu-id="e0261-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e0261-129">RELATED LINKS</span></span>

[<span data-ttu-id="e0261-130">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="e0261-130">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)



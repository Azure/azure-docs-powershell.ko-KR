---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: b87963b45010299dcb80c4b1859af8614f845526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527040"
---
# <span data-ttu-id="20998-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="20998-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="20998-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20998-102">SYNOPSIS</span></span>
<span data-ttu-id="20998-103">CDN 사용자 지정 도메인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20998-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20998-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20998-104">SYNTAX</span></span>

### <span data-ttu-id="20998-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="20998-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20998-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20998-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20998-107">설명은</span><span class="sxs-lookup"><span data-stu-id="20998-107">DESCRIPTION</span></span>
<span data-ttu-id="20998-108">**AzureRmCdnCustomDomain** CMDLET은 CDN (Azure Content Delivery Network) 사용자 지정 도메인 및 관련 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="20998-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="20998-109">예제의</span><span class="sxs-lookup"><span data-stu-id="20998-109">EXAMPLES</span></span>

## <span data-ttu-id="20998-110">변수</span><span class="sxs-lookup"><span data-stu-id="20998-110">PARAMETERS</span></span>

### <span data-ttu-id="20998-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="20998-111">-CdnEndpoint</span></span>
<span data-ttu-id="20998-112">사용자 지정 도메인이 멤버인 CDN 끝점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20998-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20998-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="20998-113">-CustomDomainName</span></span>
<span data-ttu-id="20998-114">사용자 지정 도메인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20998-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="20998-115">사용자 지정 도메인의 이름이 사용자 지정 도메인의 호스트 이름과 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="20998-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20998-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20998-116">-DefaultProfile</span></span>
<span data-ttu-id="20998-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="20998-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20998-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="20998-118">-EndpointName</span></span>
<span data-ttu-id="20998-119">사용자 지정 도메인이 속한 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20998-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20998-120">-/Profile</span><span class="sxs-lookup"><span data-stu-id="20998-120">-ProfileName</span></span>
<span data-ttu-id="20998-121">사용자 지정 도메인이 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20998-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20998-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20998-122">-ResourceGroupName</span></span>
<span data-ttu-id="20998-123">사용자 지정 도메인이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20998-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20998-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20998-124">CommonParameters</span></span>
<span data-ttu-id="20998-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20998-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20998-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20998-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20998-127">입력</span><span class="sxs-lookup"><span data-stu-id="20998-127">INPUTS</span></span>

### <span data-ttu-id="20998-128">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="20998-128">PSEndpoint</span></span>
<span data-ttu-id="20998-129">' CdnEndpoint ' 매개 변수는 파이프라인에서 ' PSEndpoint ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="20998-129">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="20998-130">출력</span><span class="sxs-lookup"><span data-stu-id="20998-130">OUTPUTS</span></span>

###  
<span data-ttu-id="20998-131">이 cmdlet은 사용자 지정 도메인 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="20998-131">This cmdlet returns a custom domain object.</span></span>

## <span data-ttu-id="20998-132">상속자</span><span class="sxs-lookup"><span data-stu-id="20998-132">NOTES</span></span>

## <span data-ttu-id="20998-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20998-133">RELATED LINKS</span></span>

[<span data-ttu-id="20998-134">새로운 AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="20998-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="20998-135">제거-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="20998-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)



---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: dcfa0968ac70f7a0abc14ee61ee615bee3aee5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533164"
---
# <span data-ttu-id="17e2f-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="17e2f-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="17e2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="17e2f-103">CDN 사용자 지정 도메인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17e2f-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17e2f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="17e2f-104">SYNTAX</span></span>

### <span data-ttu-id="17e2f-105">필드 매개 변수에 대해 설정 되는 매개 변수 (기본값)</span><span class="sxs-lookup"><span data-stu-id="17e2f-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17e2f-106">개체 매개 변수에 대해 설정 되는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="17e2f-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17e2f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="17e2f-107">DESCRIPTION</span></span>
<span data-ttu-id="17e2f-108">**AzureRmCdnCustomDomain** CMDLET은 CDN (Azure Content Delivery Network) 사용자 지정 도메인 및 관련 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="17e2f-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="17e2f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="17e2f-109">EXAMPLES</span></span>

## <span data-ttu-id="17e2f-110">변수</span><span class="sxs-lookup"><span data-stu-id="17e2f-110">PARAMETERS</span></span>

### <span data-ttu-id="17e2f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="17e2f-111">-CdnEndpoint</span></span>
<span data-ttu-id="17e2f-112">사용자 지정 도메인이 멤버인 CDN 끝점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17e2f-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17e2f-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="17e2f-113">-CustomDomainName</span></span>
<span data-ttu-id="17e2f-114">사용자 지정 도메인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17e2f-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="17e2f-115">사용자 지정 도메인의 이름이 사용자 지정 도메인의 호스트 이름과 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="17e2f-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e2f-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="17e2f-116">-EndpointName</span></span>
<span data-ttu-id="17e2f-117">사용자 지정 도메인이 속한 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17e2f-117">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="17e2f-118">-/Profile</span><span class="sxs-lookup"><span data-stu-id="17e2f-118">-ProfileName</span></span>
<span data-ttu-id="17e2f-119">사용자 지정 도메인이 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17e2f-119">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="17e2f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17e2f-120">-ResourceGroupName</span></span>
<span data-ttu-id="17e2f-121">사용자 지정 도메인이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17e2f-121">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="17e2f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e2f-122">-DefaultProfile</span></span>
<span data-ttu-id="17e2f-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17e2f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17e2f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e2f-124">CommonParameters</span></span>
<span data-ttu-id="17e2f-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17e2f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e2f-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17e2f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e2f-127">입력</span><span class="sxs-lookup"><span data-stu-id="17e2f-127">INPUTS</span></span>

### <span data-ttu-id="17e2f-128">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="17e2f-128">PSEndpoint</span></span>
<span data-ttu-id="17e2f-129">' CdnEndpoint ' 매개 변수는 파이프라인에서 ' PSEndpoint ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="17e2f-129">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="17e2f-130">출력</span><span class="sxs-lookup"><span data-stu-id="17e2f-130">OUTPUTS</span></span>

###  
<span data-ttu-id="17e2f-131">이 cmdlet은 사용자 지정 도메인 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="17e2f-131">This cmdlet returns a custom domain object.</span></span>

## <span data-ttu-id="17e2f-132">상속자</span><span class="sxs-lookup"><span data-stu-id="17e2f-132">NOTES</span></span>

## <span data-ttu-id="17e2f-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17e2f-133">RELATED LINKS</span></span>

[<span data-ttu-id="17e2f-134">새로운 AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="17e2f-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="17e2f-135">제거-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="17e2f-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: 3462e256889dffd086d9fa1d0fb96dba42ed109a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697614"
---
# <span data-ttu-id="634ca-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="634ca-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="634ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="634ca-102">SYNOPSIS</span></span>
<span data-ttu-id="634ca-103">CDN 사용자 지정 도메인을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="634ca-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="634ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="634ca-104">SYNTAX</span></span>

### <span data-ttu-id="634ca-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="634ca-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="634ca-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="634ca-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="634ca-107">설명은</span><span class="sxs-lookup"><span data-stu-id="634ca-107">DESCRIPTION</span></span>
<span data-ttu-id="634ca-108">**AzCdnCustomDomain** CMDLET은 CDN (Azure Content Delivery Network) 사용자 지정 도메인 및 관련 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="634ca-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="634ca-109">예제의</span><span class="sxs-lookup"><span data-stu-id="634ca-109">EXAMPLES</span></span>

## <span data-ttu-id="634ca-110">변수</span><span class="sxs-lookup"><span data-stu-id="634ca-110">PARAMETERS</span></span>

### <span data-ttu-id="634ca-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="634ca-111">-CdnEndpoint</span></span>
<span data-ttu-id="634ca-112">사용자 지정 도메인이 멤버인 CDN 끝점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="634ca-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="634ca-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="634ca-113">-CustomDomainName</span></span>
<span data-ttu-id="634ca-114">사용자 지정 도메인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="634ca-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="634ca-115">사용자 지정 도메인의 이름이 사용자 지정 도메인의 호스트 이름과 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="634ca-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="634ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="634ca-116">-DefaultProfile</span></span>
<span data-ttu-id="634ca-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="634ca-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="634ca-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="634ca-118">-EndpointName</span></span>
<span data-ttu-id="634ca-119">사용자 지정 도메인이 속한 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="634ca-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="634ca-120">-/Profile</span><span class="sxs-lookup"><span data-stu-id="634ca-120">-ProfileName</span></span>
<span data-ttu-id="634ca-121">사용자 지정 도메인이 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="634ca-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="634ca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="634ca-122">-ResourceGroupName</span></span>
<span data-ttu-id="634ca-123">사용자 지정 도메인이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="634ca-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="634ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="634ca-124">CommonParameters</span></span>
<span data-ttu-id="634ca-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="634ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="634ca-126">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="634ca-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="634ca-127">입력</span><span class="sxs-lookup"><span data-stu-id="634ca-127">INPUTS</span></span>

### <span data-ttu-id="634ca-128">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="634ca-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="634ca-129">출력</span><span class="sxs-lookup"><span data-stu-id="634ca-129">OUTPUTS</span></span>

### <span data-ttu-id="634ca-130">PSCustomDomain (.). c.</span><span class="sxs-lookup"><span data-stu-id="634ca-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="634ca-131">상속자</span><span class="sxs-lookup"><span data-stu-id="634ca-131">NOTES</span></span>

## <span data-ttu-id="634ca-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="634ca-132">RELATED LINKS</span></span>

[<span data-ttu-id="634ca-133">새로운 AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="634ca-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="634ca-134">제거-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="634ca-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)



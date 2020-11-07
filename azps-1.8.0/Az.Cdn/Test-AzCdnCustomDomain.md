---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 3ab4e9c673ebea17bbf15d4f978f7c500660060a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869198"
---
# <span data-ttu-id="75df3-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="75df3-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="75df3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75df3-102">SYNOPSIS</span></span>
<span data-ttu-id="75df3-103">사용자 지정 도메인을 끝점에 추가할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="75df3-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="75df3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75df3-104">SYNTAX</span></span>

### <span data-ttu-id="75df3-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="75df3-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75df3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75df3-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75df3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="75df3-107">DESCRIPTION</span></span>
<span data-ttu-id="75df3-108">**테스트 AzCdnCustomDomain** Cmdlet은 CName 매핑의 유효성을 검사 하 여 사용자 지정 도메인을 끝점에 추가할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="75df3-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="75df3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="75df3-109">EXAMPLES</span></span>

## <span data-ttu-id="75df3-110">변수</span><span class="sxs-lookup"><span data-stu-id="75df3-110">PARAMETERS</span></span>

### <span data-ttu-id="75df3-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="75df3-111">-CdnEndpoint</span></span>
<span data-ttu-id="75df3-112">사용자 지정 도메인을 추가 하려는 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75df3-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="75df3-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="75df3-113">-CustomDomainHostName</span></span>
<span data-ttu-id="75df3-114">사용자 지정 도메인의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75df3-114">Specifies the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75df3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75df3-115">-DefaultProfile</span></span>
<span data-ttu-id="75df3-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="75df3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75df3-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="75df3-117">-EndpointName</span></span>
<span data-ttu-id="75df3-118">사용자 지정 도메인을 추가 하려는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75df3-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="75df3-119">-/Profile</span><span class="sxs-lookup"><span data-stu-id="75df3-119">-ProfileName</span></span>
<span data-ttu-id="75df3-120">프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75df3-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="75df3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75df3-121">-ResourceGroupName</span></span>
<span data-ttu-id="75df3-122">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="75df3-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="75df3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75df3-123">CommonParameters</span></span>
<span data-ttu-id="75df3-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75df3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75df3-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75df3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75df3-126">입력</span><span class="sxs-lookup"><span data-stu-id="75df3-126">INPUTS</span></span>

### <span data-ttu-id="75df3-127">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="75df3-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="75df3-128">출력</span><span class="sxs-lookup"><span data-stu-id="75df3-128">OUTPUTS</span></span>

### <span data-ttu-id="75df3-129">PSValidateCustomDomainOutput를 통해 끝점을 보세요.</span><span class="sxs-lookup"><span data-stu-id="75df3-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="75df3-130">상속자</span><span class="sxs-lookup"><span data-stu-id="75df3-130">NOTES</span></span>

## <span data-ttu-id="75df3-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75df3-131">RELATED LINKS</span></span>

[<span data-ttu-id="75df3-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="75df3-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="75df3-133">새로운 AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="75df3-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="75df3-134">제거-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="75df3-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)



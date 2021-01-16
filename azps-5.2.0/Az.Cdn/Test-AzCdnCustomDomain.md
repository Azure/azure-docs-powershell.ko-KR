---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 8ceb1fe02ba4a7d5cf4435ac79d404b331b58ea9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362825"
---
# <span data-ttu-id="fcc63-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="fcc63-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="fcc63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcc63-102">SYNOPSIS</span></span>
<span data-ttu-id="fcc63-103">사용자 지정 도메인을 엔드포인트에 추가할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc63-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="fcc63-104">구문</span><span class="sxs-lookup"><span data-stu-id="fcc63-104">SYNTAX</span></span>

### <span data-ttu-id="fcc63-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fcc63-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcc63-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcc63-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcc63-107">설명</span><span class="sxs-lookup"><span data-stu-id="fcc63-107">DESCRIPTION</span></span>
<span data-ttu-id="fcc63-108">**Test-AzCdnCustomDomain** cmdlet은 CName 매핑의 유효성을 검사하여 사용자 지정 도메인을 엔드포인트에 추가할 수 있는지 여부를 검사합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc63-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="fcc63-109">예제</span><span class="sxs-lookup"><span data-stu-id="fcc63-109">EXAMPLES</span></span>

## <span data-ttu-id="fcc63-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcc63-110">PARAMETERS</span></span>

### <span data-ttu-id="fcc63-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fcc63-111">-CdnEndpoint</span></span>
<span data-ttu-id="fcc63-112">사용자 지정 도메인을 추가할 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc63-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="fcc63-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="fcc63-113">-CustomDomainHostName</span></span>
<span data-ttu-id="fcc63-114">사용자 지정 도메인의 호스트 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc63-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="fcc63-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcc63-115">-DefaultProfile</span></span>
<span data-ttu-id="fcc63-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fcc63-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcc63-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fcc63-117">-EndpointName</span></span>
<span data-ttu-id="fcc63-118">사용자 지정 도메인을 추가할 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc63-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="fcc63-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fcc63-119">-ProfileName</span></span>
<span data-ttu-id="fcc63-120">프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc63-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="fcc63-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcc63-121">-ResourceGroupName</span></span>
<span data-ttu-id="fcc63-122">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc63-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fcc63-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcc63-123">CommonParameters</span></span>
<span data-ttu-id="fcc63-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc63-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcc63-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fcc63-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcc63-126">입력</span><span class="sxs-lookup"><span data-stu-id="fcc63-126">INPUTS</span></span>

### <span data-ttu-id="fcc63-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="fcc63-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="fcc63-128">출력</span><span class="sxs-lookup"><span data-stu-id="fcc63-128">OUTPUTS</span></span>

### <span data-ttu-id="fcc63-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="fcc63-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="fcc63-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fcc63-130">NOTES</span></span>

## <span data-ttu-id="fcc63-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcc63-131">RELATED LINKS</span></span>

[<span data-ttu-id="fcc63-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="fcc63-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="fcc63-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="fcc63-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="fcc63-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="fcc63-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)



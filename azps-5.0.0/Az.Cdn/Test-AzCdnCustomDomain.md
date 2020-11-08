---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 8ceb1fe02ba4a7d5cf4435ac79d404b331b58ea9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219210"
---
# <span data-ttu-id="f3724-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f3724-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="f3724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3724-102">SYNOPSIS</span></span>
<span data-ttu-id="f3724-103">사용자 지정 도메인을 끝점에 추가할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3724-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="f3724-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3724-104">SYNTAX</span></span>

### <span data-ttu-id="f3724-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f3724-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3724-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3724-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3724-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f3724-107">DESCRIPTION</span></span>
<span data-ttu-id="f3724-108">**테스트 AzCdnCustomDomain** Cmdlet은 CName 매핑의 유효성을 검사 하 여 사용자 지정 도메인을 끝점에 추가할 수 있는지 여부를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3724-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="f3724-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f3724-109">EXAMPLES</span></span>

## <span data-ttu-id="f3724-110">변수</span><span class="sxs-lookup"><span data-stu-id="f3724-110">PARAMETERS</span></span>

### <span data-ttu-id="f3724-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f3724-111">-CdnEndpoint</span></span>
<span data-ttu-id="f3724-112">사용자 지정 도메인을 추가 하려는 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3724-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="f3724-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="f3724-113">-CustomDomainHostName</span></span>
<span data-ttu-id="f3724-114">사용자 지정 도메인의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3724-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="f3724-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3724-115">-DefaultProfile</span></span>
<span data-ttu-id="f3724-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f3724-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3724-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f3724-117">-EndpointName</span></span>
<span data-ttu-id="f3724-118">사용자 지정 도메인을 추가 하려는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3724-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="f3724-119">-/Profile</span><span class="sxs-lookup"><span data-stu-id="f3724-119">-ProfileName</span></span>
<span data-ttu-id="f3724-120">프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3724-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="f3724-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3724-121">-ResourceGroupName</span></span>
<span data-ttu-id="f3724-122">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3724-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f3724-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3724-123">CommonParameters</span></span>
<span data-ttu-id="f3724-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3724-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3724-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f3724-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3724-126">입력</span><span class="sxs-lookup"><span data-stu-id="f3724-126">INPUTS</span></span>

### <span data-ttu-id="f3724-127">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f3724-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="f3724-128">출력</span><span class="sxs-lookup"><span data-stu-id="f3724-128">OUTPUTS</span></span>

### <span data-ttu-id="f3724-129">PSValidateCustomDomainOutput를 통해 끝점을 보세요.</span><span class="sxs-lookup"><span data-stu-id="f3724-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="f3724-130">상속자</span><span class="sxs-lookup"><span data-stu-id="f3724-130">NOTES</span></span>

## <span data-ttu-id="f3724-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3724-131">RELATED LINKS</span></span>

[<span data-ttu-id="f3724-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f3724-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="f3724-133">새로운 AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f3724-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="f3724-134">제거-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f3724-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)



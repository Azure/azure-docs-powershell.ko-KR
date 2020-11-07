---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: bc37d6c6c9be6278cc2e27782000ad242ac07a2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697593"
---
# <span data-ttu-id="9144f-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="9144f-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="9144f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9144f-102">SYNOPSIS</span></span>
<span data-ttu-id="9144f-103">CDN 끝점에 대 한 사용자 지정 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9144f-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="9144f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9144f-104">SYNTAX</span></span>

### <span data-ttu-id="9144f-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9144f-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9144f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9144f-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9144f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9144f-107">DESCRIPTION</span></span>
<span data-ttu-id="9144f-108">**AzCdnCustomDomain** CMDLET은 CDN (Content Delivery Network) 끝점에 대 한 사용자 지정 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9144f-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="9144f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9144f-109">EXAMPLES</span></span>

## <span data-ttu-id="9144f-110">변수</span><span class="sxs-lookup"><span data-stu-id="9144f-110">PARAMETERS</span></span>

### <span data-ttu-id="9144f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9144f-111">-CdnEndpoint</span></span>
<span data-ttu-id="9144f-112">사용자 지정 도메인이 추가 되는 CDN 끝점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9144f-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="9144f-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="9144f-113">-CustomDomainName</span></span>
<span data-ttu-id="9144f-114">사용자 지정 도메인의 리소스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9144f-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="9144f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9144f-115">-DefaultProfile</span></span>
<span data-ttu-id="9144f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9144f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9144f-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9144f-117">-EndpointName</span></span>
<span data-ttu-id="9144f-118">끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9144f-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="9144f-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="9144f-119">-HostName</span></span>
<span data-ttu-id="9144f-120">사용자 지정 도메인의 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9144f-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="9144f-121">-/Profile</span><span class="sxs-lookup"><span data-stu-id="9144f-121">-ProfileName</span></span>
<span data-ttu-id="9144f-122">프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9144f-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="9144f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9144f-123">-ResourceGroupName</span></span>
<span data-ttu-id="9144f-124">사용자 지정 도메인이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9144f-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="9144f-125">-확인</span><span class="sxs-lookup"><span data-stu-id="9144f-125">-Confirm</span></span>
<span data-ttu-id="9144f-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9144f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9144f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9144f-127">-WhatIf</span></span>
<span data-ttu-id="9144f-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9144f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9144f-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9144f-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9144f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9144f-130">CommonParameters</span></span>
<span data-ttu-id="9144f-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9144f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9144f-132">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9144f-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9144f-133">입력</span><span class="sxs-lookup"><span data-stu-id="9144f-133">INPUTS</span></span>

### <span data-ttu-id="9144f-134">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="9144f-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="9144f-135">출력</span><span class="sxs-lookup"><span data-stu-id="9144f-135">OUTPUTS</span></span>

### <span data-ttu-id="9144f-136">PSCustomDomain (.). c.</span><span class="sxs-lookup"><span data-stu-id="9144f-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="9144f-137">상속자</span><span class="sxs-lookup"><span data-stu-id="9144f-137">NOTES</span></span>

## <span data-ttu-id="9144f-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9144f-138">RELATED LINKS</span></span>

[<span data-ttu-id="9144f-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="9144f-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="9144f-140">제거-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="9144f-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="9144f-141">테스트-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="9144f-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)



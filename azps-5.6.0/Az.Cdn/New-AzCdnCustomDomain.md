---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: 58e4d922d74f36f6f472cf3bfef8e0d0d45155d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010795"
---
# <span data-ttu-id="ffc85-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ffc85-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="ffc85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffc85-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc85-103">CDN 엔드포인트에 대한 사용자 지정 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ffc85-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="ffc85-104">구문</span><span class="sxs-lookup"><span data-stu-id="ffc85-104">SYNTAX</span></span>

### <span data-ttu-id="ffc85-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ffc85-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffc85-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffc85-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffc85-107">설명</span><span class="sxs-lookup"><span data-stu-id="ffc85-107">DESCRIPTION</span></span>
<span data-ttu-id="ffc85-108">**New-AzCdnCustomDomain** cmdlet은 CDN(Azure Content Delivery Network) 엔드포인트에 대한 사용자 지정 도메인을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ffc85-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="ffc85-109">예제</span><span class="sxs-lookup"><span data-stu-id="ffc85-109">EXAMPLES</span></span>

## <span data-ttu-id="ffc85-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ffc85-110">PARAMETERS</span></span>

### <span data-ttu-id="ffc85-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ffc85-111">-CdnEndpoint</span></span>
<span data-ttu-id="ffc85-112">사용자 지정 도메인이 추가되는 CDN 엔드포인트 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc85-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="ffc85-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="ffc85-113">-CustomDomainName</span></span>
<span data-ttu-id="ffc85-114">사용자 지정 도메인의 리소스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc85-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="ffc85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc85-115">-DefaultProfile</span></span>
<span data-ttu-id="ffc85-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ffc85-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffc85-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ffc85-117">-EndpointName</span></span>
<span data-ttu-id="ffc85-118">엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc85-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="ffc85-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="ffc85-119">-HostName</span></span>
<span data-ttu-id="ffc85-120">사용자 지정 도메인의 호스트 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc85-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="ffc85-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ffc85-121">-ProfileName</span></span>
<span data-ttu-id="ffc85-122">프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc85-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="ffc85-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffc85-123">-ResourceGroupName</span></span>
<span data-ttu-id="ffc85-124">사용자 지정 도메인이 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc85-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="ffc85-125">-확인</span><span class="sxs-lookup"><span data-stu-id="ffc85-125">-Confirm</span></span>
<span data-ttu-id="ffc85-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffc85-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffc85-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffc85-127">-WhatIf</span></span>
<span data-ttu-id="ffc85-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ffc85-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffc85-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc85-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffc85-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc85-130">CommonParameters</span></span>
<span data-ttu-id="ffc85-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc85-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc85-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ffc85-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc85-133">입력</span><span class="sxs-lookup"><span data-stu-id="ffc85-133">INPUTS</span></span>

### <span data-ttu-id="ffc85-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ffc85-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="ffc85-135">출력</span><span class="sxs-lookup"><span data-stu-id="ffc85-135">OUTPUTS</span></span>

### <span data-ttu-id="ffc85-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ffc85-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="ffc85-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ffc85-137">NOTES</span></span>

## <span data-ttu-id="ffc85-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ffc85-138">RELATED LINKS</span></span>

[<span data-ttu-id="ffc85-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ffc85-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="ffc85-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ffc85-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="ffc85-141">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ffc85-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)



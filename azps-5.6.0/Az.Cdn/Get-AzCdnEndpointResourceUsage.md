---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: d39bd2d3a10f1ff8512b54cdf45902fb10f6810d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015408"
---
# <span data-ttu-id="d1576-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="d1576-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="d1576-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1576-102">SYNOPSIS</span></span>
<span data-ttu-id="d1576-103">CDN 엔드포인트의 리소스 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1576-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="d1576-104">구문</span><span class="sxs-lookup"><span data-stu-id="d1576-104">SYNTAX</span></span>

### <span data-ttu-id="d1576-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d1576-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1576-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1576-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1576-107">설명</span><span class="sxs-lookup"><span data-stu-id="d1576-107">DESCRIPTION</span></span>
<span data-ttu-id="d1576-108">{{Description}} 채우기}</span><span class="sxs-lookup"><span data-stu-id="d1576-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="d1576-109">예제</span><span class="sxs-lookup"><span data-stu-id="d1576-109">EXAMPLES</span></span>

### <span data-ttu-id="d1576-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d1576-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d1576-111">{{ 여기에 예제 설명 추가 }}</span><span class="sxs-lookup"><span data-stu-id="d1576-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="d1576-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d1576-112">PARAMETERS</span></span>

### <span data-ttu-id="d1576-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1576-113">-CdnEndpoint</span></span>
<span data-ttu-id="d1576-114">CDN 엔드포인트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d1576-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="d1576-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1576-115">-DefaultProfile</span></span>
<span data-ttu-id="d1576-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d1576-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1576-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d1576-117">-EndpointName</span></span>
<span data-ttu-id="d1576-118">Azure CDN 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1576-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="d1576-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d1576-119">-ProfileName</span></span>
<span data-ttu-id="d1576-120">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1576-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="d1576-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1576-121">-ResourceGroupName</span></span>
<span data-ttu-id="d1576-122">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="d1576-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="d1576-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1576-123">CommonParameters</span></span>
<span data-ttu-id="d1576-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1576-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1576-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1576-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1576-126">입력</span><span class="sxs-lookup"><span data-stu-id="d1576-126">INPUTS</span></span>

### <span data-ttu-id="d1576-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="d1576-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="d1576-128">출력</span><span class="sxs-lookup"><span data-stu-id="d1576-128">OUTPUTS</span></span>

### <span data-ttu-id="d1576-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="d1576-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="d1576-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d1576-130">NOTES</span></span>

## <span data-ttu-id="d1576-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1576-131">RELATED LINKS</span></span>

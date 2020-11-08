---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 7b8773f4e8e0f63404d81c56703181124f6f8ad0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042125"
---
# <span data-ttu-id="e47ba-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="e47ba-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="e47ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e47ba-102">SYNOPSIS</span></span>
<span data-ttu-id="e47ba-103">CDN 끝점의 리소스 사용을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e47ba-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="e47ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e47ba-104">SYNTAX</span></span>

### <span data-ttu-id="e47ba-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e47ba-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e47ba-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e47ba-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e47ba-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e47ba-107">DESCRIPTION</span></span>
<span data-ttu-id="e47ba-108">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="e47ba-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="e47ba-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e47ba-109">EXAMPLES</span></span>

### <span data-ttu-id="e47ba-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e47ba-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e47ba-111">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="e47ba-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="e47ba-112">변수</span><span class="sxs-lookup"><span data-stu-id="e47ba-112">PARAMETERS</span></span>

### <span data-ttu-id="e47ba-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e47ba-113">-CdnEndpoint</span></span>
<span data-ttu-id="e47ba-114">CDN 끝점 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e47ba-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="e47ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e47ba-115">-DefaultProfile</span></span>
<span data-ttu-id="e47ba-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e47ba-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e47ba-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e47ba-117">-EndpointName</span></span>
<span data-ttu-id="e47ba-118">Azure CDN 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e47ba-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="e47ba-119">-/Profile</span><span class="sxs-lookup"><span data-stu-id="e47ba-119">-ProfileName</span></span>
<span data-ttu-id="e47ba-120">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e47ba-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="e47ba-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e47ba-121">-ResourceGroupName</span></span>
<span data-ttu-id="e47ba-122">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="e47ba-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="e47ba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e47ba-123">CommonParameters</span></span>
<span data-ttu-id="e47ba-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e47ba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e47ba-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e47ba-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e47ba-126">입력</span><span class="sxs-lookup"><span data-stu-id="e47ba-126">INPUTS</span></span>

### <span data-ttu-id="e47ba-127">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e47ba-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="e47ba-128">출력</span><span class="sxs-lookup"><span data-stu-id="e47ba-128">OUTPUTS</span></span>

### <span data-ttu-id="e47ba-129">Microsoft. Azure. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="e47ba-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="e47ba-130">상속자</span><span class="sxs-lookup"><span data-stu-id="e47ba-130">NOTES</span></span>

## <span data-ttu-id="e47ba-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e47ba-131">RELATED LINKS</span></span>

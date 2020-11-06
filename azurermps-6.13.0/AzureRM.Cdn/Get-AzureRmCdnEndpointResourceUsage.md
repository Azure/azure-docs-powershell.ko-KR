---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointResourceUsage.md
ms.openlocfilehash: 3fe740fc8643ab6ef4f010feeee57b3339426c21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531003"
---
# <span data-ttu-id="fcd1f-101">Get-AzureRmCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="fcd1f-101">Get-AzureRmCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="fcd1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcd1f-102">SYNOPSIS</span></span>
<span data-ttu-id="fcd1f-103">CDN 끝점의 리소스 사용을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fcd1f-103">Gets the resource usage of a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcd1f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fcd1f-104">SYNTAX</span></span>

### <span data-ttu-id="fcd1f-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fcd1f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcd1f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcd1f-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcd1f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fcd1f-107">DESCRIPTION</span></span>
<span data-ttu-id="fcd1f-108">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="fcd1f-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="fcd1f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fcd1f-109">EXAMPLES</span></span>

### <span data-ttu-id="fcd1f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="fcd1f-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="fcd1f-111">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="fcd1f-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="fcd1f-112">변수</span><span class="sxs-lookup"><span data-stu-id="fcd1f-112">PARAMETERS</span></span>

### <span data-ttu-id="fcd1f-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fcd1f-113">-CdnEndpoint</span></span>
<span data-ttu-id="fcd1f-114">CDN 끝점 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fcd1f-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="fcd1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcd1f-115">-DefaultProfile</span></span>
<span data-ttu-id="fcd1f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fcd1f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcd1f-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fcd1f-117">-EndpointName</span></span>
<span data-ttu-id="fcd1f-118">Azure CDN 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcd1f-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="fcd1f-119">-/Profile</span><span class="sxs-lookup"><span data-stu-id="fcd1f-119">-ProfileName</span></span>
<span data-ttu-id="fcd1f-120">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcd1f-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="fcd1f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcd1f-121">-ResourceGroupName</span></span>
<span data-ttu-id="fcd1f-122">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="fcd1f-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="fcd1f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcd1f-123">CommonParameters</span></span>
<span data-ttu-id="fcd1f-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcd1f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcd1f-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcd1f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcd1f-126">입력</span><span class="sxs-lookup"><span data-stu-id="fcd1f-126">INPUTS</span></span>

### <span data-ttu-id="fcd1f-127">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="fcd1f-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="fcd1f-128">매개 변수: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fcd1f-128">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="fcd1f-129">출력</span><span class="sxs-lookup"><span data-stu-id="fcd1f-129">OUTPUTS</span></span>

### <span data-ttu-id="fcd1f-130">Microsoft. Azure. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="fcd1f-130">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="fcd1f-131">상속자</span><span class="sxs-lookup"><span data-stu-id="fcd1f-131">NOTES</span></span>

## <span data-ttu-id="fcd1f-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcd1f-132">RELATED LINKS</span></span>

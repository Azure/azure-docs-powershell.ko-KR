---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: f648d347e45b6394776a25735efbb06157cc5611
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212435"
---
# <span data-ttu-id="5ea6e-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="5ea6e-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="5ea6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ea6e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ea6e-103">CDN 원본 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="5ea6e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5ea6e-104">SYNTAX</span></span>

### <span data-ttu-id="5ea6e-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5ea6e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ea6e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ea6e-106">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ea6e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5ea6e-107">DESCRIPTION</span></span>
<span data-ttu-id="5ea6e-108">**AzCdnOrigin** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 원본 서버와 해당 구성 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-108">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="5ea6e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5ea6e-109">EXAMPLES</span></span>

## <span data-ttu-id="5ea6e-110">변수</span><span class="sxs-lookup"><span data-stu-id="5ea6e-110">PARAMETERS</span></span>

### <span data-ttu-id="5ea6e-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ea6e-111">-CdnEndpoint</span></span>
<span data-ttu-id="5ea6e-112">원점이 속한 CDN 끝점 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="5ea6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ea6e-113">-DefaultProfile</span></span>
<span data-ttu-id="5ea6e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5ea6e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ea6e-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5ea6e-115">-EndpointName</span></span>
<span data-ttu-id="5ea6e-116">원본 서버가 속한 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="5ea6e-117">-OriginName</span><span class="sxs-lookup"><span data-stu-id="5ea6e-117">-OriginName</span></span>
<span data-ttu-id="5ea6e-118">원본 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="5ea6e-119">-/Profile</span><span class="sxs-lookup"><span data-stu-id="5ea6e-119">-ProfileName</span></span>
<span data-ttu-id="5ea6e-120">원본 서버가 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="5ea6e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ea6e-121">-ResourceGroupName</span></span>
<span data-ttu-id="5ea6e-122">원본 서버가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="5ea6e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ea6e-123">CommonParameters</span></span>
<span data-ttu-id="5ea6e-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ea6e-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5ea6e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ea6e-126">입력</span><span class="sxs-lookup"><span data-stu-id="5ea6e-126">INPUTS</span></span>

### <span data-ttu-id="5ea6e-127">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ea6e-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="5ea6e-128">출력</span><span class="sxs-lookup"><span data-stu-id="5ea6e-128">OUTPUTS</span></span>

### <span data-ttu-id="5ea6e-129">Microsoft. Cdn. 원본 PSOrigin</span><span class="sxs-lookup"><span data-stu-id="5ea6e-129">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="5ea6e-130">상속자</span><span class="sxs-lookup"><span data-stu-id="5ea6e-130">NOTES</span></span>

## <span data-ttu-id="5ea6e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ea6e-131">RELATED LINKS</span></span>

[<span data-ttu-id="5ea6e-132">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="5ea6e-132">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)



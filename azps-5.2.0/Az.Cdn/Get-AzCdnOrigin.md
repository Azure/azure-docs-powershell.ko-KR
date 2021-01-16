---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: e5e27dba4519d16ebc304f3d6cca99f32f23e341
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347246"
---
# <span data-ttu-id="3f314-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="3f314-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="3f314-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f314-102">SYNOPSIS</span></span>
<span data-ttu-id="3f314-103">CDN 원본 서버를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3f314-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="3f314-104">구문</span><span class="sxs-lookup"><span data-stu-id="3f314-104">SYNTAX</span></span>

### <span data-ttu-id="3f314-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3f314-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f314-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f314-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f314-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f314-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f314-108">설명</span><span class="sxs-lookup"><span data-stu-id="3f314-108">DESCRIPTION</span></span>
<span data-ttu-id="3f314-109">**Get-AzCdnOrigin** cmdlet은 Azure CDN(Content Delivery Network) 원본 서버 및 해당 구성 데이터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3f314-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="3f314-110">예제</span><span class="sxs-lookup"><span data-stu-id="3f314-110">EXAMPLES</span></span>

## <span data-ttu-id="3f314-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f314-111">PARAMETERS</span></span>

### <span data-ttu-id="3f314-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f314-112">-CdnEndpoint</span></span>
<span data-ttu-id="3f314-113">원본이 속한 CDN 엔드포인트 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3f314-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="3f314-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f314-114">-DefaultProfile</span></span>
<span data-ttu-id="3f314-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3f314-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f314-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3f314-116">-EndpointName</span></span>
<span data-ttu-id="3f314-117">원본 서버가 속한 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3f314-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="3f314-118">-OriginName</span><span class="sxs-lookup"><span data-stu-id="3f314-118">-OriginName</span></span>
<span data-ttu-id="3f314-119">원본 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3f314-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="3f314-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="3f314-120">-ProfileName</span></span>
<span data-ttu-id="3f314-121">원본 서버가 속한 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3f314-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="3f314-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f314-122">-ResourceGroupName</span></span>
<span data-ttu-id="3f314-123">원본 서버가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3f314-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="3f314-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f314-124">-ResourceId</span></span>
<span data-ttu-id="3f314-125">Azure CDN 원본의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3f314-125">The resource id of the Azure CDN origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f314-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f314-126">CommonParameters</span></span>
<span data-ttu-id="3f314-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3f314-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f314-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3f314-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f314-129">입력</span><span class="sxs-lookup"><span data-stu-id="3f314-129">INPUTS</span></span>

### <span data-ttu-id="3f314-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f314-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="3f314-131">출력</span><span class="sxs-lookup"><span data-stu-id="3f314-131">OUTPUTS</span></span>

### <span data-ttu-id="3f314-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="3f314-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="3f314-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3f314-133">NOTES</span></span>

## <span data-ttu-id="3f314-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f314-134">RELATED LINKS</span></span>

[<span data-ttu-id="3f314-135">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="3f314-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


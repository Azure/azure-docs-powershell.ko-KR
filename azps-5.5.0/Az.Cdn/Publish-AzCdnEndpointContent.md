---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: 6e8ba9fb6fb65980113ae8093bc4e3c258861968
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200772"
---
# <span data-ttu-id="0889f-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="0889f-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="0889f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0889f-102">SYNOPSIS</span></span>
<span data-ttu-id="0889f-103">엔드포인트에 콘텐츠를 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="0889f-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="0889f-104">구문</span><span class="sxs-lookup"><span data-stu-id="0889f-104">SYNTAX</span></span>

### <span data-ttu-id="0889f-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0889f-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0889f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0889f-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0889f-107">설명</span><span class="sxs-lookup"><span data-stu-id="0889f-107">DESCRIPTION</span></span>
<span data-ttu-id="0889f-108">**Publish-AzCdnEndpointContent** cmdlet은 Azure CDN(Content Delivery Network) 엔드포인트에 대한 원본 서버에서 콘텐츠를 로드합니다.</span><span class="sxs-lookup"><span data-stu-id="0889f-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="0889f-109">예제</span><span class="sxs-lookup"><span data-stu-id="0889f-109">EXAMPLES</span></span>

## <span data-ttu-id="0889f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0889f-110">PARAMETERS</span></span>

### <span data-ttu-id="0889f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0889f-111">-CdnEndpoint</span></span>
<span data-ttu-id="0889f-112">CDN 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0889f-112">Specifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="0889f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0889f-113">-DefaultProfile</span></span>
<span data-ttu-id="0889f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0889f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0889f-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0889f-115">-EndpointName</span></span>
<span data-ttu-id="0889f-116">엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0889f-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="0889f-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="0889f-117">-LoadContent</span></span>
<span data-ttu-id="0889f-118">이 cmdlet이 게시하는 원본 서버의 콘텐츠에 대한 상대 경로 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0889f-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0889f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0889f-119">-PassThru</span></span>
<span data-ttu-id="0889f-120">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0889f-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0889f-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0889f-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0889f-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0889f-122">-ProfileName</span></span>
<span data-ttu-id="0889f-123">원본 서버가 속한 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0889f-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="0889f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0889f-124">-ResourceGroupName</span></span>
<span data-ttu-id="0889f-125">원본 서버가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0889f-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="0889f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0889f-126">CommonParameters</span></span>
<span data-ttu-id="0889f-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0889f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0889f-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0889f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0889f-129">입력</span><span class="sxs-lookup"><span data-stu-id="0889f-129">INPUTS</span></span>

### <span data-ttu-id="0889f-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="0889f-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="0889f-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0889f-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0889f-132">출력</span><span class="sxs-lookup"><span data-stu-id="0889f-132">OUTPUTS</span></span>

### <span data-ttu-id="0889f-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0889f-133">System.Boolean</span></span>

## <span data-ttu-id="0889f-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0889f-134">NOTES</span></span>

## <span data-ttu-id="0889f-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0889f-135">RELATED LINKS</span></span>

[<span data-ttu-id="0889f-136">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="0889f-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)



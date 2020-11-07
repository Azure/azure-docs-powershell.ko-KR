---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: AFDBE48E-63B0-4A9E-9825-5246081AA129
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/publish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Publish-AzCdnEndpointContent.md
ms.openlocfilehash: a851722d02fa37c085649894f41f6273abf4372d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869218"
---
# <span data-ttu-id="e545d-101">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="e545d-101">Publish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="e545d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e545d-102">SYNOPSIS</span></span>
<span data-ttu-id="e545d-103">끝점에 콘텐츠를 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="e545d-103">Loads content to an endpoint.</span></span>

## <span data-ttu-id="e545d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e545d-104">SYNTAX</span></span>

### <span data-ttu-id="e545d-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e545d-105">ByFieldsParameterSet (Default)</span></span>
```
Publish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -LoadContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e545d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e545d-106">ByObjectParameterSet</span></span>
```
Publish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -LoadContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e545d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e545d-107">DESCRIPTION</span></span>
<span data-ttu-id="e545d-108">**AzCdnEndpointContent** CMDLET은 CDN (콘텐츠 배달 네트워크) 끝점에 대 한 원본 서버에서 콘텐츠를 로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="e545d-108">The **Publish-AzCdnEndpointContent** cmdlet loads content from an origin server for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e545d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e545d-109">EXAMPLES</span></span>

## <span data-ttu-id="e545d-110">변수</span><span class="sxs-lookup"><span data-stu-id="e545d-110">PARAMETERS</span></span>

### <span data-ttu-id="e545d-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e545d-111">-CdnEndpoint</span></span>
<span data-ttu-id="e545d-112">CDN 끝점을 Sepcifies 합니다.</span><span class="sxs-lookup"><span data-stu-id="e545d-112">Sepcifies the CDN endpoint.</span></span>

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

### <span data-ttu-id="e545d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e545d-113">-DefaultProfile</span></span>
<span data-ttu-id="e545d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e545d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e545d-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e545d-115">-EndpointName</span></span>
<span data-ttu-id="e545d-116">끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e545d-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="e545d-117">-LoadContent</span><span class="sxs-lookup"><span data-stu-id="e545d-117">-LoadContent</span></span>
<span data-ttu-id="e545d-118">이 cmdlet이 게시 하는 원본 서버의 콘텐츠에 대 한 상대 경로 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e545d-118">Specifies an array of relative paths for the content on the origin server that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="e545d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e545d-119">-PassThru</span></span>
<span data-ttu-id="e545d-120">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e545d-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e545d-121">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e545d-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e545d-122">-/Profile</span><span class="sxs-lookup"><span data-stu-id="e545d-122">-ProfileName</span></span>
<span data-ttu-id="e545d-123">원본 서버가 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e545d-123">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="e545d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e545d-124">-ResourceGroupName</span></span>
<span data-ttu-id="e545d-125">원본 서버가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e545d-125">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="e545d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e545d-126">CommonParameters</span></span>
<span data-ttu-id="e545d-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e545d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e545d-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e545d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e545d-129">입력</span><span class="sxs-lookup"><span data-stu-id="e545d-129">INPUTS</span></span>

### <span data-ttu-id="e545d-130">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e545d-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="e545d-131">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e545d-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e545d-132">출력</span><span class="sxs-lookup"><span data-stu-id="e545d-132">OUTPUTS</span></span>

### <span data-ttu-id="e545d-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e545d-133">System.Boolean</span></span>

## <span data-ttu-id="e545d-134">상속자</span><span class="sxs-lookup"><span data-stu-id="e545d-134">NOTES</span></span>

## <span data-ttu-id="e545d-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e545d-135">RELATED LINKS</span></span>

[<span data-ttu-id="e545d-136">게시 취소-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="e545d-136">Unpublish-AzCdnEndpointContent</span></span>](./Unpublish-AzCdnEndpointContent.md)



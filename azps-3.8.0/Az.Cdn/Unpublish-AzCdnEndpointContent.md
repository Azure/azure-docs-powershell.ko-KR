---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: eb108e665bce54d2b94fc4ab4a56c9573248289a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033784"
---
# <span data-ttu-id="b2e39-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="b2e39-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="b2e39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2e39-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e39-103">CDN 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e39-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="b2e39-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b2e39-104">SYNTAX</span></span>

### <span data-ttu-id="b2e39-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b2e39-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2e39-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2e39-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2e39-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b2e39-107">DESCRIPTION</span></span>
<span data-ttu-id="b2e39-108">**AzCdnEndpointContent** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 끝점에서 콘텐츠를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e39-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b2e39-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b2e39-109">EXAMPLES</span></span>

## <span data-ttu-id="b2e39-110">변수</span><span class="sxs-lookup"><span data-stu-id="b2e39-110">PARAMETERS</span></span>

### <span data-ttu-id="b2e39-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b2e39-111">-CdnEndpoint</span></span>
<span data-ttu-id="b2e39-112">이 cmdlet이 제거 하는 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e39-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="b2e39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e39-113">-DefaultProfile</span></span>
<span data-ttu-id="b2e39-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b2e39-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2e39-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b2e39-115">-EndpointName</span></span>
<span data-ttu-id="b2e39-116">이 cmdlet이 제거 하는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e39-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="b2e39-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2e39-117">-PassThru</span></span>
<span data-ttu-id="b2e39-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e39-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b2e39-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e39-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b2e39-120">-/Profile</span><span class="sxs-lookup"><span data-stu-id="b2e39-120">-ProfileName</span></span>
<span data-ttu-id="b2e39-121">종점이 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e39-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b2e39-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="b2e39-122">-PurgeContent</span></span>
<span data-ttu-id="b2e39-123">이 cmdlet이 제거 하는 원본 서버의 콘텐츠에 대 한 상대 경로 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e39-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="b2e39-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e39-124">-ResourceGroupName</span></span>
<span data-ttu-id="b2e39-125">끝점이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e39-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="b2e39-126">-확인</span><span class="sxs-lookup"><span data-stu-id="b2e39-126">-Confirm</span></span>
<span data-ttu-id="b2e39-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e39-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2e39-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2e39-128">-WhatIf</span></span>
<span data-ttu-id="b2e39-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b2e39-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2e39-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2e39-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2e39-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e39-131">CommonParameters</span></span>
<span data-ttu-id="b2e39-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2e39-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e39-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b2e39-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e39-134">입력</span><span class="sxs-lookup"><span data-stu-id="b2e39-134">INPUTS</span></span>

### <span data-ttu-id="b2e39-135">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b2e39-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="b2e39-136">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b2e39-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b2e39-137">출력</span><span class="sxs-lookup"><span data-stu-id="b2e39-137">OUTPUTS</span></span>

### <span data-ttu-id="b2e39-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b2e39-138">System.Boolean</span></span>

## <span data-ttu-id="b2e39-139">상속자</span><span class="sxs-lookup"><span data-stu-id="b2e39-139">NOTES</span></span>

## <span data-ttu-id="b2e39-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2e39-140">RELATED LINKS</span></span>

[<span data-ttu-id="b2e39-141">게시-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="b2e39-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)



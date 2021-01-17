---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: eb108e665bce54d2b94fc4ab4a56c9573248289a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342410"
---
# <span data-ttu-id="3a2c3-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="3a2c3-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="3a2c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a2c3-102">SYNOPSIS</span></span>
<span data-ttu-id="3a2c3-103">CDN 엔드포인트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3a2c3-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="3a2c3-104">구문</span><span class="sxs-lookup"><span data-stu-id="3a2c3-104">SYNTAX</span></span>

### <span data-ttu-id="3a2c3-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3a2c3-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a2c3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a2c3-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a2c3-107">설명</span><span class="sxs-lookup"><span data-stu-id="3a2c3-107">DESCRIPTION</span></span>
<span data-ttu-id="3a2c3-108">**Unpublish-AzCdnEndpointContent** cmdlet은 Azure CDN(Content Delivery Network) 엔드포인트에서 콘텐츠를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3a2c3-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="3a2c3-109">예제</span><span class="sxs-lookup"><span data-stu-id="3a2c3-109">EXAMPLES</span></span>

## <span data-ttu-id="3a2c3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a2c3-110">PARAMETERS</span></span>

### <span data-ttu-id="3a2c3-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a2c3-111">-CdnEndpoint</span></span>
<span data-ttu-id="3a2c3-112">이 cmdlet이 제거하는 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a2c3-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="3a2c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a2c3-113">-DefaultProfile</span></span>
<span data-ttu-id="3a2c3-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3a2c3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a2c3-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3a2c3-115">-EndpointName</span></span>
<span data-ttu-id="3a2c3-116">이 cmdlet에서 제거한 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a2c3-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="3a2c3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a2c3-117">-PassThru</span></span>
<span data-ttu-id="3a2c3-118">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3a2c3-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3a2c3-119">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a2c3-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3a2c3-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="3a2c3-120">-ProfileName</span></span>
<span data-ttu-id="3a2c3-121">엔드포인트가 속한 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a2c3-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="3a2c3-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="3a2c3-122">-PurgeContent</span></span>
<span data-ttu-id="3a2c3-123">이 cmdlet이 제거한 원본 서버의 콘텐츠에 대한 상대 경로 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a2c3-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="3a2c3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a2c3-124">-ResourceGroupName</span></span>
<span data-ttu-id="3a2c3-125">엔드포인트가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a2c3-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="3a2c3-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a2c3-126">-Confirm</span></span>
<span data-ttu-id="3a2c3-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a2c3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a2c3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a2c3-128">-WhatIf</span></span>
<span data-ttu-id="3a2c3-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3a2c3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a2c3-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a2c3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a2c3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a2c3-131">CommonParameters</span></span>
<span data-ttu-id="3a2c3-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3a2c3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a2c3-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3a2c3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a2c3-134">입력</span><span class="sxs-lookup"><span data-stu-id="3a2c3-134">INPUTS</span></span>

### <span data-ttu-id="3a2c3-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="3a2c3-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="3a2c3-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3a2c3-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3a2c3-137">출력</span><span class="sxs-lookup"><span data-stu-id="3a2c3-137">OUTPUTS</span></span>

### <span data-ttu-id="3a2c3-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a2c3-138">System.Boolean</span></span>

## <span data-ttu-id="3a2c3-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3a2c3-139">NOTES</span></span>

## <span data-ttu-id="3a2c3-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a2c3-140">RELATED LINKS</span></span>

[<span data-ttu-id="3a2c3-141">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="3a2c3-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)



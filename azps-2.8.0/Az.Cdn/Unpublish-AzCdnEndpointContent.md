---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: 6a5a0925967895514de8b7e5294c81571b1cbaba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697557"
---
# <span data-ttu-id="a925b-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="a925b-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="a925b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a925b-102">SYNOPSIS</span></span>
<span data-ttu-id="a925b-103">CDN 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a925b-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="a925b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a925b-104">SYNTAX</span></span>

### <span data-ttu-id="a925b-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a925b-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a925b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a925b-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a925b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a925b-107">DESCRIPTION</span></span>
<span data-ttu-id="a925b-108">**AzCdnEndpointContent** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 끝점에서 콘텐츠를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a925b-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="a925b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a925b-109">EXAMPLES</span></span>

## <span data-ttu-id="a925b-110">변수</span><span class="sxs-lookup"><span data-stu-id="a925b-110">PARAMETERS</span></span>

### <span data-ttu-id="a925b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a925b-111">-CdnEndpoint</span></span>
<span data-ttu-id="a925b-112">이 cmdlet이 제거 하는 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a925b-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="a925b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a925b-113">-DefaultProfile</span></span>
<span data-ttu-id="a925b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a925b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a925b-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a925b-115">-EndpointName</span></span>
<span data-ttu-id="a925b-116">이 cmdlet이 제거 하는 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a925b-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="a925b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a925b-117">-PassThru</span></span>
<span data-ttu-id="a925b-118">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a925b-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a925b-119">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a925b-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a925b-120">-/Profile</span><span class="sxs-lookup"><span data-stu-id="a925b-120">-ProfileName</span></span>
<span data-ttu-id="a925b-121">종점이 속한 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a925b-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="a925b-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="a925b-122">-PurgeContent</span></span>
<span data-ttu-id="a925b-123">이 cmdlet이 제거 하는 원본 서버의 콘텐츠에 대 한 상대 경로 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a925b-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

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

### <span data-ttu-id="a925b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a925b-124">-ResourceGroupName</span></span>
<span data-ttu-id="a925b-125">끝점이 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a925b-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="a925b-126">-확인</span><span class="sxs-lookup"><span data-stu-id="a925b-126">-Confirm</span></span>
<span data-ttu-id="a925b-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a925b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a925b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a925b-128">-WhatIf</span></span>
<span data-ttu-id="a925b-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a925b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a925b-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a925b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a925b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a925b-131">CommonParameters</span></span>
<span data-ttu-id="a925b-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a925b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a925b-133">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a925b-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a925b-134">입력</span><span class="sxs-lookup"><span data-stu-id="a925b-134">INPUTS</span></span>

### <span data-ttu-id="a925b-135">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a925b-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="a925b-136">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a925b-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a925b-137">출력</span><span class="sxs-lookup"><span data-stu-id="a925b-137">OUTPUTS</span></span>

### <span data-ttu-id="a925b-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a925b-138">System.Boolean</span></span>

## <span data-ttu-id="a925b-139">상속자</span><span class="sxs-lookup"><span data-stu-id="a925b-139">NOTES</span></span>

## <span data-ttu-id="a925b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a925b-140">RELATED LINKS</span></span>

[<span data-ttu-id="a925b-141">게시-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="a925b-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)



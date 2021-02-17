---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 7222b33470dc1fff22039c5e88bf3c6560b80c31
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205101"
---
# <span data-ttu-id="2f388-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f388-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="2f388-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f388-102">SYNOPSIS</span></span>
<span data-ttu-id="2f388-103">CDN 엔드포인트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2f388-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="2f388-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f388-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f388-105">설명</span><span class="sxs-lookup"><span data-stu-id="2f388-105">DESCRIPTION</span></span>
<span data-ttu-id="2f388-106">**Set-AzCdnEndpoint** cmdlet은 Azure CDN(Content Delivery Network) 엔드포인트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2f388-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="2f388-107">예제</span><span class="sxs-lookup"><span data-stu-id="2f388-107">EXAMPLES</span></span>

## <span data-ttu-id="2f388-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f388-108">PARAMETERS</span></span>

### <span data-ttu-id="2f388-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f388-109">-CdnEndpoint</span></span>
<span data-ttu-id="2f388-110">이 cmdlet이 업데이트하는 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f388-110">Specifies the endpoint that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f388-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f388-111">-DefaultProfile</span></span>
<span data-ttu-id="2f388-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2f388-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f388-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f388-113">-Confirm</span></span>
<span data-ttu-id="2f388-114">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f388-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f388-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f388-115">-WhatIf</span></span>
<span data-ttu-id="2f388-116">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2f388-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f388-117">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f388-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f388-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f388-118">CommonParameters</span></span>
<span data-ttu-id="2f388-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f388-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f388-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2f388-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f388-121">입력</span><span class="sxs-lookup"><span data-stu-id="2f388-121">INPUTS</span></span>

### <span data-ttu-id="2f388-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f388-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="2f388-123">출력</span><span class="sxs-lookup"><span data-stu-id="2f388-123">OUTPUTS</span></span>

### <span data-ttu-id="2f388-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f388-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="2f388-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f388-125">NOTES</span></span>

## <span data-ttu-id="2f388-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f388-126">RELATED LINKS</span></span>

[<span data-ttu-id="2f388-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f388-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="2f388-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f388-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="2f388-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f388-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="2f388-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f388-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="2f388-131">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2f388-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 7222b33470dc1fff22039c5e88bf3c6560b80c31
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496150"
---
# <span data-ttu-id="7728f-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7728f-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="7728f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7728f-102">SYNOPSIS</span></span>
<span data-ttu-id="7728f-103">CDN 엔드포인트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7728f-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="7728f-104">구문</span><span class="sxs-lookup"><span data-stu-id="7728f-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7728f-105">설명</span><span class="sxs-lookup"><span data-stu-id="7728f-105">DESCRIPTION</span></span>
<span data-ttu-id="7728f-106">**Set-AzCdnEndpoint** cmdlet은 Azure CDN(Content Delivery Network) 엔드포인트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7728f-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="7728f-107">예제</span><span class="sxs-lookup"><span data-stu-id="7728f-107">EXAMPLES</span></span>

## <span data-ttu-id="7728f-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7728f-108">PARAMETERS</span></span>

### <span data-ttu-id="7728f-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7728f-109">-CdnEndpoint</span></span>
<span data-ttu-id="7728f-110">이 cmdlet이 업데이트하는 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7728f-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="7728f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7728f-111">-DefaultProfile</span></span>
<span data-ttu-id="7728f-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7728f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7728f-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7728f-113">-Confirm</span></span>
<span data-ttu-id="7728f-114">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7728f-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7728f-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7728f-115">-WhatIf</span></span>
<span data-ttu-id="7728f-116">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7728f-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7728f-117">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7728f-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7728f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7728f-118">CommonParameters</span></span>
<span data-ttu-id="7728f-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7728f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7728f-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7728f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7728f-121">입력</span><span class="sxs-lookup"><span data-stu-id="7728f-121">INPUTS</span></span>

### <span data-ttu-id="7728f-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7728f-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="7728f-123">출력</span><span class="sxs-lookup"><span data-stu-id="7728f-123">OUTPUTS</span></span>

### <span data-ttu-id="7728f-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7728f-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="7728f-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7728f-125">NOTES</span></span>

## <span data-ttu-id="7728f-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7728f-126">RELATED LINKS</span></span>

[<span data-ttu-id="7728f-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7728f-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="7728f-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7728f-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="7728f-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7728f-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="7728f-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7728f-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="7728f-131">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7728f-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)



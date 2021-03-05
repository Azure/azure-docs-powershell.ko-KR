---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: 4270f7c9781ef960cdbb20a8a067a3dc22255723
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996865"
---
# <span data-ttu-id="001a6-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="001a6-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="001a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="001a6-102">SYNOPSIS</span></span>
<span data-ttu-id="001a6-103">CDN 엔드포인트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="001a6-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="001a6-104">구문</span><span class="sxs-lookup"><span data-stu-id="001a6-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="001a6-105">설명</span><span class="sxs-lookup"><span data-stu-id="001a6-105">DESCRIPTION</span></span>
<span data-ttu-id="001a6-106">**Set-AzCdnEndpoint** cmdlet은 CDN(Azure Content Delivery Network) 엔드포인트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="001a6-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="001a6-107">예제</span><span class="sxs-lookup"><span data-stu-id="001a6-107">EXAMPLES</span></span>

## <span data-ttu-id="001a6-108">매개 변수</span><span class="sxs-lookup"><span data-stu-id="001a6-108">PARAMETERS</span></span>

### <span data-ttu-id="001a6-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="001a6-109">-CdnEndpoint</span></span>
<span data-ttu-id="001a6-110">이 cmdlet이 업데이트하는 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="001a6-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="001a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="001a6-111">-DefaultProfile</span></span>
<span data-ttu-id="001a6-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="001a6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="001a6-113">-확인</span><span class="sxs-lookup"><span data-stu-id="001a6-113">-Confirm</span></span>
<span data-ttu-id="001a6-114">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="001a6-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="001a6-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="001a6-115">-WhatIf</span></span>
<span data-ttu-id="001a6-116">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="001a6-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="001a6-117">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="001a6-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="001a6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="001a6-118">CommonParameters</span></span>
<span data-ttu-id="001a6-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="001a6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="001a6-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="001a6-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="001a6-121">입력</span><span class="sxs-lookup"><span data-stu-id="001a6-121">INPUTS</span></span>

### <span data-ttu-id="001a6-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="001a6-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="001a6-123">출력</span><span class="sxs-lookup"><span data-stu-id="001a6-123">OUTPUTS</span></span>

### <span data-ttu-id="001a6-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="001a6-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="001a6-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="001a6-125">NOTES</span></span>

## <span data-ttu-id="001a6-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="001a6-126">RELATED LINKS</span></span>

[<span data-ttu-id="001a6-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="001a6-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="001a6-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="001a6-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="001a6-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="001a6-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="001a6-130">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="001a6-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="001a6-131">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="001a6-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: cce3e2f9deb1f5df5c85d4f0b289b97e9cd36820
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701399"
---
# <span data-ttu-id="67ec8-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="67ec8-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="67ec8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67ec8-102">SYNOPSIS</span></span>
<span data-ttu-id="67ec8-103">CDN 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ec8-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="67ec8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67ec8-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67ec8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="67ec8-105">DESCRIPTION</span></span>
<span data-ttu-id="67ec8-106">**AzCdnEndpoint** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ec8-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="67ec8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="67ec8-107">EXAMPLES</span></span>

## <span data-ttu-id="67ec8-108">변수</span><span class="sxs-lookup"><span data-stu-id="67ec8-108">PARAMETERS</span></span>

### <span data-ttu-id="67ec8-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="67ec8-109">-CdnEndpoint</span></span>
<span data-ttu-id="67ec8-110">이 cmdlet이 업데이트 하는 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ec8-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="67ec8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ec8-111">-DefaultProfile</span></span>
<span data-ttu-id="67ec8-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="67ec8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67ec8-113">-확인</span><span class="sxs-lookup"><span data-stu-id="67ec8-113">-Confirm</span></span>
<span data-ttu-id="67ec8-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ec8-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67ec8-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67ec8-115">-WhatIf</span></span>
<span data-ttu-id="67ec8-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="67ec8-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67ec8-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67ec8-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67ec8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ec8-118">CommonParameters</span></span>
<span data-ttu-id="67ec8-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67ec8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ec8-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67ec8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ec8-121">입력</span><span class="sxs-lookup"><span data-stu-id="67ec8-121">INPUTS</span></span>

### <span data-ttu-id="67ec8-122">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="67ec8-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="67ec8-123">출력</span><span class="sxs-lookup"><span data-stu-id="67ec8-123">OUTPUTS</span></span>

### <span data-ttu-id="67ec8-124">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="67ec8-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="67ec8-125">상속자</span><span class="sxs-lookup"><span data-stu-id="67ec8-125">NOTES</span></span>

## <span data-ttu-id="67ec8-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67ec8-126">RELATED LINKS</span></span>

[<span data-ttu-id="67ec8-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="67ec8-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="67ec8-128">새로운 AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="67ec8-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="67ec8-129">제거-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="67ec8-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="67ec8-130">시작-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="67ec8-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="67ec8-131">중지-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="67ec8-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)



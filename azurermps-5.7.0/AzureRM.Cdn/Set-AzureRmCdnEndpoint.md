---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
ms.openlocfilehash: 13b5b219ec789ac54332caa366cfb0277f0bfacb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529932"
---
# <span data-ttu-id="6f1c7-101">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f1c7-101">Set-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="6f1c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f1c7-102">SYNOPSIS</span></span>
<span data-ttu-id="6f1c7-103">CDN 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f1c7-103">Updates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f1c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f1c7-104">SYNTAX</span></span>

```
Set-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f1c7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6f1c7-105">DESCRIPTION</span></span>
<span data-ttu-id="6f1c7-106">**AzureRmCdnEndpoint** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f1c7-106">The **Set-AzureRmCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="6f1c7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6f1c7-107">EXAMPLES</span></span>

## <span data-ttu-id="6f1c7-108">변수</span><span class="sxs-lookup"><span data-stu-id="6f1c7-108">PARAMETERS</span></span>

### <span data-ttu-id="6f1c7-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f1c7-109">-CdnEndpoint</span></span>
<span data-ttu-id="6f1c7-110">이 cmdlet이 업데이트 하는 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f1c7-110">Specifies the endpoint that this cmdlet updates.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f1c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f1c7-111">-DefaultProfile</span></span>
<span data-ttu-id="6f1c7-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6f1c7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f1c7-113">-확인</span><span class="sxs-lookup"><span data-stu-id="6f1c7-113">-Confirm</span></span>
<span data-ttu-id="6f1c7-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f1c7-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f1c7-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f1c7-115">-WhatIf</span></span>
<span data-ttu-id="6f1c7-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6f1c7-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f1c7-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f1c7-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f1c7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f1c7-118">CommonParameters</span></span>
<span data-ttu-id="6f1c7-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f1c7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f1c7-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f1c7-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f1c7-121">입력</span><span class="sxs-lookup"><span data-stu-id="6f1c7-121">INPUTS</span></span>

### <span data-ttu-id="6f1c7-122">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f1c7-122">PSEndpoint</span></span>
<span data-ttu-id="6f1c7-123">' CdnEndpoint ' 매개 변수는 파이프라인에서 ' PSEndpoint ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f1c7-123">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="6f1c7-124">출력</span><span class="sxs-lookup"><span data-stu-id="6f1c7-124">OUTPUTS</span></span>

### <span data-ttu-id="6f1c7-125">Microsoft. Cdn. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f1c7-125">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="6f1c7-126">상속자</span><span class="sxs-lookup"><span data-stu-id="6f1c7-126">NOTES</span></span>

## <span data-ttu-id="6f1c7-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f1c7-127">RELATED LINKS</span></span>

[<span data-ttu-id="6f1c7-128">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f1c7-128">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="6f1c7-129">새로운 AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f1c7-129">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="6f1c7-130">제거-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f1c7-130">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="6f1c7-131">시작-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f1c7-131">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="6f1c7-132">중지-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f1c7-132">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)



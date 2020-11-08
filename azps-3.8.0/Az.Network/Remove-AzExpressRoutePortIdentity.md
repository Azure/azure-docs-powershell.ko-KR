---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044050"
---
# <span data-ttu-id="efbec-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="efbec-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="efbec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efbec-102">SYNOPSIS</span></span>
<span data-ttu-id="efbec-103">ExpressRoutePort에서 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efbec-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="efbec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="efbec-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efbec-105">설명은</span><span class="sxs-lookup"><span data-stu-id="efbec-105">DESCRIPTION</span></span>
<span data-ttu-id="efbec-106">**AzExpressRoutePortIdentity** cmdlet은 로컬 Azure ExpressRoutePort 개체에서 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efbec-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="efbec-107">**AzExpressRoutePort** 를 사용 하 여 ExpressRoutePort에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="efbec-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="efbec-108">예제의</span><span class="sxs-lookup"><span data-stu-id="efbec-108">EXAMPLES</span></span>

### <span data-ttu-id="efbec-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="efbec-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="efbec-110">변수</span><span class="sxs-lookup"><span data-stu-id="efbec-110">PARAMETERS</span></span>

### <span data-ttu-id="efbec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efbec-111">-DefaultProfile</span></span>
<span data-ttu-id="efbec-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efbec-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efbec-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="efbec-113">-ExpressRoutePort</span></span>
<span data-ttu-id="efbec-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="efbec-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efbec-115">-확인</span><span class="sxs-lookup"><span data-stu-id="efbec-115">-Confirm</span></span>
<span data-ttu-id="efbec-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="efbec-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efbec-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efbec-117">-WhatIf</span></span>
<span data-ttu-id="efbec-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="efbec-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efbec-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="efbec-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efbec-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efbec-120">CommonParameters</span></span>
<span data-ttu-id="efbec-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="efbec-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efbec-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efbec-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="efbec-123">입력</span><span class="sxs-lookup"><span data-stu-id="efbec-123">INPUTS</span></span>

### <span data-ttu-id="efbec-124">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="efbec-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="efbec-125">출력</span><span class="sxs-lookup"><span data-stu-id="efbec-125">OUTPUTS</span></span>

### <span data-ttu-id="efbec-126">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="efbec-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="efbec-127">상속자</span><span class="sxs-lookup"><span data-stu-id="efbec-127">NOTES</span></span>

## <span data-ttu-id="efbec-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efbec-128">RELATED LINKS</span></span>
[<span data-ttu-id="efbec-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="efbec-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="efbec-130">새로운 AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="efbec-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="efbec-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="efbec-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c7ffb86fa56a09fb0c5bbdd41e62bf8d47bee140
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869714"
---
# <span data-ttu-id="6490f-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="6490f-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="6490f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6490f-102">SYNOPSIS</span></span>
<span data-ttu-id="6490f-103">ExpressRoutePort에서 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6490f-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="6490f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6490f-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6490f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6490f-105">DESCRIPTION</span></span>
<span data-ttu-id="6490f-106">**AzExpressRoutePortIdentity** cmdlet은 로컬 Azure ExpressRoutePort 개체에서 id를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6490f-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="6490f-107">**AzExpressRoutePort** 를 사용 하 여 ExpressRoutePort에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6490f-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="6490f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="6490f-108">EXAMPLES</span></span>

### <span data-ttu-id="6490f-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="6490f-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="6490f-110">변수</span><span class="sxs-lookup"><span data-stu-id="6490f-110">PARAMETERS</span></span>

### <span data-ttu-id="6490f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6490f-111">-DefaultProfile</span></span>
<span data-ttu-id="6490f-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6490f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6490f-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6490f-113">-ExpressRoutePort</span></span>
<span data-ttu-id="6490f-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6490f-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="6490f-115">-확인</span><span class="sxs-lookup"><span data-stu-id="6490f-115">-Confirm</span></span>
<span data-ttu-id="6490f-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6490f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6490f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6490f-117">-WhatIf</span></span>
<span data-ttu-id="6490f-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6490f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6490f-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6490f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6490f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6490f-120">CommonParameters</span></span>
<span data-ttu-id="6490f-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6490f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6490f-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6490f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="6490f-123">입력</span><span class="sxs-lookup"><span data-stu-id="6490f-123">INPUTS</span></span>

### <span data-ttu-id="6490f-124">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6490f-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="6490f-125">출력</span><span class="sxs-lookup"><span data-stu-id="6490f-125">OUTPUTS</span></span>

### <span data-ttu-id="6490f-126">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6490f-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="6490f-127">상속자</span><span class="sxs-lookup"><span data-stu-id="6490f-127">NOTES</span></span>

## <span data-ttu-id="6490f-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6490f-128">RELATED LINKS</span></span>
[<span data-ttu-id="6490f-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="6490f-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="6490f-130">새로운 AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="6490f-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="6490f-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="6490f-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

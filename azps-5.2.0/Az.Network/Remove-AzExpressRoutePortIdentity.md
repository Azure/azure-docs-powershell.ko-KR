---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePortIdentity.md
ms.openlocfilehash: c0a2977a4d6c448f2703df258339c99f3d2851cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366822"
---
# <span data-ttu-id="fab44-101">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="fab44-101">Remove-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="fab44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fab44-102">SYNOPSIS</span></span>
<span data-ttu-id="fab44-103">ExpressRoutePort에서 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fab44-103">Removes a identity from an ExpressRoutePort.</span></span>

## <span data-ttu-id="fab44-104">구문</span><span class="sxs-lookup"><span data-stu-id="fab44-104">SYNTAX</span></span>

```
Remove-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fab44-105">설명</span><span class="sxs-lookup"><span data-stu-id="fab44-105">DESCRIPTION</span></span>
<span data-ttu-id="fab44-106">**Remove-AzExpressRoutePortIdentity** cmdlet은 로컬 Azure ExpressRoutePort 개체에서 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fab44-106">The **Remove-AzExpressRoutePortIdentity** cmdlet removes identity from a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="fab44-107">**Remove-AzExpressRoutePort를** 사용하여 ExpressRoutePort에서 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fab44-107">Use **Remove-AzExpressRoutePort** to remove it to from ExpressRoutePort.</span></span>

## <span data-ttu-id="fab44-108">예제</span><span class="sxs-lookup"><span data-stu-id="fab44-108">EXAMPLES</span></span>

### <span data-ttu-id="fab44-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="fab44-109">Example 1</span></span>
```powershell
PS C:\> $expressroutePort = Remove-AzExpressRoutePortIdentity -ExpressRoutePort $expressroutePort
```

## <span data-ttu-id="fab44-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fab44-110">PARAMETERS</span></span>

### <span data-ttu-id="fab44-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab44-111">-DefaultProfile</span></span>
<span data-ttu-id="fab44-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fab44-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fab44-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fab44-113">-ExpressRoutePort</span></span>
<span data-ttu-id="fab44-114">The ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fab44-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="fab44-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fab44-115">-Confirm</span></span>
<span data-ttu-id="fab44-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fab44-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fab44-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fab44-117">-WhatIf</span></span>
<span data-ttu-id="fab44-118">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fab44-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fab44-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fab44-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fab44-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab44-120">CommonParameters</span></span>
<span data-ttu-id="fab44-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fab44-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fab44-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fab44-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>


## <span data-ttu-id="fab44-123">입력</span><span class="sxs-lookup"><span data-stu-id="fab44-123">INPUTS</span></span>

### <span data-ttu-id="fab44-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fab44-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="fab44-125">출력</span><span class="sxs-lookup"><span data-stu-id="fab44-125">OUTPUTS</span></span>

### <span data-ttu-id="fab44-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fab44-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="fab44-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fab44-127">NOTES</span></span>

## <span data-ttu-id="fab44-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fab44-128">RELATED LINKS</span></span>
[<span data-ttu-id="fab44-129">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="fab44-129">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="fab44-130">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="fab44-130">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="fab44-131">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="fab44-131">Set-AzExpressRoutePortIdentity</span></span>](./Set-AzExpressRoutePortIdentity.md)

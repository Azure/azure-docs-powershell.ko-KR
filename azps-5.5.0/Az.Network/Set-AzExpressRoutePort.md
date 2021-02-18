---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: 2365729f3960e3652e2b4c0709ca14092fea3264
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206517"
---
# <span data-ttu-id="ce58c-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ce58c-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="ce58c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce58c-102">SYNOPSIS</span></span>
<span data-ttu-id="ce58c-103">ExpressRoutePort를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce58c-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="ce58c-104">구문</span><span class="sxs-lookup"><span data-stu-id="ce58c-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce58c-105">설명</span><span class="sxs-lookup"><span data-stu-id="ce58c-105">DESCRIPTION</span></span>
<span data-ttu-id="ce58c-106">**Set-AzExpressRoutePort** cmdlet은 수정된 ExpressRoutePort를 Azure에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ce58c-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="ce58c-107">예제</span><span class="sxs-lookup"><span data-stu-id="ce58c-107">EXAMPLES</span></span>

### <span data-ttu-id="ce58c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ce58c-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="ce58c-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="ce58c-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="ce58c-110">ExpressRoutePort 링크의 관리자 상태를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce58c-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

### <span data-ttu-id="ce58c-111">예제 3</span><span class="sxs-lookup"><span data-stu-id="ce58c-111">Example 3</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
$erport.SciState = 'Disabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

## <span data-ttu-id="ce58c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce58c-112">PARAMETERS</span></span>

### <span data-ttu-id="ce58c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce58c-113">-AsJob</span></span>
<span data-ttu-id="ce58c-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ce58c-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce58c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce58c-115">-DefaultProfile</span></span>
<span data-ttu-id="ce58c-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce58c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce58c-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ce58c-117">-ExpressRoutePort</span></span>
<span data-ttu-id="ce58c-118">ExpressRoutePort 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ce58c-118">The ExpressRoutePort object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce58c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce58c-119">-Confirm</span></span>
<span data-ttu-id="ce58c-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce58c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce58c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce58c-121">-WhatIf</span></span>
<span data-ttu-id="ce58c-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ce58c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce58c-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce58c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce58c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce58c-124">CommonParameters</span></span>
<span data-ttu-id="ce58c-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ce58c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce58c-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ce58c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce58c-127">입력</span><span class="sxs-lookup"><span data-stu-id="ce58c-127">INPUTS</span></span>

### <span data-ttu-id="ce58c-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ce58c-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="ce58c-129">출력</span><span class="sxs-lookup"><span data-stu-id="ce58c-129">OUTPUTS</span></span>

### <span data-ttu-id="ce58c-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ce58c-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="ce58c-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ce58c-131">NOTES</span></span>

## <span data-ttu-id="ce58c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce58c-132">RELATED LINKS</span></span>

[<span data-ttu-id="ce58c-133">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ce58c-133">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="ce58c-134">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ce58c-134">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="ce58c-135">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ce58c-135">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

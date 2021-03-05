---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: c431b03c4dd417638f84fe3a483bcaf9eefcb837
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963979"
---
# <span data-ttu-id="e46cb-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e46cb-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="e46cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e46cb-102">SYNOPSIS</span></span>
<span data-ttu-id="e46cb-103">ExpressRoutePort를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e46cb-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="e46cb-104">구문</span><span class="sxs-lookup"><span data-stu-id="e46cb-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e46cb-105">설명</span><span class="sxs-lookup"><span data-stu-id="e46cb-105">DESCRIPTION</span></span>
<span data-ttu-id="e46cb-106">**Set-AzExpressRoutePort** cmdlet은 수정된 ExpressRoutePort를 Azure에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e46cb-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="e46cb-107">예제</span><span class="sxs-lookup"><span data-stu-id="e46cb-107">EXAMPLES</span></span>

### <span data-ttu-id="e46cb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e46cb-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="e46cb-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="e46cb-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="e46cb-110">ExpressRoutePort의 링크의 관리자 상태를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e46cb-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

### <span data-ttu-id="e46cb-111">예제 3</span><span class="sxs-lookup"><span data-stu-id="e46cb-111">Example 3</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
$erport.SciState = 'Disabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

## <span data-ttu-id="e46cb-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e46cb-112">PARAMETERS</span></span>

### <span data-ttu-id="e46cb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e46cb-113">-AsJob</span></span>
<span data-ttu-id="e46cb-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e46cb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e46cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e46cb-115">-DefaultProfile</span></span>
<span data-ttu-id="e46cb-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e46cb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e46cb-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e46cb-117">-ExpressRoutePort</span></span>
<span data-ttu-id="e46cb-118">ExpressRoutePort 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e46cb-118">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="e46cb-119">-확인</span><span class="sxs-lookup"><span data-stu-id="e46cb-119">-Confirm</span></span>
<span data-ttu-id="e46cb-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e46cb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e46cb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e46cb-121">-WhatIf</span></span>
<span data-ttu-id="e46cb-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e46cb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e46cb-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e46cb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e46cb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e46cb-124">CommonParameters</span></span>
<span data-ttu-id="e46cb-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e46cb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e46cb-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e46cb-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e46cb-127">입력</span><span class="sxs-lookup"><span data-stu-id="e46cb-127">INPUTS</span></span>

### <span data-ttu-id="e46cb-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e46cb-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="e46cb-129">출력</span><span class="sxs-lookup"><span data-stu-id="e46cb-129">OUTPUTS</span></span>

### <span data-ttu-id="e46cb-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e46cb-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="e46cb-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e46cb-131">NOTES</span></span>

## <span data-ttu-id="e46cb-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e46cb-132">RELATED LINKS</span></span>

[<span data-ttu-id="e46cb-133">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e46cb-133">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="e46cb-134">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e46cb-134">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="e46cb-135">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e46cb-135">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

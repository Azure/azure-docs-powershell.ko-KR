---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: b5170ef175b93bc977ba047d4188d51de2858e63
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491756"
---
# <span data-ttu-id="d8416-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d8416-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="d8416-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8416-102">SYNOPSIS</span></span>
<span data-ttu-id="d8416-103">ExpressRoutePort를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d8416-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="d8416-104">구문</span><span class="sxs-lookup"><span data-stu-id="d8416-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8416-105">설명</span><span class="sxs-lookup"><span data-stu-id="d8416-105">DESCRIPTION</span></span>
<span data-ttu-id="d8416-106">**Set-AzExpressRoutePort** cmdlet은 수정된 ExpressRoutePort를 Azure에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d8416-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="d8416-107">예제</span><span class="sxs-lookup"><span data-stu-id="d8416-107">EXAMPLES</span></span>

### <span data-ttu-id="d8416-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d8416-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="d8416-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="d8416-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="d8416-110">ExpressRoutePort 링크의 관리자 상태를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d8416-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="d8416-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8416-111">PARAMETERS</span></span>

### <span data-ttu-id="d8416-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8416-112">-AsJob</span></span>
<span data-ttu-id="d8416-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d8416-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8416-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8416-114">-DefaultProfile</span></span>
<span data-ttu-id="d8416-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8416-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8416-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d8416-116">-ExpressRoutePort</span></span>
<span data-ttu-id="d8416-117">ExpressRoutePort 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d8416-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="d8416-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8416-118">-Confirm</span></span>
<span data-ttu-id="d8416-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8416-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8416-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8416-120">-WhatIf</span></span>
<span data-ttu-id="d8416-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d8416-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8416-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8416-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8416-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8416-123">CommonParameters</span></span>
<span data-ttu-id="d8416-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d8416-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8416-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d8416-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8416-126">입력</span><span class="sxs-lookup"><span data-stu-id="d8416-126">INPUTS</span></span>

### <span data-ttu-id="d8416-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d8416-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="d8416-128">출력</span><span class="sxs-lookup"><span data-stu-id="d8416-128">OUTPUTS</span></span>

### <span data-ttu-id="d8416-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d8416-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="d8416-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d8416-130">NOTES</span></span>

## <span data-ttu-id="d8416-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8416-131">RELATED LINKS</span></span>

[<span data-ttu-id="d8416-132">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d8416-132">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="d8416-133">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d8416-133">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="d8416-134">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d8416-134">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

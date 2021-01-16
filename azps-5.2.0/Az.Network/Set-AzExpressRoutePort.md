---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: b5170ef175b93bc977ba047d4188d51de2858e63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327011"
---
# <span data-ttu-id="370fd-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="370fd-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="370fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="370fd-102">SYNOPSIS</span></span>
<span data-ttu-id="370fd-103">ExpressRoutePort를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="370fd-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="370fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="370fd-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="370fd-105">설명</span><span class="sxs-lookup"><span data-stu-id="370fd-105">DESCRIPTION</span></span>
<span data-ttu-id="370fd-106">**Set-AzExpressRoutePort** cmdlet은 수정된 ExpressRoutePort를 Azure에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="370fd-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="370fd-107">예제</span><span class="sxs-lookup"><span data-stu-id="370fd-107">EXAMPLES</span></span>

### <span data-ttu-id="370fd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="370fd-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="370fd-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="370fd-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="370fd-110">ExpressRoutePort 링크의 관리자 상태를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="370fd-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="370fd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="370fd-111">PARAMETERS</span></span>

### <span data-ttu-id="370fd-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="370fd-112">-AsJob</span></span>
<span data-ttu-id="370fd-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="370fd-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="370fd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="370fd-114">-DefaultProfile</span></span>
<span data-ttu-id="370fd-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="370fd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="370fd-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="370fd-116">-ExpressRoutePort</span></span>
<span data-ttu-id="370fd-117">ExpressRoutePort 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="370fd-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="370fd-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="370fd-118">-Confirm</span></span>
<span data-ttu-id="370fd-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="370fd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="370fd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="370fd-120">-WhatIf</span></span>
<span data-ttu-id="370fd-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="370fd-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="370fd-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="370fd-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="370fd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="370fd-123">CommonParameters</span></span>
<span data-ttu-id="370fd-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="370fd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="370fd-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="370fd-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="370fd-126">입력</span><span class="sxs-lookup"><span data-stu-id="370fd-126">INPUTS</span></span>

### <span data-ttu-id="370fd-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="370fd-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="370fd-128">출력</span><span class="sxs-lookup"><span data-stu-id="370fd-128">OUTPUTS</span></span>

### <span data-ttu-id="370fd-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="370fd-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="370fd-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="370fd-130">NOTES</span></span>

## <span data-ttu-id="370fd-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="370fd-131">RELATED LINKS</span></span>

[<span data-ttu-id="370fd-132">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="370fd-132">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="370fd-133">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="370fd-133">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="370fd-134">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="370fd-134">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePort.md
ms.openlocfilehash: fe1182f165e347b312288d56604fddad6bad68da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869570"
---
# <span data-ttu-id="fae4a-101">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fae4a-101">Set-AzExpressRoutePort</span></span>

## <span data-ttu-id="fae4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fae4a-102">SYNOPSIS</span></span>
<span data-ttu-id="fae4a-103">ExpressRoutePort를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fae4a-103">Modifies an ExpressRoutePort.</span></span>

## <span data-ttu-id="fae4a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fae4a-104">SYNTAX</span></span>

```
Set-AzExpressRoutePort -ExpressRoutePort <PSExpressRoutePort> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fae4a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fae4a-105">DESCRIPTION</span></span>
<span data-ttu-id="fae4a-106">**AzExpressRoutePort** cmdlet은 수정 된 ExpressRoutePort를 Azure에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fae4a-106">The **Set-AzExpressRoutePort** cmdlet saves the modified ExpressRoutePort to Azure.</span></span>

## <span data-ttu-id="fae4a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fae4a-107">EXAMPLES</span></span>

### <span data-ttu-id="fae4a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fae4a-108">Example 1</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -ExpressRoutePort $erport
```

### <span data-ttu-id="fae4a-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="fae4a-109">Example 2</span></span>
```powershell
$erport = Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
$erport.Links[0].AdminState = 'Enabled'
Set-AzExpressRoutePort -InputObject $erport
```

<span data-ttu-id="fae4a-110">ExpressRoutePort 링크의 관리자 상태를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fae4a-110">Modifies the admin state of a link of an ExpressRoutePort</span></span>

## <span data-ttu-id="fae4a-111">변수</span><span class="sxs-lookup"><span data-stu-id="fae4a-111">PARAMETERS</span></span>

### <span data-ttu-id="fae4a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fae4a-112">-AsJob</span></span>
<span data-ttu-id="fae4a-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fae4a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fae4a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fae4a-114">-DefaultProfile</span></span>
<span data-ttu-id="fae4a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fae4a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fae4a-116">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fae4a-116">-ExpressRoutePort</span></span>
<span data-ttu-id="fae4a-117">ExpressRoutePort 개체</span><span class="sxs-lookup"><span data-stu-id="fae4a-117">The ExpressRoutePort object.</span></span>

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

### <span data-ttu-id="fae4a-118">-확인</span><span class="sxs-lookup"><span data-stu-id="fae4a-118">-Confirm</span></span>
<span data-ttu-id="fae4a-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fae4a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fae4a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fae4a-120">-WhatIf</span></span>
<span data-ttu-id="fae4a-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fae4a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fae4a-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fae4a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fae4a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fae4a-123">CommonParameters</span></span>
<span data-ttu-id="fae4a-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fae4a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fae4a-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fae4a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fae4a-126">입력</span><span class="sxs-lookup"><span data-stu-id="fae4a-126">INPUTS</span></span>

### <span data-ttu-id="fae4a-127">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="fae4a-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="fae4a-128">출력</span><span class="sxs-lookup"><span data-stu-id="fae4a-128">OUTPUTS</span></span>

### <span data-ttu-id="fae4a-129">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="fae4a-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="fae4a-130">상속자</span><span class="sxs-lookup"><span data-stu-id="fae4a-130">NOTES</span></span>

## <span data-ttu-id="fae4a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fae4a-131">RELATED LINKS</span></span>

[<span data-ttu-id="fae4a-132">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fae4a-132">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="fae4a-133">새로운 AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fae4a-133">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="fae4a-134">제거-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fae4a-134">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

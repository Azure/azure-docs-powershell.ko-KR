---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 649ae6233f312dab4f18263bb65c4a9cd43b2aee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189524"
---
# <span data-ttu-id="711ee-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="711ee-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="711ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="711ee-102">SYNOPSIS</span></span>
<span data-ttu-id="711ee-103">ExpressRoute 교차 연결을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="711ee-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="711ee-104">구문</span><span class="sxs-lookup"><span data-stu-id="711ee-104">SYNTAX</span></span>

### <span data-ttu-id="711ee-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="711ee-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="711ee-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="711ee-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="711ee-107">설명</span><span class="sxs-lookup"><span data-stu-id="711ee-107">DESCRIPTION</span></span>
<span data-ttu-id="711ee-108">**Set-AzExpressRouteCrossConnection** cmdlet은 수정된 ExpressRoute 교차 연결을 Azure에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="711ee-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="711ee-109">예제</span><span class="sxs-lookup"><span data-stu-id="711ee-109">EXAMPLES</span></span>

### <span data-ttu-id="711ee-110">예제 1: ExpressRoute 교차 연결의 서비스 공급자 프로비전 상태 변경</span><span class="sxs-lookup"><span data-stu-id="711ee-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="711ee-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="711ee-111">PARAMETERS</span></span>

### <span data-ttu-id="711ee-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="711ee-112">-AsJob</span></span>
<span data-ttu-id="711ee-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="711ee-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="711ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="711ee-114">-DefaultProfile</span></span>
<span data-ttu-id="711ee-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="711ee-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="711ee-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="711ee-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="711ee-117">이 cmdlet이 수정하는 **ExpressRouteCrossConnection** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="711ee-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: ModifyByCircuitReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="711ee-118">-Force</span><span class="sxs-lookup"><span data-stu-id="711ee-118">-Force</span></span>
<span data-ttu-id="711ee-119">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="711ee-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="711ee-120">-Name</span><span class="sxs-lookup"><span data-stu-id="711ee-120">-Name</span></span>
<span data-ttu-id="711ee-121">Express 경로 교차 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="711ee-121">The name of express route cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="711ee-122">-Peerings</span><span class="sxs-lookup"><span data-stu-id="711ee-122">-Peerings</span></span>
<span data-ttu-id="711ee-123">교차 연결에 대한 피어링 목록</span><span class="sxs-lookup"><span data-stu-id="711ee-123">The list of peerings for the cross connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionPeering[]
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="711ee-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="711ee-124">-ResourceGroupName</span></span>
<span data-ttu-id="711ee-125">The ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="711ee-125">The ExpressRouteCrossConnection</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="711ee-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="711ee-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="711ee-127">서비스 공급자 참고 사항</span><span class="sxs-lookup"><span data-stu-id="711ee-127">The service provider notes</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="711ee-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="711ee-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="711ee-129">설정할 서비스 공급자 프로비전 상태</span><span class="sxs-lookup"><span data-stu-id="711ee-129">The service provider provisioning state to be set</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="711ee-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="711ee-130">-Confirm</span></span>
<span data-ttu-id="711ee-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="711ee-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="711ee-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="711ee-132">-WhatIf</span></span>
<span data-ttu-id="711ee-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="711ee-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="711ee-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="711ee-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="711ee-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="711ee-135">CommonParameters</span></span>
<span data-ttu-id="711ee-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="711ee-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="711ee-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="711ee-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="711ee-138">입력</span><span class="sxs-lookup"><span data-stu-id="711ee-138">INPUTS</span></span>

### <span data-ttu-id="711ee-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="711ee-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="711ee-140">'ExpressRouteCrossConnection' 매개 변수는 파이프라인에서 'PSExpressRouteCrossConnection' 형식의 값을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="711ee-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="711ee-141">출력</span><span class="sxs-lookup"><span data-stu-id="711ee-141">OUTPUTS</span></span>

### <span data-ttu-id="711ee-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="711ee-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="711ee-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="711ee-143">NOTES</span></span>

## <span data-ttu-id="711ee-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="711ee-144">RELATED LINKS</span></span>

[<span data-ttu-id="711ee-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="711ee-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 9769a5506f528eb03d5e6d5a26340b961786c363
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963995"
---
# <span data-ttu-id="1427e-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1427e-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="1427e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1427e-102">SYNOPSIS</span></span>
<span data-ttu-id="1427e-103">ExpressRoute 교차 연결을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1427e-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="1427e-104">구문</span><span class="sxs-lookup"><span data-stu-id="1427e-104">SYNTAX</span></span>

### <span data-ttu-id="1427e-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="1427e-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1427e-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="1427e-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1427e-107">설명</span><span class="sxs-lookup"><span data-stu-id="1427e-107">DESCRIPTION</span></span>
<span data-ttu-id="1427e-108">**Set-AzExpressRouteCrossConnection** cmdlet은 수정된 ExpressRoute 크로스 연결을 Azure에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1427e-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="1427e-109">예제</span><span class="sxs-lookup"><span data-stu-id="1427e-109">EXAMPLES</span></span>

### <span data-ttu-id="1427e-110">예제 1: ExpressRoute 교차 연결의 서비스 공급자 프로비전 상태 변경</span><span class="sxs-lookup"><span data-stu-id="1427e-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="1427e-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1427e-111">PARAMETERS</span></span>

### <span data-ttu-id="1427e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1427e-112">-AsJob</span></span>
<span data-ttu-id="1427e-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1427e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1427e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1427e-114">-DefaultProfile</span></span>
<span data-ttu-id="1427e-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1427e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1427e-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1427e-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="1427e-117">이 cmdlet이 수정하는 **ExpressRouteCrossConnection** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1427e-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1427e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1427e-118">-Force</span></span>
<span data-ttu-id="1427e-119">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1427e-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1427e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1427e-120">-Name</span></span>
<span data-ttu-id="1427e-121">익스프레스 경로 교차 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1427e-121">The name of express route cross connection.</span></span>

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

### <span data-ttu-id="1427e-122">-피어링</span><span class="sxs-lookup"><span data-stu-id="1427e-122">-Peerings</span></span>
<span data-ttu-id="1427e-123">교차 연결에 대한 피어링 목록</span><span class="sxs-lookup"><span data-stu-id="1427e-123">The list of peerings for the cross connection</span></span>

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

### <span data-ttu-id="1427e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1427e-124">-ResourceGroupName</span></span>
<span data-ttu-id="1427e-125">The ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1427e-125">The ExpressRouteCrossConnection</span></span>

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

### <span data-ttu-id="1427e-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="1427e-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="1427e-127">서비스 공급자 노트</span><span class="sxs-lookup"><span data-stu-id="1427e-127">The service provider notes</span></span>

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

### <span data-ttu-id="1427e-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="1427e-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="1427e-129">설정할 서비스 공급자 프로비전 상태</span><span class="sxs-lookup"><span data-stu-id="1427e-129">The service provider provisioning state to be set</span></span>

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

### <span data-ttu-id="1427e-130">-확인</span><span class="sxs-lookup"><span data-stu-id="1427e-130">-Confirm</span></span>
<span data-ttu-id="1427e-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1427e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1427e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1427e-132">-WhatIf</span></span>
<span data-ttu-id="1427e-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1427e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1427e-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1427e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1427e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1427e-135">CommonParameters</span></span>
<span data-ttu-id="1427e-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1427e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1427e-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1427e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1427e-138">입력</span><span class="sxs-lookup"><span data-stu-id="1427e-138">INPUTS</span></span>

### <span data-ttu-id="1427e-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1427e-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="1427e-140">매개 변수 'ExpressRouteCrossConnection'은 파이프라인에서 'PSExpressRouteCrossConnection' 형식의 값을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="1427e-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="1427e-141">출력</span><span class="sxs-lookup"><span data-stu-id="1427e-141">OUTPUTS</span></span>

### <span data-ttu-id="1427e-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1427e-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="1427e-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1427e-143">NOTES</span></span>

## <span data-ttu-id="1427e-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1427e-144">RELATED LINKS</span></span>

[<span data-ttu-id="1427e-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="1427e-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)

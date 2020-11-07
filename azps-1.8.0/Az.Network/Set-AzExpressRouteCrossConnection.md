---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 175082a90a1a494eb4508bc83d71584326c9eb97
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700020"
---
# <span data-ttu-id="59867-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="59867-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="59867-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59867-102">SYNOPSIS</span></span>
<span data-ttu-id="59867-103">Express 경로 간 연결을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59867-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="59867-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59867-104">SYNTAX</span></span>

### <span data-ttu-id="59867-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="59867-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59867-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="59867-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59867-107">설명은</span><span class="sxs-lookup"><span data-stu-id="59867-107">DESCRIPTION</span></span>
<span data-ttu-id="59867-108">**AzExpressRouteCrossConnection** cmdlet은 수정 된 express 경로 간 연결을 Azure에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="59867-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="59867-109">예제의</span><span class="sxs-lookup"><span data-stu-id="59867-109">EXAMPLES</span></span>

### <span data-ttu-id="59867-110">예제 1: Express 경로 연결의 서비스 공급자 프로비저닝 상태 변경</span><span class="sxs-lookup"><span data-stu-id="59867-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="59867-111">변수</span><span class="sxs-lookup"><span data-stu-id="59867-111">PARAMETERS</span></span>

### <span data-ttu-id="59867-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59867-112">-AsJob</span></span>
<span data-ttu-id="59867-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="59867-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59867-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59867-114">-DefaultProfile</span></span>
<span data-ttu-id="59867-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59867-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59867-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="59867-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="59867-117">이 cmdlet이 수정 하는 **ExpressRouteCrossConnection** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59867-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="59867-118">-Force</span><span class="sxs-lookup"><span data-stu-id="59867-118">-Force</span></span>
<span data-ttu-id="59867-119">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="59867-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="59867-120">-이름</span><span class="sxs-lookup"><span data-stu-id="59867-120">-Name</span></span>
<span data-ttu-id="59867-121">Express 경로 교차 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59867-121">The name of express route cross connection.</span></span>

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

### <span data-ttu-id="59867-122">-Peerings 번</span><span class="sxs-lookup"><span data-stu-id="59867-122">-Peerings</span></span>
<span data-ttu-id="59867-123">교차 연결에 대 한 peerings</span><span class="sxs-lookup"><span data-stu-id="59867-123">The list of peerings for the cross connection</span></span>

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

### <span data-ttu-id="59867-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59867-124">-ResourceGroupName</span></span>
<span data-ttu-id="59867-125">ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="59867-125">The ExpressRouteCrossConnection</span></span>

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

### <span data-ttu-id="59867-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="59867-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="59867-127">서비스 공급자 참고 사항</span><span class="sxs-lookup"><span data-stu-id="59867-127">The service provider notes</span></span>

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

### <span data-ttu-id="59867-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="59867-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="59867-129">설정할 서비스 공급자 프로비저닝 상태</span><span class="sxs-lookup"><span data-stu-id="59867-129">The service provider provisioning state to be set</span></span>

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

### <span data-ttu-id="59867-130">-확인</span><span class="sxs-lookup"><span data-stu-id="59867-130">-Confirm</span></span>
<span data-ttu-id="59867-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="59867-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59867-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59867-132">-WhatIf</span></span>
<span data-ttu-id="59867-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="59867-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59867-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59867-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59867-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59867-135">CommonParameters</span></span>
<span data-ttu-id="59867-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59867-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59867-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59867-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59867-138">입력</span><span class="sxs-lookup"><span data-stu-id="59867-138">INPUTS</span></span>

### <span data-ttu-id="59867-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="59867-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="59867-140">' ExpressRouteCrossConnection ' 매개 변수는 파이프라인에서 ' PSExpressRouteCrossConnection ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="59867-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="59867-141">출력</span><span class="sxs-lookup"><span data-stu-id="59867-141">OUTPUTS</span></span>

### <span data-ttu-id="59867-142">PSExpressRouteCrossConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="59867-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="59867-143">상속자</span><span class="sxs-lookup"><span data-stu-id="59867-143">NOTES</span></span>

## <span data-ttu-id="59867-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59867-144">RELATED LINKS</span></span>

[<span data-ttu-id="59867-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="59867-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 4940936a50156f8515885099a205a4fa3566a7b4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492554"
---
# <span data-ttu-id="9213e-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="9213e-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="9213e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9213e-102">SYNOPSIS</span></span>
<span data-ttu-id="9213e-103">Nat Gateway 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9213e-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="9213e-104">구문</span><span class="sxs-lookup"><span data-stu-id="9213e-104">SYNTAX</span></span>

### <span data-ttu-id="9213e-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9213e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9213e-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9213e-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9213e-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9213e-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9213e-108">설명</span><span class="sxs-lookup"><span data-stu-id="9213e-108">DESCRIPTION</span></span>
<span data-ttu-id="9213e-109">Nat Gateway 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="9213e-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="9213e-110">예제</span><span class="sxs-lookup"><span data-stu-id="9213e-110">EXAMPLES</span></span>

### <span data-ttu-id="9213e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9213e-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="9213e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9213e-112">PARAMETERS</span></span>

### <span data-ttu-id="9213e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9213e-113">-AsJob</span></span>
<span data-ttu-id="9213e-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9213e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9213e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9213e-115">-DefaultProfile</span></span>
<span data-ttu-id="9213e-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9213e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9213e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9213e-117">-Force</span></span>
<span data-ttu-id="9213e-118">리소스를 삭제하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9213e-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="9213e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9213e-119">-InputObject</span></span>
<span data-ttu-id="9213e-120">Nat Gateway 리소스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9213e-120">Specifies the Nat Gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9213e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9213e-121">-Name</span></span>
<span data-ttu-id="9213e-122">Nat Gateway 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9213e-122">Name of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9213e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9213e-123">-PassThru</span></span>
<span data-ttu-id="9213e-124">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9213e-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9213e-125">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9213e-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9213e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9213e-126">-ResourceGroupName</span></span>
<span data-ttu-id="9213e-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9213e-127">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9213e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9213e-128">-ResourceId</span></span>
<span data-ttu-id="9213e-129">Nat Gateway와 연결된 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9213e-129">Resource Id associated with the Nat Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9213e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9213e-130">-Confirm</span></span>
<span data-ttu-id="9213e-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9213e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9213e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9213e-132">-WhatIf</span></span>
<span data-ttu-id="9213e-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9213e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9213e-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9213e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9213e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9213e-135">CommonParameters</span></span>
<span data-ttu-id="9213e-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9213e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9213e-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9213e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9213e-138">입력</span><span class="sxs-lookup"><span data-stu-id="9213e-138">INPUTS</span></span>

### <span data-ttu-id="9213e-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="9213e-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="9213e-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9213e-140">System.String</span></span>

## <span data-ttu-id="9213e-141">출력</span><span class="sxs-lookup"><span data-stu-id="9213e-141">OUTPUTS</span></span>

### <span data-ttu-id="9213e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9213e-142">System.Boolean</span></span>

## <span data-ttu-id="9213e-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9213e-143">NOTES</span></span>

## <span data-ttu-id="9213e-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9213e-144">RELATED LINKS</span></span>

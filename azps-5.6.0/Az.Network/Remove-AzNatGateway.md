---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 430ea183d618779045aaf5d13554edac2ce98626
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996254"
---
# <span data-ttu-id="6e011-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6e011-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="6e011-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e011-102">SYNOPSIS</span></span>
<span data-ttu-id="6e011-103">Nat Gateway 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6e011-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="6e011-104">구문</span><span class="sxs-lookup"><span data-stu-id="6e011-104">SYNTAX</span></span>

### <span data-ttu-id="6e011-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6e011-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e011-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e011-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e011-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e011-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e011-108">설명</span><span class="sxs-lookup"><span data-stu-id="6e011-108">DESCRIPTION</span></span>
<span data-ttu-id="6e011-109">Nat Gateway 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="6e011-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="6e011-110">예제</span><span class="sxs-lookup"><span data-stu-id="6e011-110">EXAMPLES</span></span>

### <span data-ttu-id="6e011-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6e011-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="6e011-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6e011-112">PARAMETERS</span></span>

### <span data-ttu-id="6e011-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e011-113">-AsJob</span></span>
<span data-ttu-id="6e011-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6e011-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e011-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e011-115">-DefaultProfile</span></span>
<span data-ttu-id="6e011-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e011-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e011-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6e011-117">-Force</span></span>
<span data-ttu-id="6e011-118">리소스를 삭제하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e011-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="6e011-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e011-119">-InputObject</span></span>
<span data-ttu-id="6e011-120">Nat Gateway 리소스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6e011-120">Specifies the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="6e011-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6e011-121">-Name</span></span>
<span data-ttu-id="6e011-122">Nat Gateway 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e011-122">Name of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="6e011-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e011-123">-PassThru</span></span>
<span data-ttu-id="6e011-124">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6e011-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6e011-125">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e011-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6e011-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e011-126">-ResourceGroupName</span></span>
<span data-ttu-id="6e011-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e011-127">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="6e011-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e011-128">-ResourceId</span></span>
<span data-ttu-id="6e011-129">Nat Gateway와 연결된 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6e011-129">Resource Id associated with the Nat Gateway.</span></span>

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

### <span data-ttu-id="6e011-130">-확인</span><span class="sxs-lookup"><span data-stu-id="6e011-130">-Confirm</span></span>
<span data-ttu-id="6e011-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e011-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e011-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e011-132">-WhatIf</span></span>
<span data-ttu-id="6e011-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6e011-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e011-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e011-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e011-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e011-135">CommonParameters</span></span>
<span data-ttu-id="6e011-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6e011-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e011-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e011-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e011-138">입력</span><span class="sxs-lookup"><span data-stu-id="6e011-138">INPUTS</span></span>

### <span data-ttu-id="6e011-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="6e011-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="6e011-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6e011-140">System.String</span></span>

## <span data-ttu-id="6e011-141">출력</span><span class="sxs-lookup"><span data-stu-id="6e011-141">OUTPUTS</span></span>

### <span data-ttu-id="6e011-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6e011-142">System.Boolean</span></span>

## <span data-ttu-id="6e011-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6e011-143">NOTES</span></span>

## <span data-ttu-id="6e011-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e011-144">RELATED LINKS</span></span>

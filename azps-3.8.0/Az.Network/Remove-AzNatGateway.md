---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 4940936a50156f8515885099a205a4fa3566a7b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044023"
---
# <span data-ttu-id="fb7e2-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="fb7e2-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="fb7e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb7e2-102">SYNOPSIS</span></span>
<span data-ttu-id="fb7e2-103">Nat 게이트웨이 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7e2-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="fb7e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb7e2-104">SYNTAX</span></span>

### <span data-ttu-id="fb7e2-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fb7e2-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7e2-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb7e2-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb7e2-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb7e2-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb7e2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fb7e2-108">DESCRIPTION</span></span>
<span data-ttu-id="fb7e2-109">Nat 게이트웨이 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="fb7e2-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="fb7e2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fb7e2-110">EXAMPLES</span></span>

### <span data-ttu-id="fb7e2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fb7e2-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="fb7e2-112">변수</span><span class="sxs-lookup"><span data-stu-id="fb7e2-112">PARAMETERS</span></span>

### <span data-ttu-id="fb7e2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb7e2-113">-AsJob</span></span>
<span data-ttu-id="fb7e2-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fb7e2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb7e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb7e2-115">-DefaultProfile</span></span>
<span data-ttu-id="fb7e2-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb7e2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb7e2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fb7e2-117">-Force</span></span>
<span data-ttu-id="fb7e2-118">리소스를 삭제 하려는 경우 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb7e2-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="fb7e2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb7e2-119">-InputObject</span></span>
<span data-ttu-id="fb7e2-120">Nat 게이트웨이 리소스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7e2-120">Specifies the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="fb7e2-121">-이름</span><span class="sxs-lookup"><span data-stu-id="fb7e2-121">-Name</span></span>
<span data-ttu-id="fb7e2-122">Nat 게이트웨이 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb7e2-122">Name of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="fb7e2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb7e2-123">-PassThru</span></span>
<span data-ttu-id="fb7e2-124">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7e2-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fb7e2-125">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb7e2-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fb7e2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb7e2-126">-ResourceGroupName</span></span>
<span data-ttu-id="fb7e2-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb7e2-127">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="fb7e2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb7e2-128">-ResourceId</span></span>
<span data-ttu-id="fb7e2-129">Nat 게이트웨이와 연결 된 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="fb7e2-129">Resource Id associated with the Nat Gateway.</span></span>

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

### <span data-ttu-id="fb7e2-130">-확인</span><span class="sxs-lookup"><span data-stu-id="fb7e2-130">-Confirm</span></span>
<span data-ttu-id="fb7e2-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7e2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb7e2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb7e2-132">-WhatIf</span></span>
<span data-ttu-id="fb7e2-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fb7e2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb7e2-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb7e2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb7e2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb7e2-135">CommonParameters</span></span>
<span data-ttu-id="fb7e2-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb7e2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb7e2-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fb7e2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb7e2-138">입력</span><span class="sxs-lookup"><span data-stu-id="fb7e2-138">INPUTS</span></span>

### <span data-ttu-id="fb7e2-139">Microsoft. \* .Patgateway.</span><span class="sxs-lookup"><span data-stu-id="fb7e2-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="fb7e2-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fb7e2-140">System.String</span></span>

## <span data-ttu-id="fb7e2-141">출력</span><span class="sxs-lookup"><span data-stu-id="fb7e2-141">OUTPUTS</span></span>

### <span data-ttu-id="fb7e2-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="fb7e2-142">System.Boolean</span></span>

## <span data-ttu-id="fb7e2-143">상속자</span><span class="sxs-lookup"><span data-stu-id="fb7e2-143">NOTES</span></span>

## <span data-ttu-id="fb7e2-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb7e2-144">RELATED LINKS</span></span>

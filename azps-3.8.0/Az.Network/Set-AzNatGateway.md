---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: fe19aba38402519a77185062ac6192d6ff9915eb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042495"
---
# <span data-ttu-id="ba5a5-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ba5a5-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="ba5a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba5a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ba5a5-103">공용 Ip 주소, 공용 Ip 접두사 및 IdleTimeoutInMinutes를 사용 하 여 Nat 게이트웨이 리소스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5a5-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="ba5a5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba5a5-104">SYNTAX</span></span>

### <span data-ttu-id="ba5a5-105">SetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ba5a5-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba5a5-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba5a5-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba5a5-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba5a5-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba5a5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ba5a5-108">DESCRIPTION</span></span>
<span data-ttu-id="ba5a5-109">공용 Ip 주소, 공용 Ip 접두사 및 IdleTimeoutInMinutes를 사용 하 여 Nat 게이트웨이 리소스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5a5-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="ba5a5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ba5a5-110">EXAMPLES</span></span>

### <span data-ttu-id="ba5a5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ba5a5-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="ba5a5-112">변수</span><span class="sxs-lookup"><span data-stu-id="ba5a5-112">PARAMETERS</span></span>

### <span data-ttu-id="ba5a5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba5a5-113">-AsJob</span></span>
<span data-ttu-id="ba5a5-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ba5a5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba5a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba5a5-115">-DefaultProfile</span></span>
<span data-ttu-id="ba5a5-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba5a5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba5a5-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ba5a5-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ba5a5-118">Nat 게이트웨이의 유휴 시간 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="ba5a5-118">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba5a5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba5a5-119">-InputObject</span></span>
<span data-ttu-id="ba5a5-120">Nat 게이트웨이 리소스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5a5-120">Specifies Nat Gateway Resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5a5-121">-이름</span><span class="sxs-lookup"><span data-stu-id="ba5a5-121">-Name</span></span>
<span data-ttu-id="ba5a5-122">Nat 게이트웨이 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba5a5-122">Name of the Nat Gateway Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba5a5-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ba5a5-123">-PublicIpAddress</span></span>
<span data-ttu-id="ba5a5-124">Nat 게이트웨이 리소스에 연결 된 공용 ip 주소의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ba5a5-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba5a5-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ba5a5-125">-PublicIpPrefix</span></span>
<span data-ttu-id="ba5a5-126">Nat 게이트웨이 리소스와 연결 된 공용 ip 접두사의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ba5a5-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba5a5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba5a5-127">-ResourceGroupName</span></span>
<span data-ttu-id="ba5a5-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba5a5-128">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba5a5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba5a5-129">-ResourceId</span></span>
<span data-ttu-id="ba5a5-130">Nat 게이트웨이 리소스의 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5a5-130">Specifies the Id of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5a5-131">-확인</span><span class="sxs-lookup"><span data-stu-id="ba5a5-131">-Confirm</span></span>
<span data-ttu-id="ba5a5-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5a5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba5a5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba5a5-133">-WhatIf</span></span>
<span data-ttu-id="ba5a5-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ba5a5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba5a5-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba5a5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba5a5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba5a5-136">CommonParameters</span></span>
<span data-ttu-id="ba5a5-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5a5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba5a5-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ba5a5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba5a5-139">입력</span><span class="sxs-lookup"><span data-stu-id="ba5a5-139">INPUTS</span></span>

### <span data-ttu-id="ba5a5-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ba5a5-140">System.String</span></span>

### <span data-ttu-id="ba5a5-141">Microsoft. \* .Patgateway.</span><span class="sxs-lookup"><span data-stu-id="ba5a5-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="ba5a5-142">출력</span><span class="sxs-lookup"><span data-stu-id="ba5a5-142">OUTPUTS</span></span>

### <span data-ttu-id="ba5a5-143">Microsoft. \* .Patgateway.</span><span class="sxs-lookup"><span data-stu-id="ba5a5-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="ba5a5-144">상속자</span><span class="sxs-lookup"><span data-stu-id="ba5a5-144">NOTES</span></span>

## <span data-ttu-id="ba5a5-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba5a5-145">RELATED LINKS</span></span>

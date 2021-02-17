---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznatgateway.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNatGateway.md
ms.openlocfilehash: fe19aba38402519a77185062ac6192d6ff9915eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202456"
---
# <span data-ttu-id="1c054-101">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="1c054-101">Set-AzNatGateway</span></span>

## <span data-ttu-id="1c054-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c054-102">SYNOPSIS</span></span>
<span data-ttu-id="1c054-103">공용 IP 주소, 공용 IP 주소 및 IdleTimeoutInMinutes로 Nat 게이트웨이 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1c054-103">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="1c054-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c054-104">SYNTAX</span></span>

### <span data-ttu-id="1c054-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1c054-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzNatGateway -ResourceGroupName <String> -Name <String> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c054-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c054-106">SetByResourceIdParameterSet</span></span>
```
Set-AzNatGateway -ResourceId <String> [-PublicIpAddress <PSResourceId[]>] [-PublicIpPrefix <PSResourceId[]>]
 [-AsJob] [-IdleTimeoutInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c054-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c054-107">SetByInputObjectParameterSet</span></span>
```
Set-AzNatGateway -InputObject <PSNatGateway> [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-AsJob] [-IdleTimeoutInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c054-108">설명</span><span class="sxs-lookup"><span data-stu-id="1c054-108">DESCRIPTION</span></span>
<span data-ttu-id="1c054-109">공용 IP 주소, 공용 IP 주소 및 IdleTimeoutInMinutes로 Nat 게이트웨이 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1c054-109">Update Nat Gateway Resource with Public Ip Address, Public Ip Prefix and IdleTimeoutInMinutes.</span></span>

## <span data-ttu-id="1c054-110">예제</span><span class="sxs-lookup"><span data-stu-id="1c054-110">EXAMPLES</span></span>

### <span data-ttu-id="1c054-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1c054-111">Example 1</span></span>
```powershell
PS C:\> $nGateway = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1"
PS C:\> $pipArray = $pip, $pip2
PS C:\> $natUpdate = Set-AzNatGateway -InputObject $nGateway -IdleTimeoutInMinutes 5 -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceGroupName "natgateway_test" -Name "ng1" -PublicIpAddress $pipArray
PS C:\> $natUpdate = Set-AzNatGateway -ResourceId "natgateway_id" -PublicIpAddress $pipArray
```

## <span data-ttu-id="1c054-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c054-112">PARAMETERS</span></span>

### <span data-ttu-id="1c054-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c054-113">-AsJob</span></span>
<span data-ttu-id="1c054-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1c054-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c054-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c054-115">-DefaultProfile</span></span>
<span data-ttu-id="1c054-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c054-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c054-117">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="1c054-117">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="1c054-118">nat 게이트웨이의 유휴 시간 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="1c054-118">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="1c054-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c054-119">-InputObject</span></span>
<span data-ttu-id="1c054-120">Nat Gateway 리소스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c054-120">Specifies Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="1c054-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1c054-121">-Name</span></span>
<span data-ttu-id="1c054-122">Nat Gateway 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c054-122">Name of the Nat Gateway Resource.</span></span>

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

### <span data-ttu-id="1c054-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1c054-123">-PublicIpAddress</span></span>
<span data-ttu-id="1c054-124">nat 게이트웨이 리소스와 연결된 공용 IP 주소의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="1c054-124">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="1c054-125">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="1c054-125">-PublicIpPrefix</span></span>
<span data-ttu-id="1c054-126">nat 게이트웨이 리소스와 연결된 공용 IP의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="1c054-126">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="1c054-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c054-127">-ResourceGroupName</span></span>
<span data-ttu-id="1c054-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c054-128">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="1c054-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c054-129">-ResourceId</span></span>
<span data-ttu-id="1c054-130">Nat Gateway 리소스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c054-130">Specifies the Id of the Nat Gateway resource.</span></span>

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

### <span data-ttu-id="1c054-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c054-131">-Confirm</span></span>
<span data-ttu-id="1c054-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c054-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c054-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c054-133">-WhatIf</span></span>
<span data-ttu-id="1c054-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1c054-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c054-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c054-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c054-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c054-136">CommonParameters</span></span>
<span data-ttu-id="1c054-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c054-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c054-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c054-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c054-139">입력</span><span class="sxs-lookup"><span data-stu-id="1c054-139">INPUTS</span></span>

### <span data-ttu-id="1c054-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1c054-140">System.String</span></span>

### <span data-ttu-id="1c054-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="1c054-141">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="1c054-142">출력</span><span class="sxs-lookup"><span data-stu-id="1c054-142">OUTPUTS</span></span>

### <span data-ttu-id="1c054-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="1c054-143">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="1c054-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c054-144">NOTES</span></span>

## <span data-ttu-id="1c054-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c054-145">RELATED LINKS</span></span>

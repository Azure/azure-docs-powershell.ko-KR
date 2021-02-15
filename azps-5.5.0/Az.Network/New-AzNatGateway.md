---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 0855ba4e7e16503045d13c370838cd5d3fffb033
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193641"
---
# <span data-ttu-id="4dbac-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="4dbac-101">New-AzNatGateway</span></span>

## <span data-ttu-id="4dbac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dbac-102">SYNOPSIS</span></span>
<span data-ttu-id="4dbac-103">공용 IP 주소/공용 IP Prefix, IdleTimeoutInMinutes 및 SKU 속성을 사용하여 새 Nat Gateway 리소스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="4dbac-104">구문</span><span class="sxs-lookup"><span data-stu-id="4dbac-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dbac-105">설명</span><span class="sxs-lookup"><span data-stu-id="4dbac-105">DESCRIPTION</span></span>
<span data-ttu-id="4dbac-106">**New-AzNatGateway** cmdlet은 Nat Gateway 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="4dbac-107">natgateway에는 다음이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="4dbac-108">공용 IP 주소 및/또는 공용 IP 주소</span><span class="sxs-lookup"><span data-stu-id="4dbac-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="4dbac-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4dbac-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="4dbac-110">SKU</span><span class="sxs-lookup"><span data-stu-id="4dbac-110">Sku</span></span>
- <span data-ttu-id="4dbac-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dbac-111">ResourceGroupName</span></span>
- <span data-ttu-id="4dbac-112">ResourceName</span><span class="sxs-lookup"><span data-stu-id="4dbac-112">ResourceName</span></span>
- <span data-ttu-id="4dbac-113">위치</span><span class="sxs-lookup"><span data-stu-id="4dbac-113">Location</span></span>

## <span data-ttu-id="4dbac-114">예제</span><span class="sxs-lookup"><span data-stu-id="4dbac-114">EXAMPLES</span></span>

### <span data-ttu-id="4dbac-115">예제 1: 공용 IP 주소를 사용하여 Nat 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="4dbac-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="4dbac-116">예제 2: 공용 IP를 사용하여 Nat 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="4dbac-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="4dbac-117">예제 3: 가용성 영역 1에서 공용 IP 주소를 사용하여 Nat Gateway 만들기</span><span class="sxs-lookup"><span data-stu-id="4dbac-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="4dbac-118">첫 번째 명령은 표준 공용 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="4dbac-119">두 번째 명령은 가용성 영역 1에서 공용 IP 주소를 사용하여 NAT 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="4dbac-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dbac-120">PARAMETERS</span></span>

### <span data-ttu-id="4dbac-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4dbac-121">-AsJob</span></span>
<span data-ttu-id="4dbac-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4dbac-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4dbac-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dbac-123">-DefaultProfile</span></span>
<span data-ttu-id="4dbac-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dbac-125">-Force</span><span class="sxs-lookup"><span data-stu-id="4dbac-125">-Force</span></span>
<span data-ttu-id="4dbac-126">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4dbac-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4dbac-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="4dbac-128">nat 게이트웨이의 유휴 시간 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-128">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="4dbac-129">-Location</span><span class="sxs-lookup"><span data-stu-id="4dbac-129">-Location</span></span>
<span data-ttu-id="4dbac-130">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-130">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbac-131">-Name</span><span class="sxs-lookup"><span data-stu-id="4dbac-131">-Name</span></span>
<span data-ttu-id="4dbac-132">nat 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-132">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbac-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4dbac-133">-PublicIpAddress</span></span>
<span data-ttu-id="4dbac-134">nat 게이트웨이 리소스와 연결된 공용 IP 주소의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="4dbac-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4dbac-135">-PublicIpPrefix</span></span>
<span data-ttu-id="4dbac-136">nat 게이트웨이 리소스와 연결된 공용 IP의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="4dbac-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dbac-137">-ResourceGroupName</span></span>
<span data-ttu-id="4dbac-138">nat 게이트웨이의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-138">The resource group name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbac-139">-Sku</span><span class="sxs-lookup"><span data-stu-id="4dbac-139">-Sku</span></span>
<span data-ttu-id="4dbac-140">NAT 게이트웨이 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-140">Name of a NAT gateway SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbac-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="4dbac-141">-Tag</span></span>
<span data-ttu-id="4dbac-142">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-142">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbac-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="4dbac-143">-Zone</span></span>
<span data-ttu-id="4dbac-144">Nat Gateway를 배포해야 하는 지역을 표시하는 가용성 영역 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dbac-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4dbac-145">-Confirm</span></span>
<span data-ttu-id="4dbac-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dbac-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dbac-147">-WhatIf</span></span>
<span data-ttu-id="4dbac-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4dbac-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dbac-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dbac-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dbac-150">CommonParameters</span></span>
<span data-ttu-id="4dbac-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4dbac-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dbac-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4dbac-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dbac-153">입력</span><span class="sxs-lookup"><span data-stu-id="4dbac-153">INPUTS</span></span>

### <span data-ttu-id="4dbac-154">System.String</span><span class="sxs-lookup"><span data-stu-id="4dbac-154">System.String</span></span>

### <span data-ttu-id="4dbac-155">System.Int32</span><span class="sxs-lookup"><span data-stu-id="4dbac-155">System.Int32</span></span>

### <span data-ttu-id="4dbac-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4dbac-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4dbac-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="4dbac-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="4dbac-158">출력</span><span class="sxs-lookup"><span data-stu-id="4dbac-158">OUTPUTS</span></span>

### <span data-ttu-id="4dbac-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="4dbac-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="4dbac-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4dbac-160">NOTES</span></span>

## <span data-ttu-id="4dbac-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4dbac-161">RELATED LINKS</span></span>

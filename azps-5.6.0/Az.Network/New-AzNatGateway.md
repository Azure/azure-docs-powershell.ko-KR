---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 168a1803781748eb81c3a2087876b2a7b18d9d39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952171"
---
# <span data-ttu-id="fed11-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="fed11-101">New-AzNatGateway</span></span>

## <span data-ttu-id="fed11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fed11-102">SYNOPSIS</span></span>
<span data-ttu-id="fed11-103">공용 IP 주소/공용 IP 프리픽스, IdleTimeoutInMinutes 및 Sku 속성을 사용하여 새 Nat Gateway 리소스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="fed11-104">구문</span><span class="sxs-lookup"><span data-stu-id="fed11-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fed11-105">설명</span><span class="sxs-lookup"><span data-stu-id="fed11-105">DESCRIPTION</span></span>
<span data-ttu-id="fed11-106">**New-AzNatGateway** cmdlet은 Nat Gateway 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="fed11-107">natgateway에는 다음이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="fed11-108">공용 IP 주소 및/또는 공용 IP 프리픽스</span><span class="sxs-lookup"><span data-stu-id="fed11-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="fed11-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="fed11-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="fed11-110">Sku</span><span class="sxs-lookup"><span data-stu-id="fed11-110">Sku</span></span>
- <span data-ttu-id="fed11-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fed11-111">ResourceGroupName</span></span>
- <span data-ttu-id="fed11-112">ResourceName</span><span class="sxs-lookup"><span data-stu-id="fed11-112">ResourceName</span></span>
- <span data-ttu-id="fed11-113">위치</span><span class="sxs-lookup"><span data-stu-id="fed11-113">Location</span></span>

## <span data-ttu-id="fed11-114">예제</span><span class="sxs-lookup"><span data-stu-id="fed11-114">EXAMPLES</span></span>

### <span data-ttu-id="fed11-115">예제 1: 공용 IP 주소로 Nat Gateway 만들기</span><span class="sxs-lookup"><span data-stu-id="fed11-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="fed11-116">예제 2: 공용 IP 프리픽스를 사용하여 Nat Gateway 만들기</span><span class="sxs-lookup"><span data-stu-id="fed11-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="fed11-117">예제 3: 가용성 영역 1에서 공용 IP 주소를 사용하여 Nat Gateway 만들기</span><span class="sxs-lookup"><span data-stu-id="fed11-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="fed11-118">첫 번째 명령은 표준 공용 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="fed11-119">두 번째 명령은 가용성 영역 1에서 공용 IP 주소를 사용하여 NAT Gateway를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="fed11-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fed11-120">PARAMETERS</span></span>

### <span data-ttu-id="fed11-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fed11-121">-AsJob</span></span>
<span data-ttu-id="fed11-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fed11-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fed11-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fed11-123">-DefaultProfile</span></span>
<span data-ttu-id="fed11-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fed11-125">-Force</span><span class="sxs-lookup"><span data-stu-id="fed11-125">-Force</span></span>
<span data-ttu-id="fed11-126">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fed11-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="fed11-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="fed11-128">nat 게이트웨이의 유휴 시간 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-128">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="fed11-129">-Location</span><span class="sxs-lookup"><span data-stu-id="fed11-129">-Location</span></span>
<span data-ttu-id="fed11-130">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-130">The location.</span></span>

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

### <span data-ttu-id="fed11-131">-Name</span><span class="sxs-lookup"><span data-stu-id="fed11-131">-Name</span></span>
<span data-ttu-id="fed11-132">nat 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-132">The name of the nat gateway.</span></span>

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

### <span data-ttu-id="fed11-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fed11-133">-PublicIpAddress</span></span>
<span data-ttu-id="fed11-134">nat 게이트웨이 리소스와 연결된 공용 IP 주소의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="fed11-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fed11-135">-PublicIpPrefix</span></span>
<span data-ttu-id="fed11-136">nat 게이트웨이 리소스와 연결된 공용 IP 프리픽스의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="fed11-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fed11-137">-ResourceGroupName</span></span>
<span data-ttu-id="fed11-138">nat 게이트웨이의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="fed11-139">-Sku</span><span class="sxs-lookup"><span data-stu-id="fed11-139">-Sku</span></span>
<span data-ttu-id="fed11-140">NAT 게이트웨이 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-140">Name of a NAT gateway SKU.</span></span>

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

### <span data-ttu-id="fed11-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="fed11-141">-Tag</span></span>
<span data-ttu-id="fed11-142">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-142">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fed11-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="fed11-143">-Zone</span></span>
<span data-ttu-id="fed11-144">Nat Gateway를 배포해야 하는 지역을 표시하는 가용성 영역 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

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

### <span data-ttu-id="fed11-145">-확인</span><span class="sxs-lookup"><span data-stu-id="fed11-145">-Confirm</span></span>
<span data-ttu-id="fed11-146">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fed11-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fed11-147">-WhatIf</span></span>
<span data-ttu-id="fed11-148">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fed11-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fed11-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed11-150">CommonParameters</span></span>
<span data-ttu-id="fed11-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fed11-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed11-152">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fed11-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed11-153">입력</span><span class="sxs-lookup"><span data-stu-id="fed11-153">INPUTS</span></span>

### <span data-ttu-id="fed11-154">System.String</span><span class="sxs-lookup"><span data-stu-id="fed11-154">System.String</span></span>

### <span data-ttu-id="fed11-155">System.Int32</span><span class="sxs-lookup"><span data-stu-id="fed11-155">System.Int32</span></span>

### <span data-ttu-id="fed11-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fed11-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fed11-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="fed11-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="fed11-158">출력</span><span class="sxs-lookup"><span data-stu-id="fed11-158">OUTPUTS</span></span>

### <span data-ttu-id="fed11-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="fed11-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="fed11-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fed11-160">NOTES</span></span>

## <span data-ttu-id="fed11-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fed11-161">RELATED LINKS</span></span>

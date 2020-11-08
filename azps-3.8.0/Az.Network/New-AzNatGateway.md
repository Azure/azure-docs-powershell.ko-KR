---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 49a6a7d817a6b84626b200faada5c36525dc1c91
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043105"
---
# <span data-ttu-id="40f2f-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="40f2f-101">New-AzNatGateway</span></span>

## <span data-ttu-id="40f2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="40f2f-103">공용 Ip 주소/공용 Ip 접두사, IdleTimeoutInMinutes 및 Sku 속성이 있는 새 Nat 게이트웨이 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="40f2f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40f2f-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40f2f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="40f2f-105">DESCRIPTION</span></span>
<span data-ttu-id="40f2f-106">**AzNatGateway** Cmdlet은 Nat 게이트웨이 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="40f2f-107">Natgateway에는 다음이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="40f2f-108">공용 Ip 주소 및/또는 공용 Ip 접두사</span><span class="sxs-lookup"><span data-stu-id="40f2f-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="40f2f-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="40f2f-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="40f2f-110">제품</span><span class="sxs-lookup"><span data-stu-id="40f2f-110">Sku</span></span>
- <span data-ttu-id="40f2f-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40f2f-111">ResourceGroupName</span></span>
- <span data-ttu-id="40f2f-112">Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="40f2f-112">ResourceName</span></span>
- <span data-ttu-id="40f2f-113">Location</span><span class="sxs-lookup"><span data-stu-id="40f2f-113">Location</span></span>

## <span data-ttu-id="40f2f-114">예제의</span><span class="sxs-lookup"><span data-stu-id="40f2f-114">EXAMPLES</span></span>

### <span data-ttu-id="40f2f-115">예제 1: 공용 Ip 주소를 사용 하 여 Nat 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="40f2f-115">Example 1 : Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="40f2f-116">예제 2: 공용 Ip 접두사를 사용 하 여 Nat 게이트웨이 만들기</span><span class="sxs-lookup"><span data-stu-id="40f2f-116">Example 2 : Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="40f2f-117">예제 3: 공개 IP 주소를 사용 하 여 Nat 게이트웨이 만들기 가용성 영역 1</span><span class="sxs-lookup"><span data-stu-id="40f2f-117">Example 3 : Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="40f2f-118">첫 번째 명령은 표준 공용 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="40f2f-119">두 번째 명령은 사용 가능 영역 1에서 공용 IP 주소를 사용 하 여 NAT 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="40f2f-120">변수</span><span class="sxs-lookup"><span data-stu-id="40f2f-120">PARAMETERS</span></span>

### <span data-ttu-id="40f2f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40f2f-121">-AsJob</span></span>
<span data-ttu-id="40f2f-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="40f2f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40f2f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40f2f-123">-DefaultProfile</span></span>
<span data-ttu-id="40f2f-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40f2f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="40f2f-125">-Force</span></span>
<span data-ttu-id="40f2f-126">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="40f2f-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="40f2f-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="40f2f-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="40f2f-128">Nat 게이트웨이의 유휴 시간 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-128">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="40f2f-129">-위치</span><span class="sxs-lookup"><span data-stu-id="40f2f-129">-Location</span></span>
<span data-ttu-id="40f2f-130">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-130">The location.</span></span>

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

### <span data-ttu-id="40f2f-131">-이름</span><span class="sxs-lookup"><span data-stu-id="40f2f-131">-Name</span></span>
<span data-ttu-id="40f2f-132">Nat 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-132">The name of the nat gateway.</span></span>

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

### <span data-ttu-id="40f2f-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="40f2f-133">-PublicIpAddress</span></span>
<span data-ttu-id="40f2f-134">Nat 게이트웨이 리소스에 연결 된 공용 ip 주소의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="40f2f-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="40f2f-135">-PublicIpPrefix</span></span>
<span data-ttu-id="40f2f-136">Nat 게이트웨이 리소스와 연결 된 공용 ip 접두사의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="40f2f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40f2f-137">-ResourceGroupName</span></span>
<span data-ttu-id="40f2f-138">Nat 게이트웨이의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="40f2f-139">-Sku</span><span class="sxs-lookup"><span data-stu-id="40f2f-139">-Sku</span></span>
<span data-ttu-id="40f2f-140">NAT 게이트웨이 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-140">Name of a NAT gateway SKU.</span></span>

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

### <span data-ttu-id="40f2f-141">태그</span><span class="sxs-lookup"><span data-stu-id="40f2f-141">-Tag</span></span>
<span data-ttu-id="40f2f-142">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-142">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="40f2f-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="40f2f-143">-Zone</span></span>
<span data-ttu-id="40f2f-144">Nat 게이트웨이를 배포 해야 하는 영역을 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

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

### <span data-ttu-id="40f2f-145">-확인</span><span class="sxs-lookup"><span data-stu-id="40f2f-145">-Confirm</span></span>
<span data-ttu-id="40f2f-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40f2f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40f2f-147">-WhatIf</span></span>
<span data-ttu-id="40f2f-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40f2f-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40f2f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40f2f-150">CommonParameters</span></span>
<span data-ttu-id="40f2f-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40f2f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40f2f-152">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="40f2f-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40f2f-153">입력</span><span class="sxs-lookup"><span data-stu-id="40f2f-153">INPUTS</span></span>

### <span data-ttu-id="40f2f-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="40f2f-154">System.String</span></span>

### <span data-ttu-id="40f2f-155">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="40f2f-155">System.Int32</span></span>

### <span data-ttu-id="40f2f-156">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="40f2f-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="40f2f-157">Microsoft. 네트워크 모델. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="40f2f-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="40f2f-158">출력</span><span class="sxs-lookup"><span data-stu-id="40f2f-158">OUTPUTS</span></span>

### <span data-ttu-id="40f2f-159">Microsoft. \* .Patgateway.</span><span class="sxs-lookup"><span data-stu-id="40f2f-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="40f2f-160">상속자</span><span class="sxs-lookup"><span data-stu-id="40f2f-160">NOTES</span></span>

## <span data-ttu-id="40f2f-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40f2f-161">RELATED LINKS</span></span>

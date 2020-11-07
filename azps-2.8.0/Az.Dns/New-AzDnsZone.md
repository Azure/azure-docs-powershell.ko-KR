---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 101440e65fbc0bb21311757a8792a2d45f855364
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696554"
---
# <span data-ttu-id="26658-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="26658-101">New-AzDnsZone</span></span>

## <span data-ttu-id="26658-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26658-102">SYNOPSIS</span></span>
<span data-ttu-id="26658-103">새 DNS 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26658-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="26658-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26658-104">SYNTAX</span></span>

### <span data-ttu-id="26658-105">Id (기본값)</span><span class="sxs-lookup"><span data-stu-id="26658-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26658-106">이름은</span><span class="sxs-lookup"><span data-stu-id="26658-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26658-107">나타내는</span><span class="sxs-lookup"><span data-stu-id="26658-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26658-108">설명은</span><span class="sxs-lookup"><span data-stu-id="26658-108">DESCRIPTION</span></span>
<span data-ttu-id="26658-109">**AzDnsZone** cmdlet은 지정 된 리소스 그룹에 새 DNS (Domain Name System) 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26658-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="26658-110">*Name* 매개 변수에 대해 고유한 DNS 영역 이름을 지정 해야 하며, cmdlet이 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="26658-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="26658-111">영역이 만들어지면 New-AzDnsRecordSet cmdlet을 사용 하 여 영역에서 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26658-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="26658-112">*확인* 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26658-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="26658-113">예제의</span><span class="sxs-lookup"><span data-stu-id="26658-113">EXAMPLES</span></span>

### <span data-ttu-id="26658-114">예제 1: DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="26658-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="26658-115">이 명령은 지정 된 리소스 그룹에 myzone.com 이라는 새 DNS 영역을 만든 다음이를 $Zone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="26658-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="26658-116">예제 2: 가상 네트워크 Id를 지정 하 여 개인 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="26658-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="26658-117">이 명령은 지정 된 리소스 그룹에서 myprivatezone.com 이라는 새 개인 DNS 영역을 만들고 해당 ID를 지정 하 여 관련 된 해결 가상 네트워크를 만든 다음이를 $Zone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="26658-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="26658-118">예제 3: 가상 네트워크 개체를 지정 하 여 개인 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="26658-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="26658-119">이 명령은 연결 된 해결 가상 네트워크 ($ResVirtualNetwork 변수)를 사용 하 여 지정 된 리소스 그룹에 myprivatezone.com 이라는 새 개인 DNS 영역을 만든 다음 $Zone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="26658-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="26658-120">예제 4: 부모 영역 이름을 지정 하 여 위임으로 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="26658-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="26658-121">이 명령은 지정 된 리소스 그룹에 mychild.zone.com 이라는 새 자식 DNS 영역을 만들고 $Zone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="26658-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="26658-122">또한 하위 영역과 동일한 구독 및 리소스 그룹에 상주 하는 zone.com 이라는 부모 DNS 영역에 위임을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="26658-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="26658-123">예제 5: 부모 영역 id를 지정 하 여 위임으로 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="26658-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="26658-124">이 명령은 지정 된 리소스 그룹에 mychild.zone.com 이라는 새 자식 DNS 영역을 만들고 $Zone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="26658-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="26658-125">또한 리소스 그룹의 zone.com 이라는 상위 DNS 영역에서 위임을 추가 합니다. 다른-rg 제공 된 구독은 생성 된 자식 영역의 경우와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="26658-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="26658-126">예제 6: 부모 영역 개체를 지정 하 여 위임을 사용 하 여 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="26658-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="26658-127">이 명령은 지정 된 리소스 그룹에 mychild.zone.com 이라는 새 자식 DNS 영역을 만들고 $Zone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="26658-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="26658-128">또한 ParentZone 개체에 전달 된 zone.com 이라는 부모 DNS 영역에서 위임을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="26658-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="26658-129">변수</span><span class="sxs-lookup"><span data-stu-id="26658-129">PARAMETERS</span></span>

### <span data-ttu-id="26658-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26658-130">-DefaultProfile</span></span>
<span data-ttu-id="26658-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="26658-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26658-132">-이름</span><span class="sxs-lookup"><span data-stu-id="26658-132">-Name</span></span>
<span data-ttu-id="26658-133">만들려는 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26658-133">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26658-134">-ParentZone</span><span class="sxs-lookup"><span data-stu-id="26658-134">-ParentZone</span></span>
<span data-ttu-id="26658-135">위임을 추가할 부모 영역의 전체 이름입니다 (종료 점이 없음).</span><span class="sxs-lookup"><span data-stu-id="26658-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26658-136">-ParentZoneId</span><span class="sxs-lookup"><span data-stu-id="26658-136">-ParentZoneId</span></span>
<span data-ttu-id="26658-137">위임을 추가할 상위 영역의 리소스 id (종료 점 없이)입니다.</span><span class="sxs-lookup"><span data-stu-id="26658-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26658-138">-ParentZoneName</span><span class="sxs-lookup"><span data-stu-id="26658-138">-ParentZoneName</span></span>
<span data-ttu-id="26658-139">위임을 추가할 부모 영역의 전체 이름입니다 (종료 점이 없음).</span><span class="sxs-lookup"><span data-stu-id="26658-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Names
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26658-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="26658-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="26658-141">이 DNS 영역에 가상 컴퓨터 호스트 이름 레코드를 등록할 가상 네트워크 목록으로, 개인 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26658-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26658-142">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="26658-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="26658-143">이 DNS 영역에 가상 컴퓨터 호스트 이름 레코드를 등록할 가상 네트워크 Id 목록으로, 개인 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26658-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26658-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="26658-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="26658-145">이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 목록으로, 개인 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26658-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26658-146">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="26658-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="26658-147">이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 Id의 목록이 며, 개인 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26658-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26658-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26658-148">-ResourceGroupName</span></span>
<span data-ttu-id="26658-149">영역을 만들 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26658-149">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26658-150">태그</span><span class="sxs-lookup"><span data-stu-id="26658-150">-Tag</span></span>
<span data-ttu-id="26658-151">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="26658-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="26658-152">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="26658-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26658-153">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="26658-153">-ZoneType</span></span>
<span data-ttu-id="26658-154">영역의 형식 (공개 또는 비공개)입니다.</span><span class="sxs-lookup"><span data-stu-id="26658-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="26658-155">형식이 나 공개 형식이 없는 영역은 DNS 계층에서 사용할 공용 DNS 처리 평면에서 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26658-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="26658-156">비공개 유형의 영역은 연결 된 가상 네트워크 집합 (이 기능은 미리 보기) 에서만 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26658-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="26658-157">이 속성은 영역에 대해 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="26658-157">This property cannot be changed for a zone.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.ZoneType]
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26658-158">-확인</span><span class="sxs-lookup"><span data-stu-id="26658-158">-Confirm</span></span>
<span data-ttu-id="26658-159">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="26658-159">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26658-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26658-160">-WhatIf</span></span>
<span data-ttu-id="26658-161">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="26658-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26658-162">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="26658-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26658-163">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26658-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26658-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26658-164">CommonParameters</span></span>
<span data-ttu-id="26658-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26658-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26658-166">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26658-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26658-167">입력</span><span class="sxs-lookup"><span data-stu-id="26658-167">INPUTS</span></span>

### <span data-ttu-id="26658-168">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="26658-168">System.String</span></span>

### <span data-ttu-id="26658-169">시스템 Null 허용 ' 1 [[ZoneType, Microsoft azure. 관리. Dns, 버전 = 3.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="26658-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="26658-170">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="26658-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="26658-171">System.webserver. List ' 1 [[System.webserver], CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="26658-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="26658-172">System.webserver. List ' 1 [[IResourceReference, Microsoft azure. 31bf3856ad364e35. 클라이언트. 네트워크, 버전 = 1.0.0.0, Culture = 중립, PublicKeyToken =]])</span><span class="sxs-lookup"><span data-stu-id="26658-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="26658-173">출력</span><span class="sxs-lookup"><span data-stu-id="26658-173">OUTPUTS</span></span>

### <span data-ttu-id="26658-174">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="26658-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="26658-175">상속자</span><span class="sxs-lookup"><span data-stu-id="26658-175">NOTES</span></span>
<span data-ttu-id="26658-176">*확인* 매개 변수를 사용 하 여이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26658-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="26658-177">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 변수의 값이 중간 인지 아래 인지 여부를 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="26658-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="26658-178">*확인* 또는 *확인: $True* 를 지정 하는 경우이 cmdlet을 실행 하기 전에 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26658-178">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="26658-179">*확인: $False* 를 지정 하면 cmdlet에서 확인을 요구 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26658-179">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="26658-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26658-180">RELATED LINKS</span></span>

[<span data-ttu-id="26658-181">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="26658-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="26658-182">새로운 AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="26658-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="26658-183">제거-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="26658-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

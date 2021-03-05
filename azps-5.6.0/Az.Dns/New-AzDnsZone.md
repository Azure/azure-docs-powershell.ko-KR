---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: 40f1b40bbb5546e1d38b9c2916ea635aab80c144
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984788"
---
# <span data-ttu-id="afcdc-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="afcdc-101">New-AzDnsZone</span></span>

## <span data-ttu-id="afcdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afcdc-102">SYNOPSIS</span></span>
<span data-ttu-id="afcdc-103">새 DNS 영역 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="afcdc-104">구문</span><span class="sxs-lookup"><span data-stu-id="afcdc-104">SYNTAX</span></span>

### <span data-ttu-id="afcdc-105">ID(기본값)</span><span class="sxs-lookup"><span data-stu-id="afcdc-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afcdc-106">이름</span><span class="sxs-lookup"><span data-stu-id="afcdc-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afcdc-107">개체</span><span class="sxs-lookup"><span data-stu-id="afcdc-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afcdc-108">설명</span><span class="sxs-lookup"><span data-stu-id="afcdc-108">DESCRIPTION</span></span>
<span data-ttu-id="afcdc-109">**New-AzDnsZone cmdlet은** 지정된 리소스 그룹에 새 DNS(도메인 이름 시스템) 지역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="afcdc-110">이름 매개 변수에 대한 고유한  DNS 영역 이름을 지정해야 합니다. 또는 cmdlet에서 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="afcdc-111">영역이 만들어진 후 New-AzDnsRecordSet cmdlet을 사용하여 영역의 레코드 집합을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="afcdc-112">확인 매개  변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="afcdc-113">예제</span><span class="sxs-lookup"><span data-stu-id="afcdc-113">EXAMPLES</span></span>

### <span data-ttu-id="afcdc-114">예제 1: DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="afcdc-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="afcdc-115">이 명령은 지정된 리소스 그룹에 myzone.com 라는 새 DNS $Zone 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="afcdc-116">예제 2: 가상 네트워크 아이디를 지정하여 개인 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="afcdc-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="afcdc-117">이 명령은 연결된 해상도 가상 myprivatezone.com(ID 지정)를 사용하여 지정된 리소스 그룹에 새 개인 DNS $Zone 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="afcdc-118">예제 3: 가상 네트워크 개체를 지정하여 개인 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="afcdc-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="afcdc-119">이 명령은 연결된 해상도 가상 네트워크(myprivatezone.com 변수로 참조)를 사용하여 지정된 리소스 그룹에 새 개인 DNS 영역($ResVirtualNetwork)을 만든 다음, 해당 $Zone 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="afcdc-120">예제 4: 상위 영역 이름을 지정하여 위임이 있는 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="afcdc-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="afcdc-121">이 명령은 지정된 리소스 그룹에 mychild.zone.com 라는 새 자식 DNS $Zone 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="afcdc-122">또한 자식 영역과 동일한 구독 및 리소스 그룹에 zone.com 라는 부모 DNS 영역의 위임도 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="afcdc-123">예제 5: 상위 영역 ID를 지정하여 위임이 있는 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="afcdc-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="afcdc-124">이 명령은 지정된 리소스 그룹에 mychild.zone.com 라는 새 자식 DNS $Zone 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="afcdc-125">또한 리소스 그룹에서 zone.com 하위 영역과 동일하게 제공된 구독의 부모 DNS 영역의 위임도 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="afcdc-126">예제 6: 상위 영역 개체를 지정하여 위임이 있는 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="afcdc-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="afcdc-127">이 명령은 지정된 리소스 그룹에 mychild.zone.com 라는 새 자식 DNS $Zone 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="afcdc-128">또한 ParentZone 개체에 전달된 zone.com DNS라는 부모 DNS 영역의 위임도 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="afcdc-129">매개 변수</span><span class="sxs-lookup"><span data-stu-id="afcdc-129">PARAMETERS</span></span>

### <span data-ttu-id="afcdc-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afcdc-130">-DefaultProfile</span></span>
<span data-ttu-id="afcdc-131">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="afcdc-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="afcdc-132">-Name</span><span class="sxs-lookup"><span data-stu-id="afcdc-132">-Name</span></span>
<span data-ttu-id="afcdc-133">만들 DNS 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-133">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="afcdc-134">-ParentZone</span><span class="sxs-lookup"><span data-stu-id="afcdc-134">-ParentZone</span></span>
<span data-ttu-id="afcdc-135">위임(종료점 없이)을 추가할 부모 영역의 전체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="afcdc-136">-ParentZoneId</span><span class="sxs-lookup"><span data-stu-id="afcdc-136">-ParentZoneId</span></span>
<span data-ttu-id="afcdc-137">위임(종료점 없이)을 추가할 부모 영역의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="afcdc-138">-ParentZoneName</span><span class="sxs-lookup"><span data-stu-id="afcdc-138">-ParentZoneName</span></span>
<span data-ttu-id="afcdc-139">위임(종료점 없이)을 추가할 부모 영역의 전체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="afcdc-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="afcdc-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="afcdc-141">이 DNS 영역의 가상 머신 호스트 이름을 등록하는 가상 네트워크 목록입니다. 개인 영역만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="afcdc-142">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="afcdc-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="afcdc-143">이 DNS 영역의 가상 머신 호스트 이름 레코드를 등록하는 가상 네트워크 아이디 목록은 개인 영역만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="afcdc-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="afcdc-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="afcdc-145">이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 목록은 개인 영역만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="afcdc-146">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="afcdc-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="afcdc-147">이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 아이디 목록은 개인 영역에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="afcdc-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afcdc-148">-ResourceGroupName</span></span>
<span data-ttu-id="afcdc-149">영역 만들기를 위한 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-149">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="afcdc-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="afcdc-150">-Tag</span></span>
<span data-ttu-id="afcdc-151">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="afcdc-152">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="afcdc-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="afcdc-153">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="afcdc-153">-ZoneType</span></span>
<span data-ttu-id="afcdc-154">영역의 형식, 공용 또는 개인입니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="afcdc-155">형식이 없는 영역 또는 공용 형식이 있는 영역은 DNS 계층 구조에서 사용할 수 있도록 공용 DNS 제공 평면에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="afcdc-156">개인 유형이 있는 영역은 연결된 가상 네트워크 집합에서만 볼 수 있습니다(이 기능은 미리 보기 상태입니다).</span><span class="sxs-lookup"><span data-stu-id="afcdc-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="afcdc-157">영역의 경우 이 속성을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-157">This property cannot be changed for a zone.</span></span>

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

### <span data-ttu-id="afcdc-158">-확인</span><span class="sxs-lookup"><span data-stu-id="afcdc-158">-Confirm</span></span>
<span data-ttu-id="afcdc-159">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afcdc-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afcdc-160">-WhatIf</span></span>
<span data-ttu-id="afcdc-161">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afcdc-162">cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afcdc-163">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afcdc-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afcdc-164">CommonParameters</span></span>
<span data-ttu-id="afcdc-165">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afcdc-166">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="afcdc-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afcdc-167">입력</span><span class="sxs-lookup"><span data-stu-id="afcdc-167">INPUTS</span></span>

### <span data-ttu-id="afcdc-168">System.String</span><span class="sxs-lookup"><span data-stu-id="afcdc-168">System.String</span></span>

### <span data-ttu-id="afcdc-169">System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="afcdc-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="afcdc-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="afcdc-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="afcdc-171">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="afcdc-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="afcdc-172">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="afcdc-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="afcdc-173">출력</span><span class="sxs-lookup"><span data-stu-id="afcdc-173">OUTPUTS</span></span>

### <span data-ttu-id="afcdc-174">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="afcdc-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="afcdc-175">참고 사항</span><span class="sxs-lookup"><span data-stu-id="afcdc-175">NOTES</span></span>
<span data-ttu-id="afcdc-176">확인 매개  변수를 사용하여 이 cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="afcdc-177">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 값이 중간 또는 더 낮은지 확인하라는 메시지를 묻는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="afcdc-178">확인 또는 *확인:$True* 지정하는 경우 이 cmdlet은 실행하기 전에 확인을 묻는 메시지를 표시합니다. </span><span class="sxs-lookup"><span data-stu-id="afcdc-178">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="afcdc-179">*Confirm:$False* 지정하면 cmdlet에서 확인을 묻는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="afcdc-179">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="afcdc-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="afcdc-180">RELATED LINKS</span></span>

[<span data-ttu-id="afcdc-181">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="afcdc-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="afcdc-182">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="afcdc-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="afcdc-183">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="afcdc-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

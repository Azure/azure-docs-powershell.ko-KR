---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/new-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsZone.md
ms.openlocfilehash: dc110c8989951c6cf5a68e35fbc22c6545c84a1a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346874"
---
# <span data-ttu-id="93fc6-101">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="93fc6-101">New-AzDnsZone</span></span>

## <span data-ttu-id="93fc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="93fc6-103">새 DNS 영역이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-103">Creates a new DNS zone.</span></span>

## <span data-ttu-id="93fc6-104">구문</span><span class="sxs-lookup"><span data-stu-id="93fc6-104">SYNTAX</span></span>

### <span data-ttu-id="93fc6-105">ID(기본값)</span><span class="sxs-lookup"><span data-stu-id="93fc6-105">Ids (Default)</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneId <String>]
 [-Tag <Hashtable>] [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93fc6-106">이름</span><span class="sxs-lookup"><span data-stu-id="93fc6-106">Names</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZoneName <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93fc6-107">개체</span><span class="sxs-lookup"><span data-stu-id="93fc6-107">Objects</span></span>
```
New-AzDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-ParentZone <DnsZone>]
 [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93fc6-108">설명</span><span class="sxs-lookup"><span data-stu-id="93fc6-108">DESCRIPTION</span></span>
<span data-ttu-id="93fc6-109">**New-AzDnsZone** cmdlet은 지정된 리소스 그룹에 새 DNS(도메인 이름 시스템) 영역이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-109">The **New-AzDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="93fc6-110">Name 매개 변수에 대해 고유한  DNS 영역 이름을 지정해야 합니다. 또는 cmdlet에서 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-110">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="93fc6-111">영역이 만들어진 후 New-AzDnsRecordSet cmdlet을 사용하여 영역의 레코드 집합을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-111">After the zone is created, use the New-AzDnsRecordSet cmdlet to create record sets in the zone.</span></span>
<span data-ttu-id="93fc6-112">*Confirm* 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="93fc6-113">예제</span><span class="sxs-lookup"><span data-stu-id="93fc6-113">EXAMPLES</span></span>

### <span data-ttu-id="93fc6-114">예제 1: DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="93fc6-114">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="93fc6-115">이 명령은 지정된 리소스 myzone.com 이름의 새 DNS $Zone 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-115">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="93fc6-116">예제 2: 가상 네트워크 ID를 지정하여 개인 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="93fc6-116">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="93fc6-117">이 명령은 연결된 확인 가상 myprivatezone.com 사용하여 지정된 리소스 그룹에 이름의 새 개인 DNS 영역(ID 지정)을 만든 다음 $Zone 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-117">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="93fc6-118">예제 3: 가상 네트워크 개체를 지정하여 개인 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="93fc6-118">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="93fc6-119">이 명령은 연결된 확인 가상 네트워크($ResVirtualNetwork 변수로 참조)를 사용하여 지정된 리소스 그룹에 myprivatezone.com 이름의 새 개인 DNS 영역이 만들어진 다음 $Zone 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-119">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="93fc6-120">예제 4: 부모 영역 이름을 지정하여 위임이 있는 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="93fc6-120">Example 4: Create a DNS zone with delegation by specifying parent zone name</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneName "zone.com"
```

<span data-ttu-id="93fc6-121">이 명령은 지정된 리소스 mychild.zone.com 이름의 새 자식 DNS $Zone 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-121">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="93fc6-122">또한 자식 영역과 동일한 구독 zone.com 리소스 그룹에 있는 부모 DNS 영역의 위임도 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-122">It also adds delegation in the parent DNS zone named zone.com residing in the same subscription and resource group as child zone.</span></span>

### <span data-ttu-id="93fc6-123">예제 5: 부모 영역 ID를 지정하여 위임이 있는 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="93fc6-123">Example 5: Create a DNS zone with delegation by specifying parent zone id</span></span>
```
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZoneId "/subscriptions/**67e2/resourceGroups/other-rg/providers/Microsoft.Network/dnszones/zone.com"
```

<span data-ttu-id="93fc6-124">이 명령은 지정된 리소스 mychild.zone.com 이름의 새 자식 DNS $Zone 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-124">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="93fc6-125">또한 다른 rg가 제공한 구독이 만든 자식 영역과 zone.com 리소스 그룹에 있는 부모 DNS 영역의 위임도 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-125">It also adds delegation in the parent DNS zone named zone.com in resource group other-rg provided subscription is same as that of child zone created.</span></span>

### <span data-ttu-id="93fc6-126">예제 6: 부모 영역 개체를 지정하여 위임이 있는 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="93fc6-126">Example 6: Create a DNS zone with delegation by specifying parent zone object</span></span>
```
PS C:\>$PZone = New-AzDnsZone -Name "zone.com" -ResourceGroupName "MyResourceGroup" 
PS C:\>$Zone = New-AzDnsZone -Name "mychild.zone.com" -ResourceGroupName "MyResourceGroup" -ParentZone @($PZone)
```

<span data-ttu-id="93fc6-127">이 명령은 지정된 리소스 mychild.zone.com 이름의 새 자식 DNS $Zone 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-127">This command creates a new child DNS zone named mychild.zone.com in the specified resource group and stores in the $Zone variable.</span></span>
<span data-ttu-id="93fc6-128">또한 ParentZone 개체에 전달된 zone.com DNS 영역의 위임도 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-128">It also adds delegation in the parent DNS zone named zone.com as passed in the ParentZone object</span></span>

## <span data-ttu-id="93fc6-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93fc6-129">PARAMETERS</span></span>

### <span data-ttu-id="93fc6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93fc6-130">-DefaultProfile</span></span>
<span data-ttu-id="93fc6-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="93fc6-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93fc6-132">-Name</span><span class="sxs-lookup"><span data-stu-id="93fc6-132">-Name</span></span>
<span data-ttu-id="93fc6-133">만들 DNS 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-133">Specifies the name of the DNS zone to create.</span></span>

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

### <span data-ttu-id="93fc6-134">-ParentZone</span><span class="sxs-lookup"><span data-stu-id="93fc6-134">-ParentZone</span></span>
<span data-ttu-id="93fc6-135">위임(종료 점 없이)을 추가할 부모 영역의 전체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-135">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="93fc6-136">-ParentZoneId</span><span class="sxs-lookup"><span data-stu-id="93fc6-136">-ParentZoneId</span></span>
<span data-ttu-id="93fc6-137">위임(종료 점 없이)을 추가할 부모 영역의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-137">The resource id of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="93fc6-138">-ParentZoneName</span><span class="sxs-lookup"><span data-stu-id="93fc6-138">-ParentZoneName</span></span>
<span data-ttu-id="93fc6-139">위임(종료 점 없이)을 추가할 부모 영역의 전체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-139">The full name of the parent zone to add delegation (without a terminating dot).</span></span>

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

### <span data-ttu-id="93fc6-140">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="93fc6-140">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="93fc6-141">이 DNS 영역의 가상 머신 호스트 이름 레코드를 등록할 가상 네트워크 목록으로, 사설 영역만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-141">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="93fc6-142">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="93fc6-142">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="93fc6-143">이 DNS 영역의 가상 머신 호스트 이름 레코드를 등록할 가상 네트워크 신분의 목록으로, 사설 영역만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-143">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="93fc6-144">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="93fc6-144">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="93fc6-145">이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 목록으로, 사설 영역만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-145">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="93fc6-146">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="93fc6-146">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="93fc6-147">이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 신분의 목록으로, 사설 영역만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-147">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="93fc6-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93fc6-148">-ResourceGroupName</span></span>
<span data-ttu-id="93fc6-149">영역 만들기에 사용할 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-149">Specifies the resource group in which to create the zone.</span></span>

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

### <span data-ttu-id="93fc6-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="93fc6-150">-Tag</span></span>
<span data-ttu-id="93fc6-151">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="93fc6-152">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="93fc6-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="93fc6-153">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="93fc6-153">-ZoneType</span></span>
<span data-ttu-id="93fc6-154">영역의 유형( 공용 또는 개인).</span><span class="sxs-lookup"><span data-stu-id="93fc6-154">The type of the zone, Public or Private.</span></span> <span data-ttu-id="93fc6-155">형식이 없는 영역 또는 공용 형식이 있는 영역은 DNS 계층 구조에서 사용할 공용 DNS 서비스 평면에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-155">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="93fc6-156">개인 유형이 있는 영역은 연결된 가상 네트워크 집합에서만 볼 수 있습니다(이 기능은 미리 보기 상태).</span><span class="sxs-lookup"><span data-stu-id="93fc6-156">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="93fc6-157">이 속성은 영역으로 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-157">This property cannot be changed for a zone.</span></span>

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

### <span data-ttu-id="93fc6-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93fc6-158">-Confirm</span></span>
<span data-ttu-id="93fc6-159">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93fc6-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93fc6-160">-WhatIf</span></span>
<span data-ttu-id="93fc6-161">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="93fc6-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93fc6-162">cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="93fc6-162">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93fc6-163">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93fc6-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93fc6-164">CommonParameters</span></span>
<span data-ttu-id="93fc6-165">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93fc6-166">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="93fc6-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93fc6-167">입력</span><span class="sxs-lookup"><span data-stu-id="93fc6-167">INPUTS</span></span>

### <span data-ttu-id="93fc6-168">System.String</span><span class="sxs-lookup"><span data-stu-id="93fc6-168">System.String</span></span>

### <span data-ttu-id="93fc6-169">System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="93fc6-169">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.ZoneType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="93fc6-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="93fc6-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="93fc6-171">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="93fc6-171">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="93fc6-172">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="93fc6-172">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="93fc6-173">출력</span><span class="sxs-lookup"><span data-stu-id="93fc6-173">OUTPUTS</span></span>

### <span data-ttu-id="93fc6-174">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="93fc6-174">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="93fc6-175">참고 사항</span><span class="sxs-lookup"><span data-stu-id="93fc6-175">NOTES</span></span>
<span data-ttu-id="93fc6-176">*확인* 매개 변수를 사용하여 이 cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-176">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="93fc6-177">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 값이 Medium 또는 lower인 경우 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-177">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="93fc6-178">*Confirm* 또는 *Confirm:$True* 지정하는 경우 이 cmdlet은 실행 전에 확인을 요청하는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-178">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="93fc6-179">*Confirm:$False* 지정하면 cmdlet에서 확인 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93fc6-179">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="93fc6-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93fc6-180">RELATED LINKS</span></span>

[<span data-ttu-id="93fc6-181">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="93fc6-181">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="93fc6-182">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="93fc6-182">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="93fc6-183">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="93fc6-183">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

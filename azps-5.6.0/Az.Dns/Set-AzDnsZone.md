---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: d1b5fb606262b680d4e83f9c8e0a9ea166070ed4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984699"
---
# <span data-ttu-id="0c25b-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="0c25b-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="0c25b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c25b-102">SYNOPSIS</span></span>
<span data-ttu-id="0c25b-103">DNS 영역의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="0c25b-104">구문</span><span class="sxs-lookup"><span data-stu-id="0c25b-104">SYNTAX</span></span>

### <span data-ttu-id="0c25b-105">필드(기본값)</span><span class="sxs-lookup"><span data-stu-id="0c25b-105">Fields (Default)</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c25b-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="0c25b-106">FieldsObjects</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c25b-107">개체</span><span class="sxs-lookup"><span data-stu-id="0c25b-107">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c25b-108">설명</span><span class="sxs-lookup"><span data-stu-id="0c25b-108">DESCRIPTION</span></span>
<span data-ttu-id="0c25b-109">**Set-AzDnsZone** cmdlet은 Azure DNS 서비스에서 지정된 DNS 영역이 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-109">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="0c25b-110">이 cmdlet은 영역의 레코드 집합을 업데이트하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-110">This cmdlet does not update the record sets in the zone.</span></span>
<span data-ttu-id="0c25b-111">**DnsZone** 개체를 매개 변수로 전달하거나 파이프라인 연산자를 사용하여 전달하거나 *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="0c25b-112">확인 매개  변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="0c25b-113">DNS 영역이 개체(영역 개체 또는 파이프라인을 통해)로 전달하는 경우 로컬 DnsZone 개체를 검색한 후 Azure DNS에서 변경된 경우 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="0c25b-114">이 기능은 동시 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="0c25b-115">동시 변경 내용에  관계없이 영역이 업데이트되는 덮어 덮어 사용 매개 변수를 사용하여 이 동작을 억제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="0c25b-116">예제</span><span class="sxs-lookup"><span data-stu-id="0c25b-116">EXAMPLES</span></span>

### <span data-ttu-id="0c25b-117">예제 1: DNS 영역 업데이트</span><span class="sxs-lookup"><span data-stu-id="0c25b-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="0c25b-118">첫 번째 명령은 지정된 리소스 myzone.com 그룹에서 $Zone 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>
<span data-ttu-id="0c25b-119">두 번째 명령은 에 대한 태그를 $Zone.</span><span class="sxs-lookup"><span data-stu-id="0c25b-119">The second command updates the tags for $Zone.</span></span>
<span data-ttu-id="0c25b-120">최종 명령은 변경을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-120">The final command commits the change.</span></span>

### <span data-ttu-id="0c25b-121">예제 2: 영역의 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="0c25b-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="0c25b-122">이 명령은 먼저 구역을 명시적으로 지정하지 않고 myzone.com 영역의 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="0c25b-123">예제 3: ID를 지정하여 가상 네트워크와 개인 영역 연결</span><span class="sxs-lookup"><span data-stu-id="0c25b-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="0c25b-124">이 명령은 ID를 지정하여 myprivatezone.com 가상 네트워크 myvnet과 개인 DNS 영역과 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="0c25b-125">예제 4: 네트워크 개체를 지정하여 가상 네트워크와 개인 영역 연결</span><span class="sxs-lookup"><span data-stu-id="0c25b-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="0c25b-126">이 명령은 myprivatezone.com 변수로 나타내는 가상 네트워크 개체를 $vnet cmdlet에 전달하여 가상 네트워크 myvnet과 개인 DNS 영역 Set-AzDnsZone 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzDnsZone cmdlet.</span></span>

## <span data-ttu-id="0c25b-127">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0c25b-127">PARAMETERS</span></span>

### <span data-ttu-id="0c25b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c25b-128">-DefaultProfile</span></span>
<span data-ttu-id="0c25b-129">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0c25b-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c25b-130">-Name</span><span class="sxs-lookup"><span data-stu-id="0c25b-130">-Name</span></span>
<span data-ttu-id="0c25b-131">업데이트할 DNS 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-131">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c25b-132">-덮어 덮어 덮어 덮어 덮어</span><span class="sxs-lookup"><span data-stu-id="0c25b-132">-Overwrite</span></span>
<span data-ttu-id="0c25b-133">DNS 영역이 개체(영역 개체 또는 파이프라인을 통해)로 전달하는 경우 로컬 DnsZone 개체를 검색한 후 Azure DNS에서 변경된 경우 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="0c25b-134">이 기능은 동시 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="0c25b-135">동시 변경 내용에  관계없이 영역이 업데이트되는 덮어 덮어 사용 매개 변수를 사용하여 이 동작을 억제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c25b-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0c25b-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="0c25b-137">이 DNS 영역의 가상 머신 호스트 이름을 등록하는 가상 네트워크 목록입니다. 개인 영역만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c25b-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="0c25b-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="0c25b-139">이 DNS 영역의 가상 머신 호스트 이름 레코드를 등록하는 가상 네트워크 아이디 목록은 개인 영역만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c25b-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0c25b-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="0c25b-141">이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 목록은 개인 영역만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: FieldsObjects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c25b-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="0c25b-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="0c25b-143">이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 아이디 목록은 개인 영역에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c25b-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c25b-144">-ResourceGroupName</span></span>
<span data-ttu-id="0c25b-145">업데이트할 영역이 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="0c25b-146">ZoneName 매개 변수도 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-146">You must also specify the ZoneName parameter.</span></span>
<span data-ttu-id="0c25b-147">또는 영역 매개 변수 또는 파이프라인을 사용하여 DnsZone 개체를 사용하여 영역을 지정할 수 있습니다. </span><span class="sxs-lookup"><span data-stu-id="0c25b-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c25b-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="0c25b-148">-Tag</span></span>
<span data-ttu-id="0c25b-149">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0c25b-150">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="0c25b-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c25b-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="0c25b-151">-Zone</span></span>
<span data-ttu-id="0c25b-152">업데이트할 DNS 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-152">Specifies the DNS zone to update.</span></span>
<span data-ttu-id="0c25b-153">또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용하여 지역을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-153">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c25b-154">-확인</span><span class="sxs-lookup"><span data-stu-id="0c25b-154">-Confirm</span></span>
<span data-ttu-id="0c25b-155">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c25b-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c25b-156">-WhatIf</span></span>
<span data-ttu-id="0c25b-157">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c25b-158">cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-158">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c25b-159">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c25b-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c25b-160">CommonParameters</span></span>
<span data-ttu-id="0c25b-161">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c25b-162">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0c25b-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c25b-163">입력</span><span class="sxs-lookup"><span data-stu-id="0c25b-163">INPUTS</span></span>

### <span data-ttu-id="0c25b-164">System.String</span><span class="sxs-lookup"><span data-stu-id="0c25b-164">System.String</span></span>

### <span data-ttu-id="0c25b-165">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0c25b-165">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0c25b-166">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0c25b-166">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0c25b-167">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0c25b-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0c25b-168">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="0c25b-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="0c25b-169">출력</span><span class="sxs-lookup"><span data-stu-id="0c25b-169">OUTPUTS</span></span>

### <span data-ttu-id="0c25b-170">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="0c25b-170">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="0c25b-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0c25b-171">NOTES</span></span>
<span data-ttu-id="0c25b-172">확인 매개  변수를 사용하여 이 cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-172">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="0c25b-173">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 값이 중간 또는 더 낮은지 확인하라는 메시지를 묻는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-173">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="0c25b-174">확인 또는 *확인:$True* 지정하는 경우 이 cmdlet은 실행하기 전에 확인을 묻는 메시지를 표시합니다. </span><span class="sxs-lookup"><span data-stu-id="0c25b-174">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="0c25b-175">*Confirm:$False* 지정하면 cmdlet에서 확인을 묻는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c25b-175">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0c25b-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c25b-176">RELATED LINKS</span></span>

[<span data-ttu-id="0c25b-177">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="0c25b-177">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="0c25b-178">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="0c25b-178">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="0c25b-179">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="0c25b-179">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

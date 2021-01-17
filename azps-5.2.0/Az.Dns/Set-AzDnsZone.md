---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 956dbc54d565c4aed074df54b550f8c8aa7b18ac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346790"
---
# <span data-ttu-id="9e59c-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="9e59c-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="9e59c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e59c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e59c-103">DNS 영역의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="9e59c-104">구문</span><span class="sxs-lookup"><span data-stu-id="9e59c-104">SYNTAX</span></span>

### <span data-ttu-id="9e59c-105">필드(기본값)</span><span class="sxs-lookup"><span data-stu-id="9e59c-105">Fields (Default)</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e59c-106">FieldsObjects</span><span class="sxs-lookup"><span data-stu-id="9e59c-106">FieldsObjects</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e59c-107">개체</span><span class="sxs-lookup"><span data-stu-id="9e59c-107">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e59c-108">설명</span><span class="sxs-lookup"><span data-stu-id="9e59c-108">DESCRIPTION</span></span>
<span data-ttu-id="9e59c-109">**Set-AzDnsZone** cmdlet은 Azure DNS 서비스에서 지정된 DNS 영역이 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-109">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="9e59c-110">이 cmdlet은 영역의 레코드 집합을 업데이트하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-110">This cmdlet does not update the record sets in the zone.</span></span>
<span data-ttu-id="9e59c-111">**DnsZone** 개체를 매개 변수로 전달하거나 파이프라인 연산자를 사용하여 전달하거나 *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="9e59c-112">*Confirm* 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="9e59c-113">DNS 영역이 개체로 전달될 때(Zone 개체 사용 또는 파이프라인을 통해) 로컬 DnsZone 개체가 검색된 이후 Azure DNS에서 변경된 경우 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="9e59c-114">이렇게 하면 동시 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="9e59c-115">동시 변경 내용에 관계없이 영역이 업데이트되는 *덮어* 사용 매개 변수를 사용하면 이 동작을 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="9e59c-116">예제</span><span class="sxs-lookup"><span data-stu-id="9e59c-116">EXAMPLES</span></span>

### <span data-ttu-id="9e59c-117">예제 1: DNS 영역 업데이트</span><span class="sxs-lookup"><span data-stu-id="9e59c-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="9e59c-118">첫 번째 명령은 지정된 리소스 myzone.com 그룹에서 이름이 지정된 영역으로 지정된 $Zone 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>
<span data-ttu-id="9e59c-119">두 번째 명령은 다음에 대한 태그를 $Zone.</span><span class="sxs-lookup"><span data-stu-id="9e59c-119">The second command updates the tags for $Zone.</span></span>
<span data-ttu-id="9e59c-120">마지막 명령은 변경을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-120">The final command commits the change.</span></span>

### <span data-ttu-id="9e59c-121">예제 2: 영역의 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="9e59c-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="9e59c-122">이 명령은 먼저 명시적으로 영역이 myzone.com 이름의 영역 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="9e59c-123">예제 3: ID를 지정하여 개인 영역과 가상 네트워크 연결</span><span class="sxs-lookup"><span data-stu-id="9e59c-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="9e59c-124">이 명령은 ID를 myprivatezone.com 등록 네트워크로 가상 네트워크 myvnet과 개인 DNS 영역 서버를 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="9e59c-125">예제 4: 네트워크 개체를 지정하여 개인 영역과 가상 네트워크 연결</span><span class="sxs-lookup"><span data-stu-id="9e59c-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="9e59c-126">이 명령은 $vnet 변수로 표현되는 가상 네트워크 개체를 myprivatezone.com cmdlet에 전달하여 가상 네트워크 myvnet과 개인 DNS 영역 Set-AzDnsZone 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzDnsZone cmdlet.</span></span>

## <span data-ttu-id="9e59c-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e59c-127">PARAMETERS</span></span>

### <span data-ttu-id="9e59c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e59c-128">-DefaultProfile</span></span>
<span data-ttu-id="9e59c-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9e59c-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e59c-130">-Name</span><span class="sxs-lookup"><span data-stu-id="9e59c-130">-Name</span></span>
<span data-ttu-id="9e59c-131">업데이트할 DNS 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-131">Specifies the name of the DNS zone to update.</span></span>

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

### <span data-ttu-id="9e59c-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="9e59c-132">-Overwrite</span></span>
<span data-ttu-id="9e59c-133">DNS 영역이 개체로 전달될 때(Zone 개체 사용 또는 파이프라인을 통해) 로컬 DnsZone 개체가 검색된 이후 Azure DNS에서 변경된 경우 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="9e59c-134">이렇게 하면 동시 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="9e59c-135">동시 변경 내용에 관계없이 영역이 업데이트되는 *덮어* 사용 매개 변수를 사용하면 이 동작을 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="9e59c-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e59c-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="9e59c-137">이 DNS 영역의 가상 머신 호스트 이름 레코드를 등록할 가상 네트워크 목록으로, 사설 영역만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="9e59c-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="9e59c-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="9e59c-139">이 DNS 영역의 가상 머신 호스트 이름 레코드를 등록할 가상 네트워크 신분의 목록으로, 사설 영역만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="9e59c-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e59c-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="9e59c-141">이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 목록으로, 사설 영역만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="9e59c-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="9e59c-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="9e59c-143">이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 신분의 목록으로, 사설 영역만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="9e59c-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e59c-144">-ResourceGroupName</span></span>
<span data-ttu-id="9e59c-145">업데이트할 영역이 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="9e59c-146">ZoneName 매개 변수도 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-146">You must also specify the ZoneName parameter.</span></span>
<span data-ttu-id="9e59c-147">또는 Zone 매개 변수 또는 파이프라인과 함께 DnsZone 개체를 사용하여 영역을 지정할 수 있습니다. </span><span class="sxs-lookup"><span data-stu-id="9e59c-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

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

### <span data-ttu-id="9e59c-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e59c-148">-Tag</span></span>
<span data-ttu-id="9e59c-149">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9e59c-150">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="9e59c-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9e59c-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="9e59c-151">-Zone</span></span>
<span data-ttu-id="9e59c-152">업데이트할 DNS 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-152">Specifies the DNS zone to update.</span></span>
<span data-ttu-id="9e59c-153">또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용하여 지역을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-153">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="9e59c-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e59c-154">-Confirm</span></span>
<span data-ttu-id="9e59c-155">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e59c-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e59c-156">-WhatIf</span></span>
<span data-ttu-id="9e59c-157">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9e59c-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e59c-158">cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9e59c-158">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e59c-159">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e59c-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e59c-160">CommonParameters</span></span>
<span data-ttu-id="9e59c-161">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e59c-162">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9e59c-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e59c-163">입력</span><span class="sxs-lookup"><span data-stu-id="9e59c-163">INPUTS</span></span>

### <span data-ttu-id="9e59c-164">System.String</span><span class="sxs-lookup"><span data-stu-id="9e59c-164">System.String</span></span>

### <span data-ttu-id="9e59c-165">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9e59c-165">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9e59c-166">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9e59c-166">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9e59c-167">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9e59c-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="9e59c-168">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="9e59c-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="9e59c-169">출력</span><span class="sxs-lookup"><span data-stu-id="9e59c-169">OUTPUTS</span></span>

### <span data-ttu-id="9e59c-170">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="9e59c-170">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="9e59c-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9e59c-171">NOTES</span></span>
<span data-ttu-id="9e59c-172">*확인* 매개 변수를 사용하여 이 cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-172">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="9e59c-173">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 값이 Medium 또는 lower인 경우 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-173">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="9e59c-174">*Confirm* 또는 *Confirm:$True* 지정하는 경우 이 cmdlet은 실행 전에 확인을 요청하는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-174">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="9e59c-175">*Confirm:$False* 지정하면 cmdlet에서 확인 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e59c-175">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9e59c-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e59c-176">RELATED LINKS</span></span>

[<span data-ttu-id="9e59c-177">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="9e59c-177">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="9e59c-178">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="9e59c-178">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="9e59c-179">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="9e59c-179">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

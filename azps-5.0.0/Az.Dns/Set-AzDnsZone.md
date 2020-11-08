---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 956dbc54d565c4aed074df54b550f8c8aa7b18ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218717"
---
# <span data-ttu-id="8f69d-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8f69d-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="8f69d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f69d-102">SYNOPSIS</span></span>
<span data-ttu-id="8f69d-103">DNS 영역의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="8f69d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f69d-104">SYNTAX</span></span>

### <span data-ttu-id="8f69d-105">필드 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8f69d-105">Fields (Default)</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f69d-106">Fieldobjects</span><span class="sxs-lookup"><span data-stu-id="8f69d-106">FieldsObjects</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f69d-107">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="8f69d-107">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f69d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8f69d-108">DESCRIPTION</span></span>
<span data-ttu-id="8f69d-109">**AzDnsZone** Cmdlet은 Azure DNS 서비스에서 지정 된 DNS 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-109">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="8f69d-110">이 cmdlet은 영역의 레코드 집합을 업데이트 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-110">This cmdlet does not update the record sets in the zone.</span></span>
<span data-ttu-id="8f69d-111">**DnsZone** 개체를 매개 변수 또는 파이프라인 연산자를 사용 하 여 전달 하거나 *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="8f69d-112">*확인* 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="8f69d-113">영역 개체를 사용 하거나 파이프라인을 통해 DNS 영역을 개체로 전달 하는 경우 로컬 DnsZone 개체가 검색 된 후 Azure DNS에서 변경 된 경우 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="8f69d-114">이는 동시 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="8f69d-115">*덮어쓰기* 매개 변수를 사용 하 여이 동작을 억제할 수 있으며,이 동작은 동시 변경에 관계 없이 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="8f69d-116">예제의</span><span class="sxs-lookup"><span data-stu-id="8f69d-116">EXAMPLES</span></span>

### <span data-ttu-id="8f69d-117">예제 1: DNS 영역 업데이트</span><span class="sxs-lookup"><span data-stu-id="8f69d-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="8f69d-118">첫 번째 명령은 지정 된 리소스 그룹에서 myzone.com 이라는 영역을 가져온 다음이를 $Zone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>
<span data-ttu-id="8f69d-119">두 번째 명령은 $Zone에 대 한 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-119">The second command updates the tags for $Zone.</span></span>
<span data-ttu-id="8f69d-120">마지막 명령은 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-120">The final command commits the change.</span></span>

### <span data-ttu-id="8f69d-121">예제 2: 영역의 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="8f69d-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="8f69d-122">이 명령은 먼저 영역을 명시적으로 가져오지 않고 myzone.com 이라는 영역에 대 한 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="8f69d-123">예제 3: ID를 지정 하 여 개인 영역을 가상 네트워크와 연결</span><span class="sxs-lookup"><span data-stu-id="8f69d-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="8f69d-124">이 명령은 ID를 지정 하 여 개인 DNS 영역 myprivatezone.com을 가상 네트워크 myvnet과 함께 등록 네트워크로 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="8f69d-125">예제 4: 네트워크 개체를 지정 하 여 개인 영역을 가상 네트워크와 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzVirtualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="8f69d-126">이 명령은 $vnet 변수로 표시 되는 가상 네트워크 개체를 Set-AzDnsZone cmdlet으로 전달 하 여 가상 네트워크 myvnet과 myprivatezone.com의 사설 DNS 영역을 등록 네트워크로 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzDnsZone cmdlet.</span></span>

## <span data-ttu-id="8f69d-127">변수</span><span class="sxs-lookup"><span data-stu-id="8f69d-127">PARAMETERS</span></span>

### <span data-ttu-id="8f69d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f69d-128">-DefaultProfile</span></span>
<span data-ttu-id="8f69d-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8f69d-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f69d-130">-이름</span><span class="sxs-lookup"><span data-stu-id="8f69d-130">-Name</span></span>
<span data-ttu-id="8f69d-131">업데이트할 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-131">Specifies the name of the DNS zone to update.</span></span>

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

### <span data-ttu-id="8f69d-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="8f69d-132">-Overwrite</span></span>
<span data-ttu-id="8f69d-133">영역 개체를 사용 하거나 파이프라인을 통해 DNS 영역을 개체로 전달 하는 경우 로컬 DnsZone 개체가 검색 된 후 Azure DNS에서 변경 된 경우 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="8f69d-134">이는 동시 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="8f69d-135">*덮어쓰기* 매개 변수를 사용 하 여이 동작을 억제할 수 있으며,이 동작은 동시 변경에 관계 없이 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="8f69d-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8f69d-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="8f69d-137">이 DNS 영역에 가상 컴퓨터 호스트 이름 레코드를 등록할 가상 네트워크 목록으로, 개인 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="8f69d-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="8f69d-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="8f69d-139">이 DNS 영역에 가상 컴퓨터 호스트 이름 레코드를 등록할 가상 네트워크 Id 목록으로, 개인 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="8f69d-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8f69d-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="8f69d-141">이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 목록으로, 개인 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="8f69d-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="8f69d-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="8f69d-143">이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 Id의 목록이 며, 개인 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="8f69d-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f69d-144">-ResourceGroupName</span></span>
<span data-ttu-id="8f69d-145">업데이트할 영역이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="8f69d-146">ZoneName 매개 변수도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-146">You must also specify the ZoneName parameter.</span></span>
<span data-ttu-id="8f69d-147">또는 *zone* 매개 변수 또는 파이프라인을 통해 DnsZone 개체를 사용 하 여 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

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

### <span data-ttu-id="8f69d-148">태그</span><span class="sxs-lookup"><span data-stu-id="8f69d-148">-Tag</span></span>
<span data-ttu-id="8f69d-149">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8f69d-150">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8f69d-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8f69d-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="8f69d-151">-Zone</span></span>
<span data-ttu-id="8f69d-152">업데이트할 DNS 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-152">Specifies the DNS zone to update.</span></span>
<span data-ttu-id="8f69d-153">또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-153">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="8f69d-154">-확인</span><span class="sxs-lookup"><span data-stu-id="8f69d-154">-Confirm</span></span>
<span data-ttu-id="8f69d-155">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f69d-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f69d-156">-WhatIf</span></span>
<span data-ttu-id="8f69d-157">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f69d-158">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-158">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f69d-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f69d-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f69d-160">CommonParameters</span></span>
<span data-ttu-id="8f69d-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f69d-162">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f69d-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f69d-163">입력</span><span class="sxs-lookup"><span data-stu-id="8f69d-163">INPUTS</span></span>

### <span data-ttu-id="8f69d-164">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8f69d-164">System.String</span></span>

### <span data-ttu-id="8f69d-165">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="8f69d-165">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8f69d-166">System.webserver. List ' 1 [[System.webserver], CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8f69d-166">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8f69d-167">System.webserver. List ' 1 [[IResourceReference, Microsoft azure. 31bf3856ad364e35. 클라이언트. 네트워크, 버전 = 1.0.0.0, Culture = 중립, PublicKeyToken =]])</span><span class="sxs-lookup"><span data-stu-id="8f69d-167">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="8f69d-168">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="8f69d-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="8f69d-169">출력</span><span class="sxs-lookup"><span data-stu-id="8f69d-169">OUTPUTS</span></span>

### <span data-ttu-id="8f69d-170">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="8f69d-170">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="8f69d-171">상속자</span><span class="sxs-lookup"><span data-stu-id="8f69d-171">NOTES</span></span>
<span data-ttu-id="8f69d-172">*확인* 매개 변수를 사용 하 여이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-172">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="8f69d-173">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 변수의 값이 중간 인지 아래 인지 여부를 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-173">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="8f69d-174">*확인* 또는 *확인: $True* 를 지정 하는 경우이 cmdlet을 실행 하기 전에 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-174">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="8f69d-175">*확인: $False* 를 지정 하면 cmdlet에서 확인을 요구 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f69d-175">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8f69d-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f69d-176">RELATED LINKS</span></span>

[<span data-ttu-id="8f69d-177">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8f69d-177">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="8f69d-178">새로운 AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8f69d-178">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="8f69d-179">제거-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="8f69d-179">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

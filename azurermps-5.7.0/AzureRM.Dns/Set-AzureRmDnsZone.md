---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/set-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Set-AzureRmDnsZone.md
ms.openlocfilehash: da504f6b8110335e6297d0c7efb2a1a27106e0e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526828"
---
# <span data-ttu-id="c2f92-101">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="c2f92-101">Set-AzureRmDnsZone</span></span>

## <span data-ttu-id="c2f92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2f92-102">SYNOPSIS</span></span>
<span data-ttu-id="c2f92-103">DNS 영역의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-103">Updates the properties of a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2f92-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2f92-104">SYNTAX</span></span>

### <span data-ttu-id="c2f92-105">필드 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c2f92-105">Fields (Default)</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f92-106">Fieldobjects</span><span class="sxs-lookup"><span data-stu-id="c2f92-106">FieldsObjects</span></span>
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2f92-107">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="c2f92-107">Object</span></span>
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2f92-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c2f92-108">DESCRIPTION</span></span>
<span data-ttu-id="c2f92-109">**AzureRmDnsZone** Cmdlet은 Azure DNS 서비스에서 지정 된 DNS 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-109">The **Set-AzureRmDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="c2f92-110">이 cmdlet은 영역의 레코드 집합을 업데이트 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-110">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="c2f92-111">**DnsZone** 개체를 매개 변수 또는 파이프라인 연산자를 사용 하 여 전달 하거나 *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-111">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="c2f92-112">*확인* 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="c2f92-113">영역 개체를 사용 하거나 파이프라인을 통해 DNS 영역을 개체로 전달 하는 경우 로컬 DnsZone 개체가 검색 된 후 Azure DNS에서 변경 된 경우 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-113">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="c2f92-114">이는 동시 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-114">This provides protection for concurrent changes.</span></span> <span data-ttu-id="c2f92-115">*덮어쓰기* 매개 변수를 사용 하 여이 동작을 억제할 수 있으며,이 동작은 동시 변경에 관계 없이 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-115">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="c2f92-116">예제의</span><span class="sxs-lookup"><span data-stu-id="c2f92-116">EXAMPLES</span></span>

### <span data-ttu-id="c2f92-117">예제 1: DNS 영역 업데이트</span><span class="sxs-lookup"><span data-stu-id="c2f92-117">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

<span data-ttu-id="c2f92-118">첫 번째 명령은 지정 된 리소스 그룹에서 myzone.com 이라는 영역을 가져온 다음이를 $Zone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-118">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="c2f92-119">두 번째 명령은 $Zone에 대 한 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-119">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="c2f92-120">마지막 명령은 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-120">The final command commits the change.</span></span>

### <span data-ttu-id="c2f92-121">예제 2: 영역의 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="c2f92-121">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="c2f92-122">이 명령은 먼저 영역을 명시적으로 가져오지 않고 myzone.com 이라는 영역에 대 한 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-122">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

### <span data-ttu-id="c2f92-123">예제 3: ID를 지정 하 여 개인 영역을 가상 네트워크와 연결</span><span class="sxs-lookup"><span data-stu-id="c2f92-123">Example 3: Associating a private zone with a virtual network by specifying its ID</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetworkId @($vnet.Id)
```

<span data-ttu-id="c2f92-124">이 명령은 ID를 지정 하 여 개인 DNS 영역 myprivatezone.com을 가상 네트워크 myvnet과 함께 등록 네트워크로 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-124">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by specifying its ID.</span></span>

### <span data-ttu-id="c2f92-125">예제 4: 네트워크 개체를 지정 하 여 개인 영역을 가상 네트워크와 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-125">Example 4: Associating a private zone with a virtual network by specifying the network object.</span></span>
```
PS C:\>$vnet = Get-AzureRmVirualNetwork -ResourceGroupName "MyResourceGroup" -Name "myvnet"
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myprivatezone.com" -RegistrationVirtualNetwork @($vnet)
```

<span data-ttu-id="c2f92-126">이 명령은 $vnet 변수로 표시 되는 가상 네트워크 개체를 Set-AzureRmDnsZone cmdlet으로 전달 하 여 가상 네트워크 myvnet과 myprivatezone.com의 사설 DNS 영역을 등록 네트워크로 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-126">This command associates the Private DNS zone myprivatezone.com with the virtual network myvnet as a registration network by passing the virtual network object represented by $vnet variable to the Set-AzureRmDnsZone cmdlet.</span></span>

## <span data-ttu-id="c2f92-127">변수</span><span class="sxs-lookup"><span data-stu-id="c2f92-127">PARAMETERS</span></span>

### <span data-ttu-id="c2f92-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2f92-128">-DefaultProfile</span></span>
<span data-ttu-id="c2f92-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c2f92-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f92-130">-이름</span><span class="sxs-lookup"><span data-stu-id="c2f92-130">-Name</span></span>
<span data-ttu-id="c2f92-131">업데이트할 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-131">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2f92-132">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="c2f92-132">-Overwrite</span></span>
<span data-ttu-id="c2f92-133">영역 개체를 사용 하거나 파이프라인을 통해 DNS 영역을 개체로 전달 하는 경우 로컬 DnsZone 개체가 검색 된 후 Azure DNS에서 변경 된 경우 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-133">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="c2f92-134">이는 동시 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-134">This provides protection for concurrent changes.</span></span> <span data-ttu-id="c2f92-135">*덮어쓰기* 매개 변수를 사용 하 여이 동작을 억제할 수 있으며,이 동작은 동시 변경에 관계 없이 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-135">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f92-136">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c2f92-136">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="c2f92-137">이 DNS 영역에 가상 컴퓨터 호스트 이름 레코드를 등록할 가상 네트워크 목록으로, 개인 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-137">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="c2f92-138">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="c2f92-138">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="c2f92-139">이 DNS 영역에 가상 컴퓨터 호스트 이름 레코드를 등록할 가상 네트워크 Id 목록으로, 개인 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-139">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="c2f92-140">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c2f92-140">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="c2f92-141">이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 목록으로, 개인 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-141">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="c2f92-142">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="c2f92-142">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="c2f92-143">이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 Id의 목록이 며, 개인 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-143">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="c2f92-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2f92-144">-ResourceGroupName</span></span>
<span data-ttu-id="c2f92-145">업데이트할 영역이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-145">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="c2f92-146">ZoneName 매개 변수도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-146">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="c2f92-147">또는 *zone* 매개 변수 또는 파이프라인을 통해 DnsZone 개체를 사용 하 여 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-147">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: Fields, FieldsObjects
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2f92-148">태그</span><span class="sxs-lookup"><span data-stu-id="c2f92-148">-Tag</span></span>
<span data-ttu-id="c2f92-149">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c2f92-150">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="c2f92-150">For example:</span></span>

<span data-ttu-id="c2f92-151">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c2f92-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Fields, FieldsObjects
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2f92-152">-Zone</span><span class="sxs-lookup"><span data-stu-id="c2f92-152">-Zone</span></span>
<span data-ttu-id="c2f92-153">업데이트할 DNS 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-153">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="c2f92-154">또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-154">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2f92-155">-확인</span><span class="sxs-lookup"><span data-stu-id="c2f92-155">-Confirm</span></span>
<span data-ttu-id="c2f92-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f92-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2f92-157">-WhatIf</span></span>
<span data-ttu-id="c2f92-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2f92-159">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-159">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2f92-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f92-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2f92-161">CommonParameters</span></span>
<span data-ttu-id="c2f92-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2f92-163">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2f92-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2f92-164">입력</span><span class="sxs-lookup"><span data-stu-id="c2f92-164">INPUTS</span></span>

### <span data-ttu-id="c2f92-165">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="c2f92-165">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="c2f92-166">DnsZone 개체를이 cmdlet에 파이프 하 여 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-166">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="c2f92-167">출력</span><span class="sxs-lookup"><span data-stu-id="c2f92-167">OUTPUTS</span></span>

### <span data-ttu-id="c2f92-168">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="c2f92-168">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="c2f92-169">이 cmdlet은 새 Etag를 사용 하 여 업데이트 된 DNS 영역을 나타내는 DnsZone 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-169">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="c2f92-170">상속자</span><span class="sxs-lookup"><span data-stu-id="c2f92-170">NOTES</span></span>
<span data-ttu-id="c2f92-171">*확인* 매개 변수를 사용 하 여이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-171">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="c2f92-172">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 변수의 값이 중간 인지 아래 인지 여부를 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-172">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="c2f92-173">*확인* 또는 *확인: $True* 를 지정 하는 경우이 cmdlet을 실행 하기 전에 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-173">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="c2f92-174">*확인: $False* 를 지정 하면 cmdlet에서 확인을 요구 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2f92-174">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c2f92-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2f92-175">RELATED LINKS</span></span>

[<span data-ttu-id="c2f92-176">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="c2f92-176">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="c2f92-177">새로운 AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="c2f92-177">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="c2f92-178">제거-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="c2f92-178">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

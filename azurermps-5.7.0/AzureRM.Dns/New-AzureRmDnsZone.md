---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: 28fabce7590644c230643822c206515957839127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702647"
---
# <span data-ttu-id="e01b4-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e01b4-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="e01b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e01b4-102">SYNOPSIS</span></span>
<span data-ttu-id="e01b4-103">새 DNS 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e01b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e01b4-104">SYNTAX</span></span>

### <span data-ttu-id="e01b4-105">Id (기본값)</span><span class="sxs-lookup"><span data-stu-id="e01b4-105">Ids (Default)</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e01b4-106">나타내는</span><span class="sxs-lookup"><span data-stu-id="e01b4-106">Objects</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e01b4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e01b4-107">DESCRIPTION</span></span>
<span data-ttu-id="e01b4-108">**AzureRmDnsZone** cmdlet은 지정 된 리소스 그룹에 새 DNS (Domain Name System) 영역을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-108">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="e01b4-109">*Name* 매개 변수에 대해 고유한 DNS 영역 이름을 지정 해야 하며, cmdlet이 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-109">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="e01b4-110">영역이 만들어지면 New-AzureRmDnsRecordSet cmdlet을 사용 하 여 영역에서 레코드 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-110">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="e01b4-111">*확인* 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="e01b4-112">예제의</span><span class="sxs-lookup"><span data-stu-id="e01b4-112">EXAMPLES</span></span>

### <span data-ttu-id="e01b4-113">예제 1: DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="e01b4-113">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="e01b4-114">이 명령은 지정 된 리소스 그룹에 myzone.com 이라는 새 DNS 영역을 만든 다음이를 $Zone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-114">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="e01b4-115">예제 2: 가상 네트워크 Id를 지정 하 여 개인 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="e01b4-115">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="e01b4-116">이 명령은 지정 된 리소스 그룹에서 myprivatezone.com 이라는 새 개인 DNS 영역을 만들고 해당 ID를 지정 하 여 관련 된 해결 가상 네트워크를 만든 다음이를 $Zone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-116">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="e01b4-117">예제 3: 가상 네트워크 개체를 지정 하 여 개인 DNS 영역 만들기</span><span class="sxs-lookup"><span data-stu-id="e01b4-117">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzureRmVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="e01b4-118">이 명령은 연결 된 해결 가상 네트워크 ($ResVirtualNetwork 변수)를 사용 하 여 지정 된 리소스 그룹에 myprivatezone.com 이라는 새 개인 DNS 영역을 만든 다음 $Zone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-118">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="e01b4-119">변수</span><span class="sxs-lookup"><span data-stu-id="e01b4-119">PARAMETERS</span></span>

### <span data-ttu-id="e01b4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e01b4-120">-DefaultProfile</span></span>
<span data-ttu-id="e01b4-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e01b4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e01b4-122">-이름</span><span class="sxs-lookup"><span data-stu-id="e01b4-122">-Name</span></span>
<span data-ttu-id="e01b4-123">만들려는 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-123">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e01b4-124">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e01b4-124">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="e01b4-125">이 DNS 영역에 가상 컴퓨터 호스트 이름 레코드를 등록할 가상 네트워크 목록으로, 개인 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-125">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="e01b4-126">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e01b4-126">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="e01b4-127">이 DNS 영역에 가상 컴퓨터 호스트 이름 레코드를 등록할 가상 네트워크 Id 목록으로, 개인 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-127">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="e01b4-128">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e01b4-128">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="e01b4-129">이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 목록으로, 개인 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-129">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="e01b4-130">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="e01b4-130">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="e01b4-131">이 DNS 영역의 레코드를 확인할 수 있는 가상 네트워크 Id의 목록이 며, 개인 영역에만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-131">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

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

### <span data-ttu-id="e01b4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e01b4-132">-ResourceGroupName</span></span>
<span data-ttu-id="e01b4-133">영역을 만들 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-133">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e01b4-134">태그</span><span class="sxs-lookup"><span data-stu-id="e01b4-134">-Tag</span></span>
<span data-ttu-id="e01b4-135">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e01b4-136">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="e01b4-136">For example:</span></span>

<span data-ttu-id="e01b4-137">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e01b4-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e01b4-138">-ZoneType</span><span class="sxs-lookup"><span data-stu-id="e01b4-138">-ZoneType</span></span>
<span data-ttu-id="e01b4-139">영역의 형식 (공개 또는 비공개)입니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-139">The type of the zone, Public or Private.</span></span> <span data-ttu-id="e01b4-140">형식이 나 공개 형식이 없는 영역은 DNS 계층에서 사용할 공용 DNS 처리 평면에서 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-140">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="e01b4-141">비공개 유형의 영역은 연결 된 가상 네트워크 집합 (이 기능은 미리 보기) 에서만 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-141">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="e01b4-142">이 속성은 영역에 대해 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-142">This property cannot be changed for a zone.</span></span>

```yaml
Type: ZoneType
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e01b4-143">-확인</span><span class="sxs-lookup"><span data-stu-id="e01b4-143">-Confirm</span></span>
<span data-ttu-id="e01b4-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e01b4-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e01b4-145">-WhatIf</span></span>
<span data-ttu-id="e01b4-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e01b4-147">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-147">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e01b4-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e01b4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e01b4-149">CommonParameters</span></span>
<span data-ttu-id="e01b4-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e01b4-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e01b4-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e01b4-152">입력</span><span class="sxs-lookup"><span data-stu-id="e01b4-152">INPUTS</span></span>

### <span data-ttu-id="e01b4-153">않아야</span><span class="sxs-lookup"><span data-stu-id="e01b4-153">None</span></span>
<span data-ttu-id="e01b4-154">이 cmdlet에는 입력을 파이프가 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-154">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="e01b4-155">출력</span><span class="sxs-lookup"><span data-stu-id="e01b4-155">OUTPUTS</span></span>

### <span data-ttu-id="e01b4-156">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="e01b4-156">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="e01b4-157">이 cmdlet은 새 DNS 영역을 나타내는 DnsZone 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-157">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="e01b4-158">상속자</span><span class="sxs-lookup"><span data-stu-id="e01b4-158">NOTES</span></span>
<span data-ttu-id="e01b4-159">*확인* 매개 변수를 사용 하 여이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-159">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="e01b4-160">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 변수의 값이 중간 인지 아래 인지 여부를 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-160">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="e01b4-161">*확인* 또는 *확인: $True* 를 지정 하는 경우이 cmdlet을 실행 하기 전에 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-161">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="e01b4-162">*확인: $False* 를 지정 하면 cmdlet에서 확인을 요구 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e01b4-162">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e01b4-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e01b4-163">RELATED LINKS</span></span>

[<span data-ttu-id="e01b4-164">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e01b4-164">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="e01b4-165">새로운 AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="e01b4-165">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="e01b4-166">제거-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="e01b4-166">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

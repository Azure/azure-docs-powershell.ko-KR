---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Set-AzDnsZone.md
ms.openlocfilehash: 9b6d84f9007a872db0e41efa78d8e16d7269eb02
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875951"
---
# <span data-ttu-id="b8093-101">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b8093-101">Set-AzDnsZone</span></span>

## <span data-ttu-id="b8093-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8093-102">SYNOPSIS</span></span>
<span data-ttu-id="b8093-103">DNS 영역의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-103">Updates the properties of a DNS zone.</span></span>

## <span data-ttu-id="b8093-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8093-104">SYNTAX</span></span>

### <span data-ttu-id="b8093-105">필드인</span><span class="sxs-lookup"><span data-stu-id="b8093-105">Fields</span></span>
```
Set-AzDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8093-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="b8093-106">Object</span></span>
```
Set-AzDnsZone -Zone <DnsZone> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8093-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b8093-107">DESCRIPTION</span></span>
<span data-ttu-id="b8093-108">**AzDnsZone** Cmdlet은 Azure DNS 서비스에서 지정 된 DNS 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-108">The **Set-AzDnsZone** cmdlet updates the specified DNS zone in the Azure DNS service.</span></span>
<span data-ttu-id="b8093-109">이 cmdlet은 영역의 레코드 집합을 업데이트 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-109">This cmdlet does not update the record sets in the zone.</span></span>

<span data-ttu-id="b8093-110">**DnsZone** 개체를 매개 변수 또는 파이프라인 연산자를 사용 하 여 전달 하거나 *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-110">You can pass a **DnsZone** object as a parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="b8093-111">*확인* 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="b8093-112">영역 개체를 사용 하거나 파이프라인을 통해 DNS 영역을 개체로 전달 하는 경우 로컬 DnsZone 개체가 검색 된 후 Azure DNS에서 변경 된 경우 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-112">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="b8093-113">이는 동시 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-113">This provides protection for concurrent changes.</span></span> <span data-ttu-id="b8093-114">*덮어쓰기* 매개 변수를 사용 하 여이 동작을 억제할 수 있으며,이 동작은 동시 변경에 관계 없이 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-114">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="b8093-115">예제의</span><span class="sxs-lookup"><span data-stu-id="b8093-115">EXAMPLES</span></span>

### <span data-ttu-id="b8093-116">예제 1: DNS 영역 업데이트</span><span class="sxs-lookup"><span data-stu-id="b8093-116">Example 1: Update a DNS zone</span></span>
```
PS C:\>$Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzDnsZone -Zone $Zone
```

<span data-ttu-id="b8093-117">첫 번째 명령은 지정 된 리소스 그룹에서 myzone.com 이라는 영역을 가져온 다음이를 $Zone 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-117">The first command gets the zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

<span data-ttu-id="b8093-118">두 번째 명령은 $Zone에 대 한 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-118">The second command updates the tags for $Zone.</span></span>

<span data-ttu-id="b8093-119">마지막 명령은 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-119">The final command commits the change.</span></span>

### <span data-ttu-id="b8093-120">예제 2: 영역의 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="b8093-120">Example 2: Update tags for a zone</span></span>
```
PS C:\>Set-AzDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

<span data-ttu-id="b8093-121">이 명령은 먼저 영역을 명시적으로 가져오지 않고 myzone.com 이라는 영역에 대 한 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-121">This command updates the tags for the zone named myzone.com without first explicitly getting the zone.</span></span>

## <span data-ttu-id="b8093-122">변수</span><span class="sxs-lookup"><span data-stu-id="b8093-122">PARAMETERS</span></span>

### <span data-ttu-id="b8093-123">-이름</span><span class="sxs-lookup"><span data-stu-id="b8093-123">-Name</span></span>
<span data-ttu-id="b8093-124">업데이트할 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-124">Specifies the name of the DNS zone to update.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8093-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="b8093-125">-Overwrite</span></span>
<span data-ttu-id="b8093-126">영역 개체를 사용 하거나 파이프라인을 통해 DNS 영역을 개체로 전달 하는 경우 로컬 DnsZone 개체가 검색 된 후 Azure DNS에서 변경 된 경우 업데이트 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-126">When passing a DNS zone as an object (using the Zone object or via the pipeline), it is not updated if it has been changed in Azure DNS since the local DnsZone object was retrieved.</span></span> <span data-ttu-id="b8093-127">이는 동시 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-127">This provides protection for concurrent changes.</span></span> <span data-ttu-id="b8093-128">*덮어쓰기* 매개 변수를 사용 하 여이 동작을 억제할 수 있으며,이 동작은 동시 변경에 관계 없이 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-128">You can suppress this behavior with the *Overwrite* parameter, which updates the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="b8093-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8093-129">-ResourceGroupName</span></span>
<span data-ttu-id="b8093-130">업데이트할 영역이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-130">Specifies the name of the resource group that contains the zone to update.</span></span>
<span data-ttu-id="b8093-131">ZoneName 매개 변수도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-131">You must also specify the ZoneName parameter.</span></span>

<span data-ttu-id="b8093-132">또는 *zone* 매개 변수 또는 파이프라인을 통해 DnsZone 개체를 사용 하 여 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-132">Alternatively, you can specify the zone using a DnsZone object with the *Zone* parameter or the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8093-133">태그</span><span class="sxs-lookup"><span data-stu-id="b8093-133">-Tag</span></span>
<span data-ttu-id="b8093-134">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b8093-135">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="b8093-135">For example:</span></span>

<span data-ttu-id="b8093-136">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b8093-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8093-137">-Zone</span><span class="sxs-lookup"><span data-stu-id="b8093-137">-Zone</span></span>
<span data-ttu-id="b8093-138">업데이트할 DNS 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-138">Specifies the DNS zone to update.</span></span>

<span data-ttu-id="b8093-139">또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-139">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="b8093-140">-확인</span><span class="sxs-lookup"><span data-stu-id="b8093-140">-Confirm</span></span>
<span data-ttu-id="b8093-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8093-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8093-142">-WhatIf</span></span>
<span data-ttu-id="b8093-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8093-144">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8093-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8093-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8093-146">CommonParameters</span></span>
<span data-ttu-id="b8093-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8093-148">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8093-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8093-149">입력</span><span class="sxs-lookup"><span data-stu-id="b8093-149">INPUTS</span></span>

### <span data-ttu-id="b8093-150">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="b8093-150">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="b8093-151">DnsZone 개체를이 cmdlet에 파이프 하 여 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-151">You can pipe a DnsZone object to this cmdlet.</span></span>

## <span data-ttu-id="b8093-152">출력</span><span class="sxs-lookup"><span data-stu-id="b8093-152">OUTPUTS</span></span>

### <span data-ttu-id="b8093-153">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="b8093-153">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="b8093-154">이 cmdlet은 새 Etag를 사용 하 여 업데이트 된 DNS 영역을 나타내는 DnsZone 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-154">This cmdlet returns a DnsZone object that represents the updated DNS zone with a new Etag.</span></span>

## <span data-ttu-id="b8093-155">상속자</span><span class="sxs-lookup"><span data-stu-id="b8093-155">NOTES</span></span>
<span data-ttu-id="b8093-156">*확인* 매개 변수를 사용 하 여이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-156">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="b8093-157">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 변수의 값이 중간 인지 아래 인지 여부를 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-157">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="b8093-158">*확인* 또는 *확인: $True* 를 지정 하는 경우이 cmdlet을 실행 하기 전에 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-158">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="b8093-159">*확인: $False* 를 지정 하면 cmdlet에서 확인을 요구 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8093-159">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b8093-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8093-160">RELATED LINKS</span></span>

[<span data-ttu-id="b8093-161">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b8093-161">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="b8093-162">새로운 AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b8093-162">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="b8093-163">제거-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="b8093-163">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)
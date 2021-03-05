---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 447b1e32473d00504446478a9efaa5634e3b1c65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984830"
---
# <span data-ttu-id="f3bdf-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f3bdf-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="f3bdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="f3bdf-103">DNS 레코드 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="f3bdf-104">구문</span><span class="sxs-lookup"><span data-stu-id="f3bdf-104">SYNTAX</span></span>

### <span data-ttu-id="f3bdf-105">필드</span><span class="sxs-lookup"><span data-stu-id="f3bdf-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3bdf-106">개체</span><span class="sxs-lookup"><span data-stu-id="f3bdf-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3bdf-107">설명</span><span class="sxs-lookup"><span data-stu-id="f3bdf-107">DESCRIPTION</span></span>
<span data-ttu-id="f3bdf-108">**Get-AzDnsRecordSet** cmdlet은 지정된 이름과 형식이 지정된 영역의 DNS(도메인 이름 시스템) 레코드 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="f3bdf-109">Name 또는 *RecordType* 매개 변수를 지정하지 않으면 이 cmdlet은 영역의 지정된 형식의 모든 레코드 집합을 반환합니다. </span><span class="sxs-lookup"><span data-stu-id="f3bdf-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="f3bdf-110">*RecordType* 매개 변수를 지정하지만 *이름* 매개 변수가 아닌 경우 이 cmdlet은 지정된 레코드 형식의 모든 레코드 집합을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="f3bdf-111">파이프라인 연산자를 사용하여 **DnsZone** 개체를 이 cmdlet에 전달하거나 **DnsZone** 개체를 영역  매개 변수로 전달하거나 또는 이름으로 영역 및 리소스 그룹을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="f3bdf-112">예제</span><span class="sxs-lookup"><span data-stu-id="f3bdf-112">EXAMPLES</span></span>

### <span data-ttu-id="f3bdf-113">예제 1: 지정된 이름 및 형식이 있는 레코드 집합을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="f3bdf-114">이 명령은 지정된 리소스 그룹 및 영역의 www라는 레코드 형식 A의 레코드 집합을 얻은 다음, $RecordSet 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="f3bdf-115">Name *및* *RecordType* 매개 변수가 지정되어 있기 때문에 **RecordSet** 개체 하나만 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="f3bdf-116">예제 2: 지정된 형식의 레코드 집합을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="f3bdf-117">이 명령은 MyResourceGroup이라는 리소스 그룹에 있는 myzone.com 영역의 레코드 형식 A의 모든 레코드 집합의 배열을 $RecordSets 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="f3bdf-118">예제 3: 영역의 모든 레코드 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="f3bdf-119">이 명령은 MyResourceGroup이라는 리소스 그룹에 있는 myzone.com 영역의 모든 레코드 집합의 배열을 구한 다음, 해당 레코드 집합을 $RecordSets 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="f3bdf-120">예제 4: DnsZone 개체를 사용하여 영역의 모든 레코드 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="f3bdf-121">이 예제는 위의 예제 3과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="f3bdf-122">이번에는 영역 개체를 사용하여 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="f3bdf-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f3bdf-123">PARAMETERS</span></span>

### <span data-ttu-id="f3bdf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3bdf-124">-DefaultProfile</span></span>
<span data-ttu-id="f3bdf-125">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f3bdf-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3bdf-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f3bdf-126">-Name</span></span>
<span data-ttu-id="f3bdf-127">얻을 **RecordSet의 이름을** 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="f3bdf-128">이름 매개 변수를  지정하지 않으면 지정된 형식의 모든 레코드 집합이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3bdf-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="f3bdf-129">-RecordType</span></span>
<span data-ttu-id="f3bdf-130">이 cmdlet에서 얻을 DNS 레코드 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="f3bdf-131">유효한 값은:</span><span class="sxs-lookup"><span data-stu-id="f3bdf-131">Valid values are:</span></span> 
- <span data-ttu-id="f3bdf-132">A</span><span class="sxs-lookup"><span data-stu-id="f3bdf-132">A</span></span>
- <span data-ttu-id="f3bdf-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="f3bdf-133">AAAA</span></span>
- <span data-ttu-id="f3bdf-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="f3bdf-134">CNAME</span></span>
- <span data-ttu-id="f3bdf-135">MX</span><span class="sxs-lookup"><span data-stu-id="f3bdf-135">MX</span></span>
- <span data-ttu-id="f3bdf-136">NS</span><span class="sxs-lookup"><span data-stu-id="f3bdf-136">NS</span></span>
- <span data-ttu-id="f3bdf-137">PTR</span><span class="sxs-lookup"><span data-stu-id="f3bdf-137">PTR</span></span>
- <span data-ttu-id="f3bdf-138">SOA</span><span class="sxs-lookup"><span data-stu-id="f3bdf-138">SOA</span></span>
- <span data-ttu-id="f3bdf-139">SRV</span><span class="sxs-lookup"><span data-stu-id="f3bdf-139">SRV</span></span>
- <span data-ttu-id="f3bdf-140">TXT *RecordType* 매개 변수를 지정하지 않으면 이름 매개 변수도 *생략해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="f3bdf-141">그런 다음 이 cmdlet은 영역의 모든 레코드 집합(모든 이름 및 형식)을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3bdf-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3bdf-142">-ResourceGroupName</span></span>
<span data-ttu-id="f3bdf-143">DNS 영역이 포함된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="f3bdf-144">ZoneName 매개 변수를 사용하여 영역 이름을 *지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="f3bdf-145">또는 영역 매개 변수를 사용하여 **DnsZone** 개체에 전달하여 영역 및 리소스 그룹을 *지정할 수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3bdf-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="f3bdf-146">-Zone</span></span>
<span data-ttu-id="f3bdf-147">이 cmdlet이 얻을 레코드 집합을 포함하는 DNS 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="f3bdf-148">또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용하여 지역을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="f3bdf-149">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="f3bdf-149">-ZoneName</span></span>
<span data-ttu-id="f3bdf-150">얻을 레코드 집합이 포함된 DNS 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="f3bdf-151">*ResourceGroupName* 매개 변수를 사용하여 영역이 포함된 리소스 그룹도 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="f3bdf-152">또는 영역 매개 변수를 사용하여 DNS 영역 개체에 전달하여 영역 및 리소스 그룹을 *지정할 수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3bdf-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3bdf-153">CommonParameters</span></span>
<span data-ttu-id="f3bdf-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3bdf-155">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f3bdf-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3bdf-156">입력</span><span class="sxs-lookup"><span data-stu-id="f3bdf-156">INPUTS</span></span>

### <span data-ttu-id="f3bdf-157">System.String</span><span class="sxs-lookup"><span data-stu-id="f3bdf-157">System.String</span></span>

### <span data-ttu-id="f3bdf-158">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="f3bdf-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="f3bdf-159">System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f3bdf-159">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="f3bdf-160">출력</span><span class="sxs-lookup"><span data-stu-id="f3bdf-160">OUTPUTS</span></span>

### <span data-ttu-id="f3bdf-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f3bdf-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="f3bdf-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f3bdf-162">NOTES</span></span>

## <span data-ttu-id="f3bdf-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3bdf-163">RELATED LINKS</span></span>

[<span data-ttu-id="f3bdf-164">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f3bdf-164">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="f3bdf-165">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f3bdf-165">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="f3bdf-166">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f3bdf-166">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)



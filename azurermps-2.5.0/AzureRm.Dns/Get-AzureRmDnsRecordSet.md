---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4027b13fb398d69bee09be5c0a939ff86a099e39
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882258"
---
# <span data-ttu-id="c3e9a-101">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3e9a-101">Get-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="c3e9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e9a-103">DNS 레코드 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-103">Gets a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3e9a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c3e9a-104">SYNTAX</span></span>

### <span data-ttu-id="c3e9a-105">필드인</span><span class="sxs-lookup"><span data-stu-id="c3e9a-105">Fields</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [<CommonParameters>]
```

### <span data-ttu-id="c3e9a-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="c3e9a-106">Object</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>] [<CommonParameters>]
```

## <span data-ttu-id="c3e9a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c3e9a-107">DESCRIPTION</span></span>
<span data-ttu-id="c3e9a-108">**AzureRmDnsRecordSet** cmdlet은 지정 된 영역에서 지정 된 이름 및 형식으로 DNS (Domain Name System) 레코드 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-108">The **Get-AzureRmDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>

<span data-ttu-id="c3e9a-109">*Name* 또는 *RecordType* 매개 변수를 지정 하지 않으면이 cmdlet은 영역에 지정 된 형식의 모든 레코드 집합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="c3e9a-110">*Name* 매개 변수를 제외한 *RecordType* 매개 변수를 지정 하면이 cmdlet은 지정 된 레코드 형식의 모든 레코드 집합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>

<span data-ttu-id="c3e9a-111">파이프라인 연산자를 사용 하 여 **DnsZone** 개체를이 cmdlet에 전달 하거나, **DnsZone** 개체를 *zone* 매개 변수로 전달 하거나, 이름을 기준으로 영역과 리소스 그룹을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="c3e9a-112">예제의</span><span class="sxs-lookup"><span data-stu-id="c3e9a-112">EXAMPLES</span></span>

### <span data-ttu-id="c3e9a-113">예제 1: 지정 된 이름 및 형식으로 레코드 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3e9a-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="c3e9a-114">이 명령은 지정 된 리소스 그룹 및 영역에서 www 라는 레코드 종류의 레코드 집합을 가져온 다음이를 $RecordSet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="c3e9a-115">*Name* 및 *RecordType* 매개 변수는 지정 되어 있으므로 하나의 **레코드 집합** 개체만 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="c3e9a-116">예제 2: 지정 된 형식의 레코드 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3e9a-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="c3e9a-117">이 명령은 MyResourceGroup 이라는 리소스 그룹에 있는 myzone.com 이라는 영역에 있는 레코드 종류 A의 모든 레코드 집합의 배열을 가져온 다음이를 $RecordSets 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="c3e9a-118">예제 3: 영역의 모든 레코드 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3e9a-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="c3e9a-119">이 명령은 MyResourceGroup 이라는 리소스 그룹의 myzone.com 이라는 영역에 있는 모든 레코드 집합의 배열을 가져온 다음이를 $RecordSets 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="c3e9a-120">예제 4: DnsZone 개체를 사용 하 여 영역의 모든 레코드 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="c3e9a-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

<span data-ttu-id="c3e9a-121">이 예제는 위의 예제 3과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="c3e9a-122">이번에는 zone 개체를 사용 하 여 영역이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="c3e9a-123">변수</span><span class="sxs-lookup"><span data-stu-id="c3e9a-123">PARAMETERS</span></span>

### <span data-ttu-id="c3e9a-124">-이름</span><span class="sxs-lookup"><span data-stu-id="c3e9a-124">-Name</span></span>
<span data-ttu-id="c3e9a-125">가져올 **레코드 집합** 의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-125">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="c3e9a-126">*Name* 매개 변수를 지정 하지 않으면 지정 된 형식의 모든 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-126">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e9a-127">-RecordType</span><span class="sxs-lookup"><span data-stu-id="c3e9a-127">-RecordType</span></span>
<span data-ttu-id="c3e9a-128">이 cmdlet이 가져오는 DNS 레코드의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-128">Specifies the type of DNS record that this cmdlet gets.</span></span>

<span data-ttu-id="c3e9a-129">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-129">Valid values are:</span></span> 

- <span data-ttu-id="c3e9a-130">에서</span><span class="sxs-lookup"><span data-stu-id="c3e9a-130">A</span></span>
- <span data-ttu-id="c3e9a-131">AAAA</span><span class="sxs-lookup"><span data-stu-id="c3e9a-131">AAAA</span></span>
- <span data-ttu-id="c3e9a-132">CNAME</span><span class="sxs-lookup"><span data-stu-id="c3e9a-132">CNAME</span></span>
- <span data-ttu-id="c3e9a-133">멕시코</span><span class="sxs-lookup"><span data-stu-id="c3e9a-133">MX</span></span>
- <span data-ttu-id="c3e9a-134">NS</span><span class="sxs-lookup"><span data-stu-id="c3e9a-134">NS</span></span>
- <span data-ttu-id="c3e9a-135">PTR 레코드로</span><span class="sxs-lookup"><span data-stu-id="c3e9a-135">PTR</span></span>
- <span data-ttu-id="c3e9a-136">SOA</span><span class="sxs-lookup"><span data-stu-id="c3e9a-136">SOA</span></span>
- <span data-ttu-id="c3e9a-137">SRV</span><span class="sxs-lookup"><span data-stu-id="c3e9a-137">SRV</span></span>
- <span data-ttu-id="c3e9a-138">라는</span><span class="sxs-lookup"><span data-stu-id="c3e9a-138">TXT</span></span>

<span data-ttu-id="c3e9a-139">*RecordType* 매개 변수를 지정 하지 않으면 *Name* 매개 변수도 생략 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-139">If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="c3e9a-140">그런 다음이 cmdlet은 모든 이름과 형식의 영역에 있는 모든 레코드 집합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-140">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e9a-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e9a-141">-ResourceGroupName</span></span>
<span data-ttu-id="c3e9a-142">DNS 영역이 포함 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-142">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="c3e9a-143">*ZoneName* 매개 변수를 사용 하 여 영역 이름도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-143">The zone name must also be specified, using the *ZoneName* parameter.</span></span>

<span data-ttu-id="c3e9a-144">또는 *zone* 매개 변수를 사용 하 여 **DnsZone** 개체를 전달 하 여 영역 및 리소스 그룹을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-144">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="c3e9a-145">-Zone</span><span class="sxs-lookup"><span data-stu-id="c3e9a-145">-Zone</span></span>
<span data-ttu-id="c3e9a-146">이 cmdlet이 가져오는 레코드 집합을 포함 하는 DNS 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-146">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="c3e9a-147">또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-147">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="c3e9a-148">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="c3e9a-148">-ZoneName</span></span>
<span data-ttu-id="c3e9a-149">가져올 레코드 집합을 포함 하는 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-149">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="c3e9a-150">*ResourceGroupName* 매개 변수를 사용 하 여 영역을 포함 하는 리소스 그룹도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-150">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="c3e9a-151">또는 *zone* 매개 변수를 사용 하 여 DNS 영역 개체를 전달 하 여 영역 및 리소스 그룹을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-151">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="c3e9a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e9a-152">CommonParameters</span></span>
<span data-ttu-id="c3e9a-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e9a-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3e9a-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e9a-155">입력</span><span class="sxs-lookup"><span data-stu-id="c3e9a-155">INPUTS</span></span>

### <span data-ttu-id="c3e9a-156">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="c3e9a-156">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="c3e9a-157">**DnsZone** 개체를이 cmdlet에 파이프 하 여 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-157">You can pipe a **DnsZone** object to this cmdlet.</span></span>
<span data-ttu-id="c3e9a-158">**DnsZone** 개체는 **레코드 집합** 개체를 찾을 영역을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-158">The **DnsZone** object represents the zone in which to look for the **RecordSet** object.</span></span>

## <span data-ttu-id="c3e9a-159">출력</span><span class="sxs-lookup"><span data-stu-id="c3e9a-159">OUTPUTS</span></span>

### <span data-ttu-id="c3e9a-160">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3e9a-160">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="c3e9a-161">이 cmdlet은 검색 된 레코드 집합을 나타내는 하나 이상의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-161">This cmdlet returns one or more objects that represents the record sets that are found.</span></span>
<span data-ttu-id="c3e9a-162">*Name* 및 *RecordType* 매개 변수를 지정한 경우 **레코드 집합** 을 하나만 반환 하 고, 그렇지 않으면 여러 **레코드 집합** 개체가 배열로 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c3e9a-162">There will be at most one **RecordSet** returned if the *Name* and *RecordType* parameters are specified, otherwise multiple **RecordSet** objects are returned as an array.</span></span>

## <span data-ttu-id="c3e9a-163">상속자</span><span class="sxs-lookup"><span data-stu-id="c3e9a-163">NOTES</span></span>

## <span data-ttu-id="c3e9a-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3e9a-164">RELATED LINKS</span></span>

[<span data-ttu-id="c3e9a-165">새로운 AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3e9a-165">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="c3e9a-166">제거-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3e9a-166">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="c3e9a-167">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3e9a-167">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)



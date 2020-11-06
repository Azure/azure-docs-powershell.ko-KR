---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/get-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Get-AzureRmDnsRecordSet.md
ms.openlocfilehash: 5c7a2a42964be10aa02f4c3205e701b310febb78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532848"
---
# <span data-ttu-id="d2005-101">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d2005-101">Get-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="d2005-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2005-102">SYNOPSIS</span></span>
<span data-ttu-id="d2005-103">DNS 레코드 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-103">Gets a DNS record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2005-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2005-104">SYNTAX</span></span>

### <span data-ttu-id="d2005-105">필드인</span><span class="sxs-lookup"><span data-stu-id="d2005-105">Fields</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2005-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="d2005-106">Object</span></span>
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2005-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d2005-107">DESCRIPTION</span></span>
<span data-ttu-id="d2005-108">**AzureRmDnsRecordSet** cmdlet은 지정 된 영역에서 지정 된 이름 및 형식으로 DNS (Domain Name System) 레코드 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-108">The **Get-AzureRmDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>

<span data-ttu-id="d2005-109">*Name* 또는 *RecordType* 매개 변수를 지정 하지 않으면이 cmdlet은 영역에 지정 된 형식의 모든 레코드 집합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="d2005-110">*Name* 매개 변수를 제외한 *RecordType* 매개 변수를 지정 하면이 cmdlet은 지정 된 레코드 형식의 모든 레코드 집합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>

<span data-ttu-id="d2005-111">파이프라인 연산자를 사용 하 여 **DnsZone** 개체를이 cmdlet에 전달 하거나, **DnsZone** 개체를 *zone* 매개 변수로 전달 하거나, 이름을 기준으로 영역과 리소스 그룹을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="d2005-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d2005-112">EXAMPLES</span></span>

### <span data-ttu-id="d2005-113">예제 1: 지정 된 이름 및 형식으로 레코드 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="d2005-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="d2005-114">이 명령은 지정 된 리소스 그룹 및 영역에서 www 라는 레코드 종류의 레코드 집합을 가져온 다음이를 $RecordSet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="d2005-115">*Name* 및 *RecordType* 매개 변수는 지정 되어 있으므로 하나의 **레코드 집합** 개체만 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="d2005-116">예제 2: 지정 된 형식의 레코드 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="d2005-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="d2005-117">이 명령은 MyResourceGroup 이라는 리소스 그룹에 있는 myzone.com 이라는 영역에 있는 레코드 종류 A의 모든 레코드 집합의 배열을 가져온 다음이를 $RecordSets 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="d2005-118">예제 3: 영역의 모든 레코드 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="d2005-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="d2005-119">이 명령은 MyResourceGroup 이라는 리소스 그룹의 myzone.com 이라는 영역에 있는 모든 레코드 집합의 배열을 가져온 다음이를 $RecordSets 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="d2005-120">예제 4: DnsZone 개체를 사용 하 여 영역의 모든 레코드 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="d2005-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

<span data-ttu-id="d2005-121">이 예제는 위의 예제 3과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="d2005-122">이번에는 zone 개체를 사용 하 여 영역이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="d2005-123">변수</span><span class="sxs-lookup"><span data-stu-id="d2005-123">PARAMETERS</span></span>

### <span data-ttu-id="d2005-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2005-124">-DefaultProfile</span></span>
<span data-ttu-id="d2005-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d2005-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2005-126">-이름</span><span class="sxs-lookup"><span data-stu-id="d2005-126">-Name</span></span>
<span data-ttu-id="d2005-127">가져올 **레코드 집합** 의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="d2005-128">*Name* 매개 변수를 지정 하지 않으면 지정 된 형식의 모든 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

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

### <span data-ttu-id="d2005-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="d2005-129">-RecordType</span></span>
<span data-ttu-id="d2005-130">이 cmdlet이 가져오는 DNS 레코드의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-130">Specifies the type of DNS record that this cmdlet gets.</span></span>

<span data-ttu-id="d2005-131">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-131">Valid values are:</span></span> 

- <span data-ttu-id="d2005-132">에서</span><span class="sxs-lookup"><span data-stu-id="d2005-132">A</span></span>
- <span data-ttu-id="d2005-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="d2005-133">AAAA</span></span>
- <span data-ttu-id="d2005-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="d2005-134">CNAME</span></span>
- <span data-ttu-id="d2005-135">멕시코</span><span class="sxs-lookup"><span data-stu-id="d2005-135">MX</span></span>
- <span data-ttu-id="d2005-136">NS</span><span class="sxs-lookup"><span data-stu-id="d2005-136">NS</span></span>
- <span data-ttu-id="d2005-137">PTR 레코드로</span><span class="sxs-lookup"><span data-stu-id="d2005-137">PTR</span></span>
- <span data-ttu-id="d2005-138">SOA</span><span class="sxs-lookup"><span data-stu-id="d2005-138">SOA</span></span>
- <span data-ttu-id="d2005-139">SRV</span><span class="sxs-lookup"><span data-stu-id="d2005-139">SRV</span></span>
- <span data-ttu-id="d2005-140">라는</span><span class="sxs-lookup"><span data-stu-id="d2005-140">TXT</span></span>

<span data-ttu-id="d2005-141">*RecordType* 매개 변수를 지정 하지 않으면 *Name* 매개 변수도 생략 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-141">If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="d2005-142">그런 다음이 cmdlet은 모든 이름과 형식의 영역에 있는 모든 레코드 집합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-142">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

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

### <span data-ttu-id="d2005-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2005-143">-ResourceGroupName</span></span>
<span data-ttu-id="d2005-144">DNS 영역이 포함 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-144">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="d2005-145">*ZoneName* 매개 변수를 사용 하 여 영역 이름도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-145">The zone name must also be specified, using the *ZoneName* parameter.</span></span>

<span data-ttu-id="d2005-146">또는 *zone* 매개 변수를 사용 하 여 **DnsZone** 개체를 전달 하 여 영역 및 리소스 그룹을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-146">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="d2005-147">-Zone</span><span class="sxs-lookup"><span data-stu-id="d2005-147">-Zone</span></span>
<span data-ttu-id="d2005-148">이 cmdlet이 가져오는 레코드 집합을 포함 하는 DNS 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-148">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="d2005-149">또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-149">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="d2005-150">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="d2005-150">-ZoneName</span></span>
<span data-ttu-id="d2005-151">가져올 레코드 집합을 포함 하는 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-151">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="d2005-152">*ResourceGroupName* 매개 변수를 사용 하 여 영역을 포함 하는 리소스 그룹도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-152">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="d2005-153">또는 *zone* 매개 변수를 사용 하 여 DNS 영역 개체를 전달 하 여 영역 및 리소스 그룹을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-153">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="d2005-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2005-154">CommonParameters</span></span>
<span data-ttu-id="d2005-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2005-156">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2005-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2005-157">입력</span><span class="sxs-lookup"><span data-stu-id="d2005-157">INPUTS</span></span>

### <span data-ttu-id="d2005-158">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="d2005-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="d2005-159">**DnsZone** 개체를이 cmdlet에 파이프 하 여 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-159">You can pipe a **DnsZone** object to this cmdlet.</span></span>
<span data-ttu-id="d2005-160">**DnsZone** 개체는 **레코드 집합** 개체를 찾을 영역을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-160">The **DnsZone** object represents the zone in which to look for the **RecordSet** object.</span></span>

## <span data-ttu-id="d2005-161">출력</span><span class="sxs-lookup"><span data-stu-id="d2005-161">OUTPUTS</span></span>

### <span data-ttu-id="d2005-162">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d2005-162">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="d2005-163">이 cmdlet은 검색 된 레코드 집합을 나타내는 하나 이상의 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-163">This cmdlet returns one or more objects that represents the record sets that are found.</span></span>
<span data-ttu-id="d2005-164">*Name* 및 *RecordType* 매개 변수를 지정한 경우 **레코드 집합** 을 하나만 반환 하 고, 그렇지 않으면 여러 **레코드 집합** 개체가 배열로 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2005-164">There will be at most one **RecordSet** returned if the *Name* and *RecordType* parameters are specified, otherwise multiple **RecordSet** objects are returned as an array.</span></span>

## <span data-ttu-id="d2005-165">상속자</span><span class="sxs-lookup"><span data-stu-id="d2005-165">NOTES</span></span>

## <span data-ttu-id="d2005-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2005-166">RELATED LINKS</span></span>

[<span data-ttu-id="d2005-167">새로운 AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d2005-167">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="d2005-168">제거-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d2005-168">Remove-AzureRmDnsRecordSet</span></span>](./Remove-AzureRmDnsRecordSet.md)

[<span data-ttu-id="d2005-169">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="d2005-169">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)


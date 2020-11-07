---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 37cd1f7b00cbfae6421b5dab06ce87c0f462434c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696563"
---
# <span data-ttu-id="59fb8-101">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="59fb8-101">Get-AzDnsRecordSet</span></span>

## <span data-ttu-id="59fb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="59fb8-103">DNS 레코드 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-103">Gets a DNS record set.</span></span>

## <span data-ttu-id="59fb8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59fb8-104">SYNTAX</span></span>

### <span data-ttu-id="59fb8-105">필드인</span><span class="sxs-lookup"><span data-stu-id="59fb8-105">Fields</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59fb8-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="59fb8-106">Object</span></span>
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59fb8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="59fb8-107">DESCRIPTION</span></span>
<span data-ttu-id="59fb8-108">**AzDnsRecordSet** cmdlet은 지정 된 영역에서 지정 된 이름 및 형식으로 DNS (Domain Name System) 레코드 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-108">The **Get-AzDnsRecordSet** cmdlet gets the Domain Name System (DNS) record set with the specified name and type, in the specified zone.</span></span>
<span data-ttu-id="59fb8-109">*Name* 또는 *RecordType* 매개 변수를 지정 하지 않으면이 cmdlet은 영역에 지정 된 형식의 모든 레코드 집합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-109">If you do not specify the *Name* or *RecordType* parameters, this cmdlet returns all record sets of the specified type in the zone.</span></span>
<span data-ttu-id="59fb8-110">*Name* 매개 변수를 제외한 *RecordType* 매개 변수를 지정 하면이 cmdlet은 지정 된 레코드 형식의 모든 레코드 집합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-110">If you specify the *RecordType* parameter but not the *Name* parameter, this cmdlet returns all record sets of the specified record type.</span></span>
<span data-ttu-id="59fb8-111">파이프라인 연산자를 사용 하 여 **DnsZone** 개체를이 cmdlet에 전달 하거나, **DnsZone** 개체를 *zone* 매개 변수로 전달 하거나, 이름을 기준으로 영역과 리소스 그룹을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-111">You can use the pipeline operator to pass a **DnsZone** object to this cmdlet, or you can pass a **DnsZone** object as the *Zone* parameter, or alternatively you can specify the zone and resource group by name.</span></span>

## <span data-ttu-id="59fb8-112">예제의</span><span class="sxs-lookup"><span data-stu-id="59fb8-112">EXAMPLES</span></span>

### <span data-ttu-id="59fb8-113">예제 1: 지정 된 이름 및 형식으로 레코드 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="59fb8-113">Example 1: Get record sets with a specified name and type</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

<span data-ttu-id="59fb8-114">이 명령은 지정 된 리소스 그룹 및 영역에서 www 라는 레코드 종류의 레코드 집합을 가져온 다음이를 $RecordSet 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-114">This command gets the record set of record type A named www in the specified resource group and zone, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="59fb8-115">*Name* 및 *RecordType* 매개 변수는 지정 되어 있으므로 하나의 **레코드 집합** 개체만 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-115">Because the *Name* and *RecordType* parameters are specified, only one **RecordSet** object is returned.</span></span>

### <span data-ttu-id="59fb8-116">예제 2: 지정 된 형식의 레코드 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="59fb8-116">Example 2: Get record sets of a specified type</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

<span data-ttu-id="59fb8-117">이 명령은 MyResourceGroup 이라는 리소스 그룹에 있는 myzone.com 이라는 영역에 있는 레코드 종류 A의 모든 레코드 집합의 배열을 가져온 다음이를 $RecordSets 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-117">This command gets an array of all record sets of record type A in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="59fb8-118">예제 3: 영역의 모든 레코드 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="59fb8-118">Example 3: Get all record sets in a zone</span></span>
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

<span data-ttu-id="59fb8-119">이 명령은 MyResourceGroup 이라는 리소스 그룹의 myzone.com 이라는 영역에 있는 모든 레코드 집합의 배열을 가져온 다음이를 $RecordSets 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-119">This command gets an array of all record sets in the zone named myzone.com in the resource group named MyResourceGroup, and then stores them in the $RecordSets variable.</span></span>

### <span data-ttu-id="59fb8-120">예제 4: DnsZone 개체를 사용 하 여 영역의 모든 레코드 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="59fb8-120">Example 4: Get all record sets in a zone, using a DnsZone object</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

<span data-ttu-id="59fb8-121">이 예제는 위의 예제 3과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-121">This example is equivalent to Example 3 above.</span></span>
<span data-ttu-id="59fb8-122">이번에는 zone 개체를 사용 하 여 영역이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-122">This time, the zone is specified using a zone object.</span></span>

## <span data-ttu-id="59fb8-123">변수</span><span class="sxs-lookup"><span data-stu-id="59fb8-123">PARAMETERS</span></span>

### <span data-ttu-id="59fb8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59fb8-124">-DefaultProfile</span></span>
<span data-ttu-id="59fb8-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="59fb8-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59fb8-126">-이름</span><span class="sxs-lookup"><span data-stu-id="59fb8-126">-Name</span></span>
<span data-ttu-id="59fb8-127">가져올 **레코드 집합** 의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-127">Specifies the name of the **RecordSet** to get.</span></span>
<span data-ttu-id="59fb8-128">*Name* 매개 변수를 지정 하지 않으면 지정 된 형식의 모든 레코드 집합이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-128">If you do not specify the *Name* parameter, all record sets of the specified type are returned.</span></span>

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

### <span data-ttu-id="59fb8-129">-RecordType</span><span class="sxs-lookup"><span data-stu-id="59fb8-129">-RecordType</span></span>
<span data-ttu-id="59fb8-130">이 cmdlet이 가져오는 DNS 레코드의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-130">Specifies the type of DNS record that this cmdlet gets.</span></span>
<span data-ttu-id="59fb8-131">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-131">Valid values are:</span></span> 
- <span data-ttu-id="59fb8-132">에서</span><span class="sxs-lookup"><span data-stu-id="59fb8-132">A</span></span>
- <span data-ttu-id="59fb8-133">AAAA</span><span class="sxs-lookup"><span data-stu-id="59fb8-133">AAAA</span></span>
- <span data-ttu-id="59fb8-134">CNAME</span><span class="sxs-lookup"><span data-stu-id="59fb8-134">CNAME</span></span>
- <span data-ttu-id="59fb8-135">멕시코</span><span class="sxs-lookup"><span data-stu-id="59fb8-135">MX</span></span>
- <span data-ttu-id="59fb8-136">NS</span><span class="sxs-lookup"><span data-stu-id="59fb8-136">NS</span></span>
- <span data-ttu-id="59fb8-137">PTR 레코드로</span><span class="sxs-lookup"><span data-stu-id="59fb8-137">PTR</span></span>
- <span data-ttu-id="59fb8-138">SOA</span><span class="sxs-lookup"><span data-stu-id="59fb8-138">SOA</span></span>
- <span data-ttu-id="59fb8-139">SRV</span><span class="sxs-lookup"><span data-stu-id="59fb8-139">SRV</span></span>
- <span data-ttu-id="59fb8-140">TXT *RecordType* 매개 변수를 지정 하지 않은 경우에는 *Name* 매개 변수도 생략 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-140">TXT If you do not specify the *RecordType* parameter, you must also omit the *Name* parameter.</span></span> <span data-ttu-id="59fb8-141">그런 다음이 cmdlet은 모든 이름과 형식의 영역에 있는 모든 레코드 집합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-141">This cmdlet then returns all record sets in the zone (of all names and types).</span></span>

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

### <span data-ttu-id="59fb8-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59fb8-142">-ResourceGroupName</span></span>
<span data-ttu-id="59fb8-143">DNS 영역이 포함 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-143">Specifies the resource group that contains the DNS zone.</span></span>
<span data-ttu-id="59fb8-144">*ZoneName* 매개 변수를 사용 하 여 영역 이름도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-144">The zone name must also be specified, using the *ZoneName* parameter.</span></span>
<span data-ttu-id="59fb8-145">또는 *zone* 매개 변수를 사용 하 여 **DnsZone** 개체를 전달 하 여 영역 및 리소스 그룹을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-145">Alternatively, you can specify the zone and resource group by passing in a **DnsZone** object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="59fb8-146">-Zone</span><span class="sxs-lookup"><span data-stu-id="59fb8-146">-Zone</span></span>
<span data-ttu-id="59fb8-147">이 cmdlet이 가져오는 레코드 집합을 포함 하는 DNS 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-147">Specifies the DNS zone that contains the record set that this cmdlet gets.</span></span>
<span data-ttu-id="59fb8-148">또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-148">Alternatively, you can specify the zone using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="59fb8-149">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="59fb8-149">-ZoneName</span></span>
<span data-ttu-id="59fb8-150">가져올 레코드 집합을 포함 하는 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-150">Specifies the name of the DNS zone that contains the record set to get.</span></span>
<span data-ttu-id="59fb8-151">*ResourceGroupName* 매개 변수를 사용 하 여 영역을 포함 하는 리소스 그룹도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-151">The resource group containing the zone must also be specified, using the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="59fb8-152">또는 *zone* 매개 변수를 사용 하 여 DNS 영역 개체를 전달 하 여 영역 및 리소스 그룹을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-152">Alternatively, you can specify the zone and resource group by passing in a DNS Zone object using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="59fb8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59fb8-153">CommonParameters</span></span>
<span data-ttu-id="59fb8-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59fb8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59fb8-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59fb8-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59fb8-156">입력</span><span class="sxs-lookup"><span data-stu-id="59fb8-156">INPUTS</span></span>

### <span data-ttu-id="59fb8-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="59fb8-157">System.String</span></span>

### <span data-ttu-id="59fb8-158">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="59fb8-158">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="59fb8-159">시스템 Null 허용 ' 1 [[RecordType, Microsoft azure. 관리. Dns, 버전 = 3.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="59fb8-159">System.Nullable\`1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="59fb8-160">출력</span><span class="sxs-lookup"><span data-stu-id="59fb8-160">OUTPUTS</span></span>

### <span data-ttu-id="59fb8-161">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="59fb8-161">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="59fb8-162">상속자</span><span class="sxs-lookup"><span data-stu-id="59fb8-162">NOTES</span></span>

## <span data-ttu-id="59fb8-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59fb8-163">RELATED LINKS</span></span>

[<span data-ttu-id="59fb8-164">새로운 AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="59fb8-164">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="59fb8-165">제거-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="59fb8-165">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

[<span data-ttu-id="59fb8-166">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="59fb8-166">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)



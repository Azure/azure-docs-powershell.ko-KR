---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsRecordSet.md
ms.openlocfilehash: fce5cbe993861d2a0d97bffd4bf4c7dbe19cc535
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702738"
---
# <span data-ttu-id="3eb98-101">Remove-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3eb98-101">Remove-AzureRmDnsRecordSet</span></span>

## <span data-ttu-id="3eb98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eb98-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb98-103">레코드 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-103">Deletes a record set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3eb98-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3eb98-104">SYNTAX</span></span>

### <span data-ttu-id="3eb98-105">필드인</span><span class="sxs-lookup"><span data-stu-id="3eb98-105">Fields</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eb98-106">섞여</span><span class="sxs-lookup"><span data-stu-id="3eb98-106">Mixed</span></span>
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eb98-107">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="3eb98-107">Object</span></span>
```
Remove-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eb98-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3eb98-108">DESCRIPTION</span></span>
<span data-ttu-id="3eb98-109">**AzureRmDnsRecordSet** cmdlet은 지정 된 영역에서 지정 된 레코드 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-109">The **Remove-AzureRmDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="3eb98-110">영역 apex에서 자동으로 만들어지는 SOA 또는 NS (이름 서버) 레코드는 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>

<span data-ttu-id="3eb98-111">파이프라인 연산자 또는 매개 변수를 사용 하 여이 cmdlet에 **RecordSet** 개체를 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="3eb98-112">**레코드 집합 개체를** 사용 하지 않고 이름 및 형식을 기준으로 하 여 변수를 확인 하려면 파이프라인 연산자 또는 매개 변수를 사용 하 여이 Cmdlet에 **DnsZone** 개체로 영역을 전달 하거나 *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="3eb98-113">확인 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="3eb98-114">**RecordSet** 개체를 사용 하 여 레코드 집합을 지정 하는 경우 로컬 **RecordSet** 개체를 검색 한 후 Azure DNS에서 레코드 집합이 변경 되 면 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="3eb98-115">이는 동시 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="3eb98-116">동시 변경 내용에 관계 없이 레코드 집합을 삭제 하는 *Overwrite* 매개 변수를 사용 하 여이를 억제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="3eb98-117">예제의</span><span class="sxs-lookup"><span data-stu-id="3eb98-117">EXAMPLES</span></span>

### <span data-ttu-id="3eb98-118">예제 1: 레코드 집합 제거</span><span class="sxs-lookup"><span data-stu-id="3eb98-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="3eb98-119">첫 번째 명령은 지정 된 레코드 집합을 가져온 다음 $RecordSet 변수에 저장 합니다. 두 번째 명령은 $RecordSet에 설정 된 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="3eb98-120">예제 2: 레코드 집합 제거 및 모든 확인 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="3eb98-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="3eb98-121">첫 번째 명령은 지정 된 레코드 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-121">The first command gets the specified record set.</span></span>

<span data-ttu-id="3eb98-122">두 번째 명령은 레코드 집합을 삭제 했지만 그 동안에는 레코드가 변경 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="3eb98-123">확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="3eb98-124">변수</span><span class="sxs-lookup"><span data-stu-id="3eb98-124">PARAMETERS</span></span>

### <span data-ttu-id="3eb98-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb98-125">-DefaultProfile</span></span>
<span data-ttu-id="3eb98-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3eb98-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3eb98-127">-Force</span><span class="sxs-lookup"><span data-stu-id="3eb98-127">-Force</span></span>
<span data-ttu-id="3eb98-128">이 매개 변수는이 cmdlet에 대해 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-128">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="3eb98-129">이후 릴리스에서 제거 될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-129">It will be removed in a future release.</span></span>

<span data-ttu-id="3eb98-130">이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어 하려면 *Confirm* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-130">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb98-131">-이름</span><span class="sxs-lookup"><span data-stu-id="3eb98-131">-Name</span></span>
<span data-ttu-id="3eb98-132">제거할 **레코드 집합** 의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-132">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="3eb98-133">이름으로 레코드 집합을 지정 하는 경우 *영역* 매개 변수 또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 DNS 영역을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-133">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="3eb98-134">또는 레코드 집합 *은 레코드 집합 매개 변수* 를 사용 하 여 전달 되는 **레코드** 집합 개체를 사용 하 여 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-134">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: Fields, Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb98-135">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="3eb98-135">-Overwrite</span></span>
<span data-ttu-id="3eb98-136">**RecordSet** 개체를 사용 하 여 레코드 집합을 지정 하는 경우 로컬 **RecordSet** 개체를 검색 한 후 Azure DNS에서 레코드 집합이 변경 되 면 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-136">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="3eb98-137">이는 동시 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-137">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="3eb98-138">이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며, 동시 변경 내용에 관계 없이 레코드 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-138">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="3eb98-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3eb98-139">-PassThru</span></span>
<span data-ttu-id="3eb98-140">passthru</span><span class="sxs-lookup"><span data-stu-id="3eb98-140">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eb98-141">-레코드 집합</span><span class="sxs-lookup"><span data-stu-id="3eb98-141">-RecordSet</span></span>
<span data-ttu-id="3eb98-142">제거할 **레코드 집합** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-142">Specifies the **RecordSet** object to remove.</span></span>

<span data-ttu-id="3eb98-143">또는 *이름* , *영역* 매개 변수를 사용 하거나 *name* , *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 레코드 집합을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-143">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsRecordSet
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb98-144">-RecordType</span><span class="sxs-lookup"><span data-stu-id="3eb98-144">-RecordType</span></span>
<span data-ttu-id="3eb98-145">DNS 레코드의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-145">Specifies the type of DNS record.</span></span>

<span data-ttu-id="3eb98-146">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-146">Valid values are:</span></span>

- <span data-ttu-id="3eb98-147">에서</span><span class="sxs-lookup"><span data-stu-id="3eb98-147">A</span></span>
- <span data-ttu-id="3eb98-148">AAAA</span><span class="sxs-lookup"><span data-stu-id="3eb98-148">AAAA</span></span>
- <span data-ttu-id="3eb98-149">CNAME</span><span class="sxs-lookup"><span data-stu-id="3eb98-149">CNAME</span></span>
- <span data-ttu-id="3eb98-150">멕시코</span><span class="sxs-lookup"><span data-stu-id="3eb98-150">MX</span></span>
- <span data-ttu-id="3eb98-151">NS</span><span class="sxs-lookup"><span data-stu-id="3eb98-151">NS</span></span>
- <span data-ttu-id="3eb98-152">PTR 레코드로</span><span class="sxs-lookup"><span data-stu-id="3eb98-152">PTR</span></span>
- <span data-ttu-id="3eb98-153">SRV</span><span class="sxs-lookup"><span data-stu-id="3eb98-153">SRV</span></span>
- <span data-ttu-id="3eb98-154">라는</span><span class="sxs-lookup"><span data-stu-id="3eb98-154">TXT</span></span>

<span data-ttu-id="3eb98-155">SOA 레코드는 영역이 삭제 될 때 자동으로 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-155">SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="3eb98-156">SOA 레코드는 수동으로 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-156">You cannot manually delete SOA records.</span></span>

```yaml
Type: RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb98-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb98-157">-ResourceGroupName</span></span>
<span data-ttu-id="3eb98-158">삭제할 **레코드 집합** 을 포함 하는 DNS 영역이 포함 된 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-158">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="3eb98-159">이 매개 변수는 record set 및 DNS 영역이 *Name* 및 *ZoneName* 매개 변수를 사용 하 여 지정 된 경우에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-159">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>

<span data-ttu-id="3eb98-160">또는 *RecordSet* 매개 변수 또는 *Name* 및 *Zone* 매개 변수를 사용 하 여 레코드 집합을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-160">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="3eb98-161">-Zone</span><span class="sxs-lookup"><span data-stu-id="3eb98-161">-Zone</span></span>
<span data-ttu-id="3eb98-162">삭제할 **레코드 집합** 을 포함 하는 DNS 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-162">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="3eb98-163">이 매개 변수는 *Name* 매개 변수를 사용 하 여 레코드 집합을 지정 하는 경우에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-163">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>

<span data-ttu-id="3eb98-164">또는 *RecordSet* 매개 변수 또는 *Name* , *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 레코드 집합을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-164">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* , *ZoneName* , and *ResourceGroupName* parameters.</span></span>

```yaml
Type: DnsZone
Parameter Sets: Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb98-165">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="3eb98-165">-ZoneName</span></span>
<span data-ttu-id="3eb98-166">삭제할 **레코드 집합** 을 포함 하는 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-166">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="3eb98-167">또한 *Name* 및 *ResourceGroupName* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-167">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="3eb98-168">또는 레코드 집합은 *레코드* 집합 매개 변수 또는 *Name* 및 *Zone* 매개 변수를 사용 하 여 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-168">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="3eb98-169">-확인</span><span class="sxs-lookup"><span data-stu-id="3eb98-169">-Confirm</span></span>
<span data-ttu-id="3eb98-170">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eb98-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eb98-171">-WhatIf</span></span>
<span data-ttu-id="3eb98-172">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eb98-173">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eb98-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb98-174">CommonParameters</span></span>
<span data-ttu-id="3eb98-175">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb98-176">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb98-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb98-177">입력</span><span class="sxs-lookup"><span data-stu-id="3eb98-177">INPUTS</span></span>

### <span data-ttu-id="3eb98-178">Microsoft Azure. DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3eb98-178">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>
<span data-ttu-id="3eb98-179">**RecordSet** 개체를이 cmdlet에 파이프 하 여 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-179">You can pipe a **RecordSet** object to this cmdlet.</span></span>

## <span data-ttu-id="3eb98-180">출력</span><span class="sxs-lookup"><span data-stu-id="3eb98-180">OUTPUTS</span></span>

### <span data-ttu-id="3eb98-181">않아야</span><span class="sxs-lookup"><span data-stu-id="3eb98-181">None</span></span>
<span data-ttu-id="3eb98-182">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-182">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="3eb98-183">상속자</span><span class="sxs-lookup"><span data-stu-id="3eb98-183">NOTES</span></span>
<span data-ttu-id="3eb98-184">*확인* 매개 변수를 사용 하 여이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-184">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="3eb98-185">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 변수의 값이 중간 인지 아래 인지 여부를 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-185">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="3eb98-186">*확인* 또는 *확인: $True* 를 지정 하는 경우이 cmdlet을 실행 하기 전에 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-186">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="3eb98-187">*확인: $False* 를 지정 하면 cmdlet에서 확인을 요구 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb98-187">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3eb98-188">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3eb98-188">RELATED LINKS</span></span>

[<span data-ttu-id="3eb98-189">Get-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3eb98-189">Get-AzureRmDnsRecordSet</span></span>](./Get-AzureRmDnsRecordSet.md)

[<span data-ttu-id="3eb98-190">새로운 AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3eb98-190">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="3eb98-191">Set-AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="3eb98-191">Set-AzureRmDnsRecordSet</span></span>](./Set-AzureRmDnsRecordSet.md)

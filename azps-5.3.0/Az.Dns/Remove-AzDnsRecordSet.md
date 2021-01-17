---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: f5d7075322bb2b5a4b61635400664f0e909f126d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489844"
---
# <span data-ttu-id="106f9-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="106f9-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="106f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="106f9-102">SYNOPSIS</span></span>
<span data-ttu-id="106f9-103">레코드 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-103">Deletes a record set.</span></span>

## <span data-ttu-id="106f9-104">구문</span><span class="sxs-lookup"><span data-stu-id="106f9-104">SYNTAX</span></span>

### <span data-ttu-id="106f9-105">필드</span><span class="sxs-lookup"><span data-stu-id="106f9-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="106f9-106">혼합</span><span class="sxs-lookup"><span data-stu-id="106f9-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="106f9-107">개체</span><span class="sxs-lookup"><span data-stu-id="106f9-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="106f9-108">설명</span><span class="sxs-lookup"><span data-stu-id="106f9-108">DESCRIPTION</span></span>
<span data-ttu-id="106f9-109">**Remove-AzDnsRecordSet** cmdlet은 지정된 영역의 지정된 레코드 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="106f9-110">영역 apex에서 자동으로 생성된 SOA 또는 NS(이름 서버) 레코드는 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="106f9-111">파이프라인 연산자를 사용하여 또는 매개 변수로 **RecordSet** 개체를 이 cmdlet에 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="106f9-112">**RecordSet** 개체를 사용하지 않고 이름 및 형식별로 레코드 집합을 식별하려면 파이프라인 연산자 또는 매개 변수로 사용하여 이 cmdlet에 **DnsZone** 개체로 영역이 전달되어야 합니다. 또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="106f9-113">Confirm 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="106f9-114">**RecordSet** 개체를 사용하여 레코드 집합을 지정할 때 로컬 **RecordSet** 개체를 검색한 후 Azure DNS에서 변경된 레코드 집합은 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="106f9-115">이렇게 하면 동시 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="106f9-116">동시 변경 내용에 관계없이 레코드 집합을 삭제하는 *덮어* 사용 매개 변수를 사용하여 이를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="106f9-117">예제</span><span class="sxs-lookup"><span data-stu-id="106f9-117">EXAMPLES</span></span>

### <span data-ttu-id="106f9-118">예제 1: 레코드 집합 제거</span><span class="sxs-lookup"><span data-stu-id="106f9-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="106f9-119">첫 번째 명령은 지정된 레코드 집합을 1차원 변수에 $RecordSet 저장합니다. 두 번째 명령은 레코드 집합을 $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="106f9-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="106f9-120">예제 2: 레코드 집합 제거 및 모든 확인 표시 안</span><span class="sxs-lookup"><span data-stu-id="106f9-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="106f9-121">첫 번째 명령은 지정된 레코드 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="106f9-122">두 번째 명령은 그동안 변경된 레코드 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="106f9-123">확인 프롬프트가 표시 안 됩니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="106f9-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="106f9-124">PARAMETERS</span></span>

### <span data-ttu-id="106f9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="106f9-125">-DefaultProfile</span></span>
<span data-ttu-id="106f9-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="106f9-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="106f9-127">-Name</span><span class="sxs-lookup"><span data-stu-id="106f9-127">-Name</span></span>
<span data-ttu-id="106f9-128">제거할 **RecordSet의 이름을** 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="106f9-129">레코드 집합을 이름으로 지정할 때 DNS 영역은 *Zone* 매개 변수 또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용하여 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="106f9-130">또는 RecordSet 매개 변수를 사용하여 **전달되는 RecordSet** 개체를 사용하여 레코드 집합을 지정할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="106f9-131">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="106f9-131">-Overwrite</span></span>
<span data-ttu-id="106f9-132">**RecordSet** 개체를 사용하여 레코드 집합을 지정할 때 로컬 **RecordSet** 개체를 검색한 후 Azure DNS에서 변경된 레코드 집합은 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="106f9-133">이렇게 하면 동시 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="106f9-134">이는 동시 변경 내용에 관계없이 레코드 집합을 삭제하는 *덮어* 사용 매개 변수를 사용하여 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="106f9-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="106f9-135">-PassThru</span></span>
<span data-ttu-id="106f9-136">passthru</span><span class="sxs-lookup"><span data-stu-id="106f9-136">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="106f9-137">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="106f9-137">-RecordSet</span></span>
<span data-ttu-id="106f9-138">제거할 **RecordSet** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="106f9-139">또는 이름 및 영역 매개 변수를  사용하여 또는 *이름,* *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용하여 레코드 집합을 지정할 수 있습니다. </span><span class="sxs-lookup"><span data-stu-id="106f9-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="106f9-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="106f9-140">-RecordType</span></span>
<span data-ttu-id="106f9-141">DNS 레코드의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="106f9-142">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="106f9-142">Valid values are:</span></span>
- <span data-ttu-id="106f9-143">A</span><span class="sxs-lookup"><span data-stu-id="106f9-143">A</span></span>
- <span data-ttu-id="106f9-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="106f9-144">AAAA</span></span>
- <span data-ttu-id="106f9-145">CNAME</span><span class="sxs-lookup"><span data-stu-id="106f9-145">CNAME</span></span>
- <span data-ttu-id="106f9-146">MX</span><span class="sxs-lookup"><span data-stu-id="106f9-146">MX</span></span>
- <span data-ttu-id="106f9-147">NS</span><span class="sxs-lookup"><span data-stu-id="106f9-147">NS</span></span>
- <span data-ttu-id="106f9-148">PTR</span><span class="sxs-lookup"><span data-stu-id="106f9-148">PTR</span></span>
- <span data-ttu-id="106f9-149">SRV</span><span class="sxs-lookup"><span data-stu-id="106f9-149">SRV</span></span>
- <span data-ttu-id="106f9-150">영역이 삭제되면 TXT SOA 레코드가 자동으로 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="106f9-151">SOA 레코드는 수동으로 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-151">You cannot manually delete SOA records.</span></span>

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="106f9-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="106f9-152">-ResourceGroupName</span></span>
<span data-ttu-id="106f9-153">삭제할 **RecordSet을** 포함하는 DNS 영역이 포함된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="106f9-154">이 매개 변수는 이름 및 *ZoneName* 매개  변수를 사용하여 레코드 집합 및 DNS 영역이 지정된 경우만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="106f9-155">또는 *RecordSet* 매개 변수 또는 이름 및 영역 매개 변수를 사용하여 레코드 집합을 *지정할* *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="106f9-156">-Zone</span><span class="sxs-lookup"><span data-stu-id="106f9-156">-Zone</span></span>
<span data-ttu-id="106f9-157">삭제할 **RecordSet이** 포함된 DNS 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="106f9-158">이 매개 변수는 이름 매개 변수를 사용하여 레코드 집합을 지정할 때만 *적용할 수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="106f9-159">또는 *RecordSet* 매개 변수 또는 *Name,* *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용하여 레코드 집합을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="106f9-160">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="106f9-160">-ZoneName</span></span>
<span data-ttu-id="106f9-161">삭제할 **RecordSet이** 포함된 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="106f9-162">이름 및 *ResourceGroupName* 매개 변수도 지정해야 합니다. </span><span class="sxs-lookup"><span data-stu-id="106f9-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="106f9-163">또는 *RecordSet* 매개 변수 또는 이름 및 영역 매개 변수를 사용하여 레코드 집합을 *지정할* *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="106f9-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="106f9-164">-Confirm</span></span>
<span data-ttu-id="106f9-165">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="106f9-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="106f9-166">-WhatIf</span></span>
<span data-ttu-id="106f9-167">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="106f9-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="106f9-168">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="106f9-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="106f9-169">CommonParameters</span></span>
<span data-ttu-id="106f9-170">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="106f9-171">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="106f9-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="106f9-172">입력</span><span class="sxs-lookup"><span data-stu-id="106f9-172">INPUTS</span></span>

### <span data-ttu-id="106f9-173">Microsoft.Azure.Management.Dns.Models.RecordType</span><span class="sxs-lookup"><span data-stu-id="106f9-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="106f9-174">System.String</span><span class="sxs-lookup"><span data-stu-id="106f9-174">System.String</span></span>

### <span data-ttu-id="106f9-175">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="106f9-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="106f9-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="106f9-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="106f9-177">출력</span><span class="sxs-lookup"><span data-stu-id="106f9-177">OUTPUTS</span></span>

### <span data-ttu-id="106f9-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="106f9-178">System.Boolean</span></span>

## <span data-ttu-id="106f9-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="106f9-179">NOTES</span></span>
<span data-ttu-id="106f9-180">*확인* 매개 변수를 사용하여 이 cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="106f9-181">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 값이 Medium 또는 lower인 경우 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="106f9-182">*Confirm* 또는 *Confirm:$True* 지정하는 경우 이 cmdlet은 실행 전에 확인을 요청하는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-182">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="106f9-183">*Confirm:$False* 지정하면 cmdlet에서 확인 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="106f9-183">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="106f9-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="106f9-184">RELATED LINKS</span></span>

[<span data-ttu-id="106f9-185">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="106f9-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="106f9-186">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="106f9-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="106f9-187">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="106f9-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)

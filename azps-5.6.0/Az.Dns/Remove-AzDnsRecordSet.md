---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: ab4f7bf6693eda413587b572832706d617b3e683
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984774"
---
# <span data-ttu-id="07bbb-101">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="07bbb-101">Remove-AzDnsRecordSet</span></span>

## <span data-ttu-id="07bbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="07bbb-103">레코드 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-103">Deletes a record set.</span></span>

## <span data-ttu-id="07bbb-104">구문</span><span class="sxs-lookup"><span data-stu-id="07bbb-104">SYNTAX</span></span>

### <span data-ttu-id="07bbb-105">필드</span><span class="sxs-lookup"><span data-stu-id="07bbb-105">Fields</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07bbb-106">혼합</span><span class="sxs-lookup"><span data-stu-id="07bbb-106">Mixed</span></span>
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07bbb-107">개체</span><span class="sxs-lookup"><span data-stu-id="07bbb-107">Object</span></span>
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07bbb-108">설명</span><span class="sxs-lookup"><span data-stu-id="07bbb-108">DESCRIPTION</span></span>
<span data-ttu-id="07bbb-109">**Remove-AzDnsRecordSet** cmdlet은 지정된 영역의 지정된 레코드 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-109">The **Remove-AzDnsRecordSet** cmdlet deletes the specified record set from the specified zone.</span></span>
<span data-ttu-id="07bbb-110">영역 정수에서 자동으로 생성된 SOA 또는 NS(이름 서버) 레코드를 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-110">You cannot delete SOA or name server (NS) records that are automatically created at the zone apex.</span></span>
<span data-ttu-id="07bbb-111">파이프라인 연산자를 사용하여 또는 매개 변수로 **RecordSet** 개체를 이 cmdlet에 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-111">You can pass a **RecordSet** object to this cmdlet by using the pipeline operator or as a parameter.</span></span>
<span data-ttu-id="07bbb-112">**RecordSet** 개체를 사용하지 않고 이름으로 설정된 레코드를 식별하고 형식을 지정하려면 파이프라인 연산자 또는 매개 변수로 이 cmdlet에 **DnsZone** 개체로 구역을 전달하거나 *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-112">To identify a record set by name and type without using a **RecordSet** object, you must pass the zone as a **DnsZone** object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="07bbb-113">확인 매개 변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-113">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="07bbb-114">**RecordSet** 개체를 사용하여 레코드 집합을 지정할 때 로컬 **RecordSet** 개체를 검색한 후 Azure DNS에서 레코드 집합이 변경된 경우 레코드 집합이 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-114">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="07bbb-115">이 기능은 동시 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-115">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="07bbb-116">덮어 덮어  사용 매개 변수를 사용하여 이 기능을 억제할 수 있습니다. 이는 동시 변경 내용에 관계없이 레코드 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-116">You can suppress this by using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="07bbb-117">예제</span><span class="sxs-lookup"><span data-stu-id="07bbb-117">EXAMPLES</span></span>

### <span data-ttu-id="07bbb-118">예제 1: 레코드 집합 제거</span><span class="sxs-lookup"><span data-stu-id="07bbb-118">Example 1: Remove a record set</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="07bbb-119">첫 번째 명령은 지정된 레코드 집합을 얻은 다음, 해당 레코드 집합을 $RecordSet 변수에 저장합니다. 두 번째 명령은 레코드 집합을 $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="07bbb-119">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="07bbb-120">예제 2: 레코드 집합을 제거하고 모든 확인을 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-120">Example 2: Remove a record set and suppress all confirmation</span></span>
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="07bbb-121">첫 번째 명령은 지정된 레코드 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-121">The first command gets the specified record set.</span></span>
<span data-ttu-id="07bbb-122">두 번째 명령은 레코드 집합이 그동안 변경된 경우에도 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-122">The second command deletes the record set, even if it has changed in the meantime.</span></span>
<span data-ttu-id="07bbb-123">확인 프롬프트가 억제됩니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-123">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="07bbb-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="07bbb-124">PARAMETERS</span></span>

### <span data-ttu-id="07bbb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07bbb-125">-DefaultProfile</span></span>
<span data-ttu-id="07bbb-126">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="07bbb-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07bbb-127">-Name</span><span class="sxs-lookup"><span data-stu-id="07bbb-127">-Name</span></span>
<span data-ttu-id="07bbb-128">제거할 **RecordSet의** 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-128">Specifies the name of the **RecordSet** to remove.</span></span>
<span data-ttu-id="07bbb-129">이름으로 레코드 집합을 지정할 때 영역 매개 변수 또는  *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용하여 DNS 영역이 지정되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-129">When specifying the record set by name, the DNS zone must be specified using either the *Zone* parameter or the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="07bbb-130">또는 *RecordSet* 매개 변수를 사용하여 **전달되는 RecordSet** 개체를 사용하여 레코드 집합을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-130">Alternatively, the record set can be specified using a **RecordSet** object, passed using the *RecordSet* parameter.</span></span>

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

### <span data-ttu-id="07bbb-131">-덮어 덮어 덮어 덮어 덮어</span><span class="sxs-lookup"><span data-stu-id="07bbb-131">-Overwrite</span></span>
<span data-ttu-id="07bbb-132">**RecordSet** 개체를 사용하여 레코드 집합을 지정할 때 로컬 **RecordSet** 개체를 검색한 후 Azure DNS에서 레코드 집합이 변경된 경우 레코드 집합이 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-132">When specifying the record set using a **RecordSet** object, the record set is not deleted if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="07bbb-133">이 기능은 동시 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-133">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="07bbb-134">이는 덮어 덮어 사용 매개 변수를 사용하여 억제될 수 있습니다. 이는 동시 변경 내용에 관계없이 레코드 집합을 삭제합니다. </span><span class="sxs-lookup"><span data-stu-id="07bbb-134">This can be suppressed using the *Overwrite* parameter, which deletes the record set regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="07bbb-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07bbb-135">-PassThru</span></span>
<span data-ttu-id="07bbb-136">passthru</span><span class="sxs-lookup"><span data-stu-id="07bbb-136">passthru</span></span>

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

### <span data-ttu-id="07bbb-137">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="07bbb-137">-RecordSet</span></span>
<span data-ttu-id="07bbb-138">제거할 **RecordSet 개체를** 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-138">Specifies the **RecordSet** object to remove.</span></span>
<span data-ttu-id="07bbb-139">또는 이름 및 영역 매개 변수를  사용하여 레코드 집합을 지정하거나 이름 *,* *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용할 수 있습니다. </span><span class="sxs-lookup"><span data-stu-id="07bbb-139">Alternatively, the record set can be specified using the *Name* and *Zone* parameters, or using the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="07bbb-140">-RecordType</span><span class="sxs-lookup"><span data-stu-id="07bbb-140">-RecordType</span></span>
<span data-ttu-id="07bbb-141">DNS 레코드 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-141">Specifies the type of DNS record.</span></span>
<span data-ttu-id="07bbb-142">유효한 값은:</span><span class="sxs-lookup"><span data-stu-id="07bbb-142">Valid values are:</span></span>
- <span data-ttu-id="07bbb-143">A</span><span class="sxs-lookup"><span data-stu-id="07bbb-143">A</span></span>
- <span data-ttu-id="07bbb-144">AAAA</span><span class="sxs-lookup"><span data-stu-id="07bbb-144">AAAA</span></span>
- <span data-ttu-id="07bbb-145">CNAME</span><span class="sxs-lookup"><span data-stu-id="07bbb-145">CNAME</span></span>
- <span data-ttu-id="07bbb-146">MX</span><span class="sxs-lookup"><span data-stu-id="07bbb-146">MX</span></span>
- <span data-ttu-id="07bbb-147">NS</span><span class="sxs-lookup"><span data-stu-id="07bbb-147">NS</span></span>
- <span data-ttu-id="07bbb-148">PTR</span><span class="sxs-lookup"><span data-stu-id="07bbb-148">PTR</span></span>
- <span data-ttu-id="07bbb-149">SRV</span><span class="sxs-lookup"><span data-stu-id="07bbb-149">SRV</span></span>
- <span data-ttu-id="07bbb-150">영역이 삭제되면 TXT SOA 레코드가 자동으로 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-150">TXT SOA records are deleted automatically when the zone is deleted.</span></span>
<span data-ttu-id="07bbb-151">SOA 레코드를 수동으로 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-151">You cannot manually delete SOA records.</span></span>

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

### <span data-ttu-id="07bbb-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07bbb-152">-ResourceGroupName</span></span>
<span data-ttu-id="07bbb-153">삭제할 **RecordSet을** 포함하는 DNS 영역이 포함된 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-153">Specifies the resource group that contains the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="07bbb-154">이 매개 변수는 이름 및 *ZoneName* 매개  변수를 사용하여 레코드 집합 및 DNS 영역이 지정된 경우만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-154">This parameter is applicable only when the record set and DNS zone are specified using the *Name* and *ZoneName* parameters.</span></span>
<span data-ttu-id="07bbb-155">또는 *RecordSet* 매개 변수 또는 이름 및 영역 매개 변수를 사용하여 레코드 집합을 *지정할* *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-155">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="07bbb-156">-Zone</span><span class="sxs-lookup"><span data-stu-id="07bbb-156">-Zone</span></span>
<span data-ttu-id="07bbb-157">삭제할 **RecordSet이** 포함된 DNS 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-157">Specifies the DNS zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="07bbb-158">이 매개 변수는 이름 매개 변수를 사용하여 레코드 집합을 지정할 *때만 적용할 수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-158">This parameter is applicable only when specifying the record set using the *Name* parameter.</span></span>
<span data-ttu-id="07bbb-159">또는 *RecordSet* 매개 변수 또는 이름 *,* *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용하여 레코드 집합을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-159">Alternatively, you can specify the record set using either the *RecordSet* parameter, or the *Name*, *ZoneName*, and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="07bbb-160">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="07bbb-160">-ZoneName</span></span>
<span data-ttu-id="07bbb-161">삭제할 **RecordSet이** 포함된 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-161">Specifies the name of the zone that contains the **RecordSet** to delete.</span></span>
<span data-ttu-id="07bbb-162">이름 및 *ResourceGroupName 매개 변수도 지정해야* 합니다. </span><span class="sxs-lookup"><span data-stu-id="07bbb-162">You must also specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="07bbb-163">또는 *RecordSet* 매개 변수 또는 이름 및 영역 매개 변수를 사용하여 레코드 집합을 *지정할* *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-163">Alternatively, the record set can be specified using either the *RecordSet* parameter, or the *Name* and *Zone* parameters.</span></span>

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

### <span data-ttu-id="07bbb-164">-확인</span><span class="sxs-lookup"><span data-stu-id="07bbb-164">-Confirm</span></span>
<span data-ttu-id="07bbb-165">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07bbb-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07bbb-166">-WhatIf</span></span>
<span data-ttu-id="07bbb-167">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07bbb-168">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07bbb-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07bbb-169">CommonParameters</span></span>
<span data-ttu-id="07bbb-170">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07bbb-171">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="07bbb-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07bbb-172">입력</span><span class="sxs-lookup"><span data-stu-id="07bbb-172">INPUTS</span></span>

### <span data-ttu-id="07bbb-173">Microsoft.Azure.Management.Dns.Models.RecordType</span><span class="sxs-lookup"><span data-stu-id="07bbb-173">Microsoft.Azure.Management.Dns.Models.RecordType</span></span>

### <span data-ttu-id="07bbb-174">System.String</span><span class="sxs-lookup"><span data-stu-id="07bbb-174">System.String</span></span>

### <span data-ttu-id="07bbb-175">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="07bbb-175">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

### <span data-ttu-id="07bbb-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="07bbb-176">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="07bbb-177">출력</span><span class="sxs-lookup"><span data-stu-id="07bbb-177">OUTPUTS</span></span>

### <span data-ttu-id="07bbb-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="07bbb-178">System.Boolean</span></span>

## <span data-ttu-id="07bbb-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="07bbb-179">NOTES</span></span>
<span data-ttu-id="07bbb-180">확인 매개  변수를 사용하여 이 cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-180">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="07bbb-181">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 값이 중간 또는 더 낮은지 확인하라는 메시지를 묻는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-181">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="07bbb-182">확인 또는 *확인:$True* 지정하는 경우 이 cmdlet은 실행하기 전에 확인을 묻는 메시지를 표시합니다. </span><span class="sxs-lookup"><span data-stu-id="07bbb-182">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="07bbb-183">*Confirm:$False* 지정하면 cmdlet에서 확인을 묻는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07bbb-183">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="07bbb-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07bbb-184">RELATED LINKS</span></span>

[<span data-ttu-id="07bbb-185">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="07bbb-185">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="07bbb-186">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="07bbb-186">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="07bbb-187">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="07bbb-187">Set-AzDnsRecordSet</span></span>](./Set-AzDnsRecordSet.md)

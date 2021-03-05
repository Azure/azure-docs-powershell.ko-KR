---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: 1ab2d10800648d04c9e8dcb2cf8907d426bd2d48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984741"
---
# <span data-ttu-id="f1ce7-101">Set-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f1ce7-101">Set-AzDnsRecordSet</span></span>

## <span data-ttu-id="f1ce7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="f1ce7-103">DNS 레코드 집합을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-103">Updates a DNS record set.</span></span>

## <span data-ttu-id="f1ce7-104">구문</span><span class="sxs-lookup"><span data-stu-id="f1ce7-104">SYNTAX</span></span>

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1ce7-105">설명</span><span class="sxs-lookup"><span data-stu-id="f1ce7-105">DESCRIPTION</span></span>
<span data-ttu-id="f1ce7-106">**Set-AzDnsRecordSet** cmdlet은 로컬 RecordSet 개체에서 Azure DNS 서비스에서 레코드 **집합을 업데이트합니다.**</span><span class="sxs-lookup"><span data-stu-id="f1ce7-106">The **Set-AzDnsRecordSet** cmdlet updates a record set in the Azure DNS service from a local **RecordSet** object.</span></span>
<span data-ttu-id="f1ce7-107">**RecordSet** 개체를 매개 변수로 전달하거나 파이프라인 연산자를 사용하여 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-107">You can pass a **RecordSet** object as a parameter or by using the pipeline operator.</span></span>
<span data-ttu-id="f1ce7-108">확인 매개  변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="f1ce7-109">로컬 **RecordSet** 개체를 검색한 후 Azure DNS에서 레코드 집합이 변경된 경우 레코드 집합이 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-109">The record set is not updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="f1ce7-110">이 기능은 동시 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-110">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="f1ce7-111">동시 변경 내용에  관계없이 레코드 집합을 업데이트하는 덮어 덮어 사용 매개 변수를 사용하여 이 동작을 억제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-111">You can suppress this behavior using the *Overwrite* parameter, which updates the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="f1ce7-112">예제</span><span class="sxs-lookup"><span data-stu-id="f1ce7-112">EXAMPLES</span></span>

### <span data-ttu-id="f1ce7-113">예제 1: 레코드 집합 업데이트</span><span class="sxs-lookup"><span data-stu-id="f1ce7-113">Example 1: Update a record set</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

<span data-ttu-id="f1ce7-114">첫 번째 명령은 Get-AzDnsRecordSet cmdlet을 사용하여 지정된 레코드 집합을 구한 다음 해당 $RecordSet 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-114">The first command uses the Get-AzDnsRecordSet cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="f1ce7-115">두 번째 및 세 번째 명령은 레코드 집합에 두 개의 A 레코드를 추가하는 오프라인 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-115">The second and third commands are off-line operations to add two A records to the record set.</span></span>
<span data-ttu-id="f1ce7-116">최종 명령은 **Set-AzDnsRecordSet** cmdlet을 사용하여 업데이트를 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-116">The final command uses the **Set-AzDnsRecordSet** cmdlet to commit the update.</span></span>

### <span data-ttu-id="f1ce7-117">예제 2: SOA 레코드 업데이트</span><span class="sxs-lookup"><span data-stu-id="f1ce7-117">Example 2: Update an SOA record</span></span>
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="f1ce7-118">첫 번째 명령은 **Get-AzDnsRecordset** cmdlet을 사용하여 지정된 레코드 집합을 구한 다음, 해당 레코드 집합을 $RecordSet 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-118">The first command uses the **Get-AzDnsRecordset** cmdlet to get the specified record set, and then stores it in the $RecordSet variable.</span></span>
<span data-ttu-id="f1ce7-119">두 번째 명령은 지정된 SOA 레코드를 $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-119">The second command updates the specified SOA record in $RecordSet.</span></span>
<span data-ttu-id="f1ce7-120">최종 명령은 **Set-AzDnsRecordSet** cmdlet을 사용하여 업데이트가 $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-120">The final command uses the **Set-AzDnsRecordSet** cmdlet to propagate the update in $RecordSet.</span></span>

## <span data-ttu-id="f1ce7-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f1ce7-121">PARAMETERS</span></span>

### <span data-ttu-id="f1ce7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1ce7-122">-DefaultProfile</span></span>
<span data-ttu-id="f1ce7-123">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f1ce7-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1ce7-124">-덮어 덮어 덮어 덮어 덮어</span><span class="sxs-lookup"><span data-stu-id="f1ce7-124">-Overwrite</span></span>
<span data-ttu-id="f1ce7-125">동시 변경 내용에 관계없이 레코드 집합을 업데이트하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-125">Indicates to update the record set regardless of concurrent changes.</span></span>
<span data-ttu-id="f1ce7-126">로컬 **RecordSet** 개체를 검색한 후 Azure DNS에서 레코드 집합이 변경된 경우 레코드 집합이 업데이트되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-126">The record set will not be updated if it has been changed in Azure DNS since the local **RecordSet** object was retrieved.</span></span>
<span data-ttu-id="f1ce7-127">이 기능은 동시 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-127">This provides protection for concurrent changes.</span></span>
<span data-ttu-id="f1ce7-128">이 동작을 억제하기 위해  덮어 덮어 사용 매개 변수를 사용할 수 있습니다. 따라서 레코드 집합이 동시 변경 내용에 관계없이 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-128">To suppress this behavior, you can use the *Overwrite* parameter, which results in the record set being updated regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="f1ce7-129">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="f1ce7-129">-RecordSet</span></span>
<span data-ttu-id="f1ce7-130">업데이트할 **RecordSet을** 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-130">Specifies the **RecordSet** to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1ce7-131">-확인</span><span class="sxs-lookup"><span data-stu-id="f1ce7-131">-Confirm</span></span>
<span data-ttu-id="f1ce7-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1ce7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1ce7-133">-WhatIf</span></span>
<span data-ttu-id="f1ce7-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1ce7-135">cmdlet이 실행되지 않습니다. cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1ce7-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1ce7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1ce7-137">CommonParameters</span></span>
<span data-ttu-id="f1ce7-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1ce7-139">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1ce7-140">입력</span><span class="sxs-lookup"><span data-stu-id="f1ce7-140">INPUTS</span></span>

### <span data-ttu-id="f1ce7-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f1ce7-141">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="f1ce7-142">출력</span><span class="sxs-lookup"><span data-stu-id="f1ce7-142">OUTPUTS</span></span>

### <span data-ttu-id="f1ce7-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f1ce7-143">Microsoft.Azure.Commands.Dns.DnsRecordSet</span></span>

## <span data-ttu-id="f1ce7-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1ce7-144">NOTES</span></span>
<span data-ttu-id="f1ce7-145">확인 매개  변수를 사용하여 이 cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-145">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="f1ce7-146">기본적으로 cmdlet은 $ConfirmPreference Windows PowerShell 값이 중간 또는 더 낮은지 확인하라는 메시지를 묻는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-146">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>
<span data-ttu-id="f1ce7-147">확인 또는 *확인:$True* 지정하는 경우 이 cmdlet은 실행하기 전에 확인을 묻는 메시지를 표시합니다. </span><span class="sxs-lookup"><span data-stu-id="f1ce7-147">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="f1ce7-148">*Confirm:$False* 지정하면 cmdlet에서 확인을 묻는 메시지가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1ce7-148">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="f1ce7-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1ce7-149">RELATED LINKS</span></span>

[<span data-ttu-id="f1ce7-150">Get-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f1ce7-150">Get-AzDnsRecordSet</span></span>](./Get-AzDnsRecordSet.md)

[<span data-ttu-id="f1ce7-151">New-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f1ce7-151">New-AzDnsRecordSet</span></span>](./New-AzDnsRecordSet.md)

[<span data-ttu-id="f1ce7-152">Remove-AzDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="f1ce7-152">Remove-AzDnsRecordSet</span></span>](./Remove-AzDnsRecordSet.md)

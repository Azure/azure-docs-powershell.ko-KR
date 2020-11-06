---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/remove-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/Remove-AzureRmDnsZone.md
ms.openlocfilehash: ac3f65ed82f9b04eb49e26a8cb03a3dcd8c9bc34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534832"
---
# <span data-ttu-id="2e7a9-101">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2e7a9-101">Remove-AzureRmDnsZone</span></span>

## <span data-ttu-id="2e7a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e7a9-102">SYNOPSIS</span></span>
<span data-ttu-id="2e7a9-103">리소스 그룹에서 DNS 영역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-103">Removes a DNS zone from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e7a9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2e7a9-104">SYNTAX</span></span>

### <span data-ttu-id="2e7a9-105">필드인</span><span class="sxs-lookup"><span data-stu-id="2e7a9-105">Fields</span></span>
```
Remove-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e7a9-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="2e7a9-106">Object</span></span>
```
Remove-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e7a9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2e7a9-107">DESCRIPTION</span></span>
<span data-ttu-id="2e7a9-108">**AzureRmDnsZone** cmdlet은 지정 된 리소스 그룹에서 DNS (Domain Name System) 영역을 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-108">The **Remove-AzureRmDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="2e7a9-109">영역에 포함 된 모든 레코드 집합도 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-109">All record sets contained in the zone are also deleted.</span></span>

<span data-ttu-id="2e7a9-110">*Name* 매개 변수를 사용 하거나 파이프라인 연산자를 사용 하 여 **DnsZone** 개체를 전달 하거나 *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>

<span data-ttu-id="2e7a9-111">확인 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

<span data-ttu-id="2e7a9-112">**DnsZone** 개체 (파이프라인 또는 *zone* 매개 변수를 통해 전달 됨)를 사용 하 여 영역을 지정 하는 경우에는 로컬 **DnsZone** 개체가 검색 된 이후 해당 영역이 Azure DNS에서 변경 되지 않습니다 (DNS 영역 리소스에서 직접 작업을 변경 하는 경우에만 해당 영역 내의 레코드 집합에 대 한 작업을 수행 하지 않음).</span><span class="sxs-lookup"><span data-stu-id="2e7a9-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="2e7a9-113">이는 동시 영역 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="2e7a9-114">이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며, 동시 변경 내용에 관계 없이 영역이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="2e7a9-115">예제의</span><span class="sxs-lookup"><span data-stu-id="2e7a9-115">EXAMPLES</span></span>

### <span data-ttu-id="2e7a9-116">예제 1: 영역 제거</span><span class="sxs-lookup"><span data-stu-id="2e7a9-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="2e7a9-117">이 명령은 MyResourceGroup 이라는 리소스 그룹에서 myzone.com 이라는 영역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="2e7a9-118">변수</span><span class="sxs-lookup"><span data-stu-id="2e7a9-118">PARAMETERS</span></span>

### <span data-ttu-id="2e7a9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e7a9-119">-DefaultProfile</span></span>
<span data-ttu-id="2e7a9-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2e7a9-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e7a9-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2e7a9-121">-Force</span></span>
<span data-ttu-id="2e7a9-122">이 매개 변수는이 cmdlet에 대해 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-122">This parameter is deprecated for this cmdlet.</span></span>
<span data-ttu-id="2e7a9-123">이후 릴리스에서 제거 될 것입니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-123">It will be removed in a future release.</span></span>

<span data-ttu-id="2e7a9-124">이 cmdlet이 확인을 묻는 메시지를 표시할지 여부를 제어 하려면 *Confirm* 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-124">To control whether this cmdlet prompts you for confirmation, use the *Confirm* parameter.</span></span>

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

### <span data-ttu-id="2e7a9-125">-이름</span><span class="sxs-lookup"><span data-stu-id="2e7a9-125">-Name</span></span>
<span data-ttu-id="2e7a9-126">이 cmdlet이 제거 하는 DNS 영역의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-126">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="2e7a9-127">또한 *ResourceGroupName* 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-127">You must also specify the *ResourceGroupName* parameter.</span></span>

<span data-ttu-id="2e7a9-128">또는 *zone* 매개 변수를 사용 하 여 DNS 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-128">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="2e7a9-129">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="2e7a9-129">-Overwrite</span></span>
<span data-ttu-id="2e7a9-130">**DnsZone** 개체 (파이프라인 또는 *zone* 매개 변수를 통해 전달 됨)를 사용 하 여 영역을 지정 하는 경우에는 로컬 **DnsZone** 개체가 검색 된 이후 해당 영역이 Azure DNS에서 변경 되지 않습니다 (DNS 영역 리소스에서 직접 작업을 변경 하는 경우에만 해당 영역 내의 레코드 집합에 대 한 작업을 수행 하지 않음).</span><span class="sxs-lookup"><span data-stu-id="2e7a9-130">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="2e7a9-131">이는 동시 영역 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-131">This provides protection for concurrent zone changes.</span></span>

<span data-ttu-id="2e7a9-132">이는 *덮어쓰기* 매개 변수를 사용 하 여 억제할 수 있으며, 동시 변경 내용에 관계 없이 영역이 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-132">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="2e7a9-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e7a9-133">-PassThru</span></span>
<span data-ttu-id="2e7a9-134">passthru</span><span class="sxs-lookup"><span data-stu-id="2e7a9-134">passthru</span></span>

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

### <span data-ttu-id="2e7a9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e7a9-135">-ResourceGroupName</span></span>
<span data-ttu-id="2e7a9-136">제거할 영역이 포함 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-136">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="2e7a9-137">*ZoneName* 매개 변수도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-137">You must also specify the *ZoneName* parameter.</span></span>

<span data-ttu-id="2e7a9-138">또는 파이프라인 또는 *zone* 매개 변수를 통해 전달 되는 **DnsZone** 개체를 사용 하 여 DNS 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-138">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="2e7a9-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="2e7a9-139">-Zone</span></span>
<span data-ttu-id="2e7a9-140">삭제할 DNS 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-140">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="2e7a9-141">**DnsZone** 개체는 파이프라인을 통해 전달할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-141">The **DnsZone** object passed can also be passed via the pipeline.</span></span>

<span data-ttu-id="2e7a9-142">또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용 하 여 삭제할 DNS 영역을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-142">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="2e7a9-143">-확인</span><span class="sxs-lookup"><span data-stu-id="2e7a9-143">-Confirm</span></span>
<span data-ttu-id="2e7a9-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e7a9-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e7a9-145">-WhatIf</span></span>
<span data-ttu-id="2e7a9-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e7a9-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e7a9-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e7a9-148">CommonParameters</span></span>
<span data-ttu-id="2e7a9-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e7a9-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e7a9-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e7a9-151">입력</span><span class="sxs-lookup"><span data-stu-id="2e7a9-151">INPUTS</span></span>

### <span data-ttu-id="2e7a9-152">DnsZone에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="2e7a9-152">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="2e7a9-153">**DnsZone** 개체를이 cmdlet에 파이프 하 여 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-153">You can pipe a **DnsZone** object to this cmdlet.</span></span>

## <span data-ttu-id="2e7a9-154">출력</span><span class="sxs-lookup"><span data-stu-id="2e7a9-154">OUTPUTS</span></span>

### <span data-ttu-id="2e7a9-155">않아야</span><span class="sxs-lookup"><span data-stu-id="2e7a9-155">None</span></span>
<span data-ttu-id="2e7a9-156">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-156">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="2e7a9-157">상속자</span><span class="sxs-lookup"><span data-stu-id="2e7a9-157">NOTES</span></span>
<span data-ttu-id="2e7a9-158">DNS 영역 삭제 시 발생할 가능성이 높은 영향으로 인해,이 cmdlet은 $ConfirmPreference Windows PowerShell 변수에 없음이 아닌 값이 있는 경우 확인을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-158">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>

<span data-ttu-id="2e7a9-159">*확인* 또는 *확인: $True* 를 지정 하는 경우이 cmdlet을 실행 하기 전에 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-159">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="2e7a9-160">*확인: $False* 를 지정 하면 cmdlet에서 확인을 요구 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e7a9-160">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="2e7a9-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e7a9-161">RELATED LINKS</span></span>

[<span data-ttu-id="2e7a9-162">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2e7a9-162">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="2e7a9-163">새로운 AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2e7a9-163">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="2e7a9-164">Set-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="2e7a9-164">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)

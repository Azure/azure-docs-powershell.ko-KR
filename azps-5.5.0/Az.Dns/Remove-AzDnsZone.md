---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 633a71788bb9578438053f7a296422e99e7c488e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180745"
---
# <span data-ttu-id="5a5d8-101">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="5a5d8-101">Remove-AzDnsZone</span></span>

## <span data-ttu-id="5a5d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a5d8-102">SYNOPSIS</span></span>
<span data-ttu-id="5a5d8-103">리소스 그룹에서 DNS 영역 제거</span><span class="sxs-lookup"><span data-stu-id="5a5d8-103">Removes a DNS zone from a resource group.</span></span>

## <span data-ttu-id="5a5d8-104">구문</span><span class="sxs-lookup"><span data-stu-id="5a5d8-104">SYNTAX</span></span>

### <span data-ttu-id="5a5d8-105">필드</span><span class="sxs-lookup"><span data-stu-id="5a5d8-105">Fields</span></span>
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a5d8-106">개체</span><span class="sxs-lookup"><span data-stu-id="5a5d8-106">Object</span></span>
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a5d8-107">설명</span><span class="sxs-lookup"><span data-stu-id="5a5d8-107">DESCRIPTION</span></span>
<span data-ttu-id="5a5d8-108">**Remove-AzDnsZone** cmdlet은 지정된 리소스 그룹에서 DNS(도메인 이름 시스템) 영역이 영구적으로 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-108">The **Remove-AzDnsZone** cmdlet permanently deletes a Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="5a5d8-109">영역 내에 포함된 모든 레코드 집합도 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-109">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="5a5d8-110">이름 매개 변수를 사용하여 또는  파이프라인 연산자를 사용하여 **DnsZone** 개체를 전달하거나 *ZoneName* 및 *ResourceGroupName* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-110">You can pass a **DnsZone** object using the *Name* parameter or by using the pipeline operator, or alternatively you can specify the *ZoneName* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="5a5d8-111">Confirm 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="5a5d8-112">**DnsZone** 개체를 사용하여 지역을 지정할 때(파이프라인 또는  영역 매개 변수를 통해 전달) 로컬 **DnsZone** 개체가 검색된 이후 Azure DNS에서 변경된 경우 영역이 삭제되지 않습니다(DNS 영역 리소스에 대한 직접 작업만 변경으로, 영역 내의 레코드 집합에 대한 작업은 수행되지 않습니다).</span><span class="sxs-lookup"><span data-stu-id="5a5d8-112">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="5a5d8-113">이렇게 하면 동시 영역 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-113">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="5a5d8-114">이는 동시 변경  내용에 관계없이 영역이 삭제되는 덮어 사용 매개 변수를 사용하여 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-114">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="5a5d8-115">예제</span><span class="sxs-lookup"><span data-stu-id="5a5d8-115">EXAMPLES</span></span>

### <span data-ttu-id="5a5d8-116">예제 1: 영역 제거</span><span class="sxs-lookup"><span data-stu-id="5a5d8-116">Example 1: Remove a zone</span></span>
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="5a5d8-117">이 명령은 MyResourceGroup이라는 myzone.com 그룹에서 이름이 지정되는 영역이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-117">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="5a5d8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a5d8-118">PARAMETERS</span></span>

### <span data-ttu-id="5a5d8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a5d8-119">-DefaultProfile</span></span>
<span data-ttu-id="5a5d8-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5a5d8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a5d8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5a5d8-121">-Name</span></span>
<span data-ttu-id="5a5d8-122">이 cmdlet이 제거하는 DNS 영역의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-122">Specifies the name of the DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="5a5d8-123">*ResourceGroupName 매개 변수도 지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-123">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="5a5d8-124">또는 영역 매개 변수를 사용하여 DNS 지역을 지정할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-124">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

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

### <span data-ttu-id="5a5d8-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="5a5d8-125">-Overwrite</span></span>
<span data-ttu-id="5a5d8-126">**DnsZone** 개체를 사용하여 지역을 지정할 때(파이프라인 또는  영역 매개 변수를 통해 전달) 로컬 **DnsZone** 개체가 검색된 이후 Azure DNS에서 변경된 경우 영역이 삭제되지 않습니다(DNS 영역 리소스에 대한 직접 작업만 변경으로, 영역 내의 레코드 집합에 대한 작업은 수행되지 않습니다).</span><span class="sxs-lookup"><span data-stu-id="5a5d8-126">When specifying the zone using a **DnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **DnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="5a5d8-127">이렇게 하면 동시 영역 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-127">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="5a5d8-128">이는 동시 변경  내용에 관계없이 영역이 삭제되는 덮어 사용 매개 변수를 사용하여 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-128">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

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

### <span data-ttu-id="5a5d8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a5d8-129">-PassThru</span></span>
<span data-ttu-id="5a5d8-130">passthru</span><span class="sxs-lookup"><span data-stu-id="5a5d8-130">passthru</span></span>

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

### <span data-ttu-id="5a5d8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a5d8-131">-ResourceGroupName</span></span>
<span data-ttu-id="5a5d8-132">제거할 영역이 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-132">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="5a5d8-133">*ZoneName 매개 변수도 지정해야* 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-133">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="5a5d8-134">또는 파이프라인 또는 영역 매개 변수를 통해 전달된 **DnsZone** 개체를 사용하여 DNS 지역을 지정할 *수* 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-134">Alternatively, you can specify the DNS zone using a **DnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

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

### <span data-ttu-id="5a5d8-135">-Zone</span><span class="sxs-lookup"><span data-stu-id="5a5d8-135">-Zone</span></span>
<span data-ttu-id="5a5d8-136">삭제할 DNS 영역이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-136">Specifies the DNS zone to delete.</span></span>
<span data-ttu-id="5a5d8-137">전달된 **DnsZone** 개체는 파이프라인을 통해 전달될 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-137">The **DnsZone** object passed can also be passed via the pipeline.</span></span>
<span data-ttu-id="5a5d8-138">또는 *ZoneName* 및 *ResourceGroupName* 매개 변수를 사용하여 삭제할 DNS 지역을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-138">Alternatively, you can specify the DNS zone to delete by using the *ZoneName* and *ResourceGroupName* parameters.</span></span>

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

### <span data-ttu-id="5a5d8-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a5d8-139">-Confirm</span></span>
<span data-ttu-id="5a5d8-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a5d8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a5d8-141">-WhatIf</span></span>
<span data-ttu-id="5a5d8-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5a5d8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a5d8-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a5d8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a5d8-144">CommonParameters</span></span>
<span data-ttu-id="5a5d8-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a5d8-146">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a5d8-147">입력</span><span class="sxs-lookup"><span data-stu-id="5a5d8-147">INPUTS</span></span>

### <span data-ttu-id="5a5d8-148">System.String</span><span class="sxs-lookup"><span data-stu-id="5a5d8-148">System.String</span></span>

### <span data-ttu-id="5a5d8-149">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="5a5d8-149">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="5a5d8-150">출력</span><span class="sxs-lookup"><span data-stu-id="5a5d8-150">OUTPUTS</span></span>

### <span data-ttu-id="5a5d8-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5a5d8-151">System.Boolean</span></span>

## <span data-ttu-id="5a5d8-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5a5d8-152">NOTES</span></span>
<span data-ttu-id="5a5d8-153">DNS 영역 삭제의 잠재적으로 높은 영향으로 인해 기본적으로 이 cmdlet은 $ConfirmPreference Windows PowerShell 값이 None이면 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-153">Due to the potentially high impact of deleting a DNS zone, by default, this cmdlet prompts for confirmation if the $ConfirmPreference Windows PowerShell variable has any value other than None.</span></span>
<span data-ttu-id="5a5d8-154">*Confirm* 또는 *Confirm:$True* 지정하는 경우 이 cmdlet은 실행 전에 확인을 요청하는 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-154">If you specify *Confirm* or *Confirm:$True*, this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="5a5d8-155">*Confirm:$False* 지정하면 cmdlet에서 확인 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5a5d8-155">If you specify *Confirm:$False*, the cmdlet does not prompt you for confirmation.</span></span> 

## <span data-ttu-id="5a5d8-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a5d8-156">RELATED LINKS</span></span>

[<span data-ttu-id="5a5d8-157">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="5a5d8-157">Get-AzDnsZone</span></span>](./Get-AzDnsZone.md)

[<span data-ttu-id="5a5d8-158">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="5a5d8-158">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="5a5d8-159">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="5a5d8-159">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)

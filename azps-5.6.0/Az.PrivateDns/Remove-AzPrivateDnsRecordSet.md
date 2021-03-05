---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: d54b2952c617782ec30193372b430785c0a8b79d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965579"
---
# <span data-ttu-id="2ef7a-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2ef7a-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="2ef7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ef7a-102">SYNOPSIS</span></span>
<span data-ttu-id="2ef7a-103">개인 DNS 영역의 레코드 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="2ef7a-104">구문</span><span class="sxs-lookup"><span data-stu-id="2ef7a-104">SYNTAX</span></span>

### <span data-ttu-id="2ef7a-105">필드(기본값)</span><span class="sxs-lookup"><span data-stu-id="2ef7a-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ef7a-106">혼합</span><span class="sxs-lookup"><span data-stu-id="2ef7a-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ef7a-107">개체</span><span class="sxs-lookup"><span data-stu-id="2ef7a-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ef7a-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ef7a-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ef7a-109">설명</span><span class="sxs-lookup"><span data-stu-id="2ef7a-109">DESCRIPTION</span></span>
<span data-ttu-id="2ef7a-110">Remove-AzPrivateDnsRecordSet cmdlet은 지정된 영역의 지정된 레코드 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="2ef7a-111">개인 영역 정수에서 자동으로 생성된 SOA 레코드는 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="2ef7a-112">파이프라인 연산자 또는 매개 변수 또는 ResourceId로 사용하여 RecordSet 개체를 이 cmdlet에 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="2ef7a-113">RecordSet 개체를 사용하지 않고 이름으로 설정된 레코드를 식별하고 입력하려면 파이프라인 연산자 또는 매개 변수로 또는 ZoneName 및 ResourceGroupName 매개 변수를 지정하여 이 cmdlet에 PSPrivateDnsZone 개체로 구역을 전달해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="2ef7a-114">확인 매개 변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="2ef7a-115">RecordSet 개체를 사용하여 레코드 집합을 지정할 때 로컬 RecordSet 개체를 검색한 후 Azure Private DNS에서 레코드 집합이 변경된 경우 레코드 집합이 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="2ef7a-116">이 기능은 동시 변경에 대한 보호를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="2ef7a-117">덮어 덮어 사용 매개 변수를 사용하여 이 기능을 억제할 수 있습니다. 이는 동시 변경 내용에 관계없이 레코드 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="2ef7a-118">예제</span><span class="sxs-lookup"><span data-stu-id="2ef7a-118">EXAMPLES</span></span>

### <span data-ttu-id="2ef7a-119">예제 1: 레코드 집합 제거</span><span class="sxs-lookup"><span data-stu-id="2ef7a-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="2ef7a-120">첫 번째 명령은 지정된 레코드 집합을 얻은 다음, 해당 레코드 집합을 $RecordSet 변수에 저장합니다. 두 번째 명령은 레코드 집합을 $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="2ef7a-121">예제 2: 레코드 집합을 제거하고 모든 확인을 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="2ef7a-122">첫 번째 명령은 지정된 레코드 집합을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-122">The first command gets the specified record set.</span></span> <span data-ttu-id="2ef7a-123">두 번째 명령은 레코드 집합이 그동안 변경된 경우에도 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="2ef7a-124">확인 프롬프트가 억제됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="2ef7a-125">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2ef7a-125">PARAMETERS</span></span>

### <span data-ttu-id="2ef7a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ef7a-126">-DefaultProfile</span></span>
<span data-ttu-id="2ef7a-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ef7a-128">-Name</span><span class="sxs-lookup"><span data-stu-id="2ef7a-128">-Name</span></span>
<span data-ttu-id="2ef7a-129">레코드 집합의 레코드 이름(영역의 이름과 종료점 없이)입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="2ef7a-130">-덮어 덮어 덮어 덮어 덮어</span><span class="sxs-lookup"><span data-stu-id="2ef7a-130">-Overwrite</span></span>
<span data-ttu-id="2ef7a-131">낙관적 동시성 검사를 위해 RecordSet 매개 변수의 ETag 필드를 사용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="2ef7a-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2ef7a-132">-PassThru</span></span>
<span data-ttu-id="2ef7a-133">작업의 결과(부울)를 전달하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="2ef7a-134">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="2ef7a-134">-RecordSet</span></span>
<span data-ttu-id="2ef7a-135">레코드를 추가할 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-135">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ef7a-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="2ef7a-136">-RecordType</span></span>
<span data-ttu-id="2ef7a-137">레코드 집합의 개인 DNS 레코드 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-137">The type of Private DNS records in the record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ef7a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ef7a-138">-ResourceGroupName</span></span>
<span data-ttu-id="2ef7a-139">영역이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-139">The resource group to which the zone belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ef7a-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ef7a-140">-ResourceId</span></span>
<span data-ttu-id="2ef7a-141">개인 DNS RecordSet ResourceID.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-141">Private DNS RecordSet ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ef7a-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="2ef7a-142">-Zone</span></span>
<span data-ttu-id="2ef7a-143">레코드 집합을 만들 영역의 개인DnsZone 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ef7a-144">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="2ef7a-144">-ZoneName</span></span>
<span data-ttu-id="2ef7a-145">레코드 집합이 있는 영역(종료점 없이).</span><span class="sxs-lookup"><span data-stu-id="2ef7a-145">The zone in which the record set exists (without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ef7a-146">-확인</span><span class="sxs-lookup"><span data-stu-id="2ef7a-146">-Confirm</span></span>
<span data-ttu-id="2ef7a-147">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ef7a-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ef7a-148">-WhatIf</span></span>
<span data-ttu-id="2ef7a-149">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ef7a-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ef7a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ef7a-151">CommonParameters</span></span>
<span data-ttu-id="2ef7a-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ef7a-153">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2ef7a-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ef7a-154">입력</span><span class="sxs-lookup"><span data-stu-id="2ef7a-154">INPUTS</span></span>

### <span data-ttu-id="2ef7a-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="2ef7a-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="2ef7a-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="2ef7a-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="2ef7a-157">System.String</span><span class="sxs-lookup"><span data-stu-id="2ef7a-157">System.String</span></span>

## <span data-ttu-id="2ef7a-158">출력</span><span class="sxs-lookup"><span data-stu-id="2ef7a-158">OUTPUTS</span></span>

### <span data-ttu-id="2ef7a-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2ef7a-159">System.Boolean</span></span>

## <span data-ttu-id="2ef7a-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2ef7a-160">NOTES</span></span>

## <span data-ttu-id="2ef7a-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ef7a-161">RELATED LINKS</span></span>

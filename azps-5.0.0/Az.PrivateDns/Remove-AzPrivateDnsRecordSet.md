---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 865ab4ab3cca9d921fc8c40e9c6ae5cd03eaf00a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311168"
---
# <span data-ttu-id="9b760-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="9b760-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="9b760-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b760-102">SYNOPSIS</span></span>
<span data-ttu-id="9b760-103">개인 DNS 영역에서 레코드 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="9b760-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b760-104">SYNTAX</span></span>

### <span data-ttu-id="9b760-105">필드 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9b760-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b760-106">섞여</span><span class="sxs-lookup"><span data-stu-id="9b760-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b760-107">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="9b760-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b760-108">리소스</span><span class="sxs-lookup"><span data-stu-id="9b760-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b760-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9b760-109">DESCRIPTION</span></span>
<span data-ttu-id="9b760-110">Remove-AzPrivateDnsRecordSet cmdlet은 지정 된 영역에서 지정 된 레코드 집합을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="9b760-111">개인 영역 apex에서 자동으로 만들어지는 SOA 레코드는 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="9b760-112">파이프라인 연산자나 매개 변수 또는 ResourceId로 사용 하 여 레코드 집합 개체를이 cmdlet에 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="9b760-113">레코드 집합 개체를 사용 하지 않고 이름 및 형식을 기준으로 하 여 변수를 확인 하려면 파이프라인 연산자 또는 매개 변수를 사용 하 여이 cmdlet에 PSPrivateDnsZone 개체로 영역을 전달 하거나 ZoneName 및 ResourceGroupName 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="9b760-114">확인 매개 변수를 사용 하 여 Windows PowerShell 변수를 $ConfirmPreference 하 여 cmdlet에서 확인을 묻는 메시지를 표시할지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="9b760-115">RecordSet 개체를 사용 하 여 레코드 집합을 지정 하는 경우 로컬 RecordSet 개체를 검색 한 후 Azure Private DNS에서 레코드 집합이 변경 되 면 삭제 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="9b760-116">이는 동시 변경에 대 한 보호를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="9b760-117">동시 변경 내용에 관계 없이 레코드 집합을 삭제 하는 Overwrite 매개 변수를 사용 하 여이를 억제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="9b760-118">예제의</span><span class="sxs-lookup"><span data-stu-id="9b760-118">EXAMPLES</span></span>

### <span data-ttu-id="9b760-119">예제 1: 레코드 집합 제거</span><span class="sxs-lookup"><span data-stu-id="9b760-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="9b760-120">첫 번째 명령은 지정 된 레코드 집합을 가져온 다음 $RecordSet 변수에 저장 합니다. 두 번째 명령은 $RecordSet에 설정 된 레코드를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="9b760-121">예제 2: 레코드 집합 제거 및 모든 확인 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="9b760-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="9b760-122">첫 번째 명령은 지정 된 레코드 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-122">The first command gets the specified record set.</span></span> <span data-ttu-id="9b760-123">두 번째 명령은 레코드 집합을 삭제 했지만 그 동안에는 레코드가 변경 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="9b760-124">확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="9b760-125">변수</span><span class="sxs-lookup"><span data-stu-id="9b760-125">PARAMETERS</span></span>

### <span data-ttu-id="9b760-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b760-126">-DefaultProfile</span></span>
<span data-ttu-id="9b760-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b760-128">-이름</span><span class="sxs-lookup"><span data-stu-id="9b760-128">-Name</span></span>
<span data-ttu-id="9b760-129">레코드 집합의 레코드 이름 (영역의 이름과 종료 점이 없는 위치)을 기준으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="9b760-130">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="9b760-130">-Overwrite</span></span>
<span data-ttu-id="9b760-131">낙관적 동시성 검사에 레코드 집합 매개 변수의 ETag 필드를 사용 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="9b760-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="9b760-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b760-132">-PassThru</span></span>
<span data-ttu-id="9b760-133">작업의 결과 (부울)를 전달 하는 데 사용 됩니다. 파이프라인에서 개인 영역 삭제</span><span class="sxs-lookup"><span data-stu-id="9b760-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="9b760-134">-레코드 집합</span><span class="sxs-lookup"><span data-stu-id="9b760-134">-RecordSet</span></span>
<span data-ttu-id="9b760-135">레코드를 추가할 레코드 집합입니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-135">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="9b760-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="9b760-136">-RecordType</span></span>
<span data-ttu-id="9b760-137">레코드 집합의 개인 DNS 레코드 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-137">The type of Private DNS records in the record set.</span></span>

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

### <span data-ttu-id="9b760-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b760-138">-ResourceGroupName</span></span>
<span data-ttu-id="9b760-139">영역이 속해 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-139">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="9b760-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b760-140">-ResourceId</span></span>
<span data-ttu-id="9b760-141">개인 DNS 레코드 집합 ResourceID입니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-141">Private DNS RecordSet ResourceID.</span></span>

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

### <span data-ttu-id="9b760-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="9b760-142">-Zone</span></span>
<span data-ttu-id="9b760-143">레코드 집합을 만들 영역을 나타내는 PrivateDnsZone 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="9b760-144">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="9b760-144">-ZoneName</span></span>
<span data-ttu-id="9b760-145">레코드 집합이 존재 하는 영역 (종료 점이 없음)입니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-145">The zone in which the record set exists (without a terminating dot).</span></span>

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

### <span data-ttu-id="9b760-146">-확인</span><span class="sxs-lookup"><span data-stu-id="9b760-146">-Confirm</span></span>
<span data-ttu-id="9b760-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b760-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b760-148">-WhatIf</span></span>
<span data-ttu-id="9b760-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b760-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b760-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b760-151">CommonParameters</span></span>
<span data-ttu-id="9b760-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b760-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b760-153">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b760-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b760-154">입력</span><span class="sxs-lookup"><span data-stu-id="9b760-154">INPUTS</span></span>

### <span data-ttu-id="9b760-155">PrivateDns. PSPrivateDnsZone/.</span><span class="sxs-lookup"><span data-stu-id="9b760-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="9b760-156">PrivateDns. PSPrivateDnsRecordSet/.</span><span class="sxs-lookup"><span data-stu-id="9b760-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="9b760-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9b760-157">System.String</span></span>

## <span data-ttu-id="9b760-158">출력</span><span class="sxs-lookup"><span data-stu-id="9b760-158">OUTPUTS</span></span>

### <span data-ttu-id="9b760-159">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9b760-159">System.Boolean</span></span>

## <span data-ttu-id="9b760-160">상속자</span><span class="sxs-lookup"><span data-stu-id="9b760-160">NOTES</span></span>

## <span data-ttu-id="9b760-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b760-161">RELATED LINKS</span></span>

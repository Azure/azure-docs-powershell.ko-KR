---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/new-azsippool
schema: 2.0.0
ms.openlocfilehash: 2b04c5c1eb4d0a2b79543bf81bbfc02d1f0fb4ad
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876061"
---
# <span data-ttu-id="1f77a-101">New-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="1f77a-101">New-AzsIPPool</span></span>

## <span data-ttu-id="1f77a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f77a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f77a-103">IP 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-103">Create an IP pool.</span></span>
<span data-ttu-id="1f77a-104">만든 후에는 IP 풀을 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-104">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="1f77a-105">구문과</span><span class="sxs-lookup"><span data-stu-id="1f77a-105">SYNTAX</span></span>

### <span data-ttu-id="1f77a-106">CreateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="1f77a-106">CreateExpanded (Default)</span></span>
```
New-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AddressPrefix <String>] [-EndIPAddress <String>]
 [-NumberOfAllocatedIPAddress <Int64>] [-NumberOfIPAddress <Int64>] [-NumberOfIPAddressesInTransition <Int64>]
 [-StartIPAddress <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1f77a-107">만드는</span><span class="sxs-lookup"><span data-stu-id="1f77a-107">Create</span></span>
```
New-AzsIPPool -Name <String> -Pool <IIPPool> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1f77a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1f77a-108">DESCRIPTION</span></span>
<span data-ttu-id="1f77a-109">IP 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-109">Create an IP pool.</span></span>
<span data-ttu-id="1f77a-110">만든 후에는 IP 풀을 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-110">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="1f77a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1f77a-111">EXAMPLES</span></span>

### <span data-ttu-id="1f77a-112">예제 1:</span><span class="sxs-lookup"><span data-stu-id="1f77a-112">Example 1:</span></span>
```powershell
PS C:\> New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24

```

<span data-ttu-id="1f77a-113">새 IP 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-113">Create a new IP pool.</span></span>



## <span data-ttu-id="1f77a-114">변수</span><span class="sxs-lookup"><span data-stu-id="1f77a-114">PARAMETERS</span></span>

### <span data-ttu-id="1f77a-115">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1f77a-115">-AddressPrefix</span></span>
<span data-ttu-id="1f77a-116">주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-116">The address prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f77a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f77a-117">-AsJob</span></span>
<span data-ttu-id="1f77a-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="1f77a-118">Run the command as a job</span></span>

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

### <span data-ttu-id="1f77a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f77a-119">-DefaultProfile</span></span>
<span data-ttu-id="1f77a-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f77a-121">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="1f77a-121">-EndIPAddress</span></span>
<span data-ttu-id="1f77a-122">끝 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-122">The ending IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f77a-123">-위치</span><span class="sxs-lookup"><span data-stu-id="1f77a-123">-Location</span></span>
<span data-ttu-id="1f77a-124">리소스가 있는 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-124">The region where the resource is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f77a-125">-이름</span><span class="sxs-lookup"><span data-stu-id="1f77a-125">-Name</span></span>
<span data-ttu-id="1f77a-126">IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-126">IP pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f77a-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1f77a-127">-NoWait</span></span>
<span data-ttu-id="1f77a-128">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="1f77a-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1f77a-129">-NumberOfAllocatedIPAddress</span><span class="sxs-lookup"><span data-stu-id="1f77a-129">-NumberOfAllocatedIPAddress</span></span>
<span data-ttu-id="1f77a-130">현재 할당 된 IP 주소의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-130">The number of currently allocated IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f77a-131">-NumberOfIPAddress</span><span class="sxs-lookup"><span data-stu-id="1f77a-131">-NumberOfIPAddress</span></span>
<span data-ttu-id="1f77a-132">IP 주소의 총 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-132">The total number of IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f77a-133">-NumberOfIPAddressesInTransition</span><span class="sxs-lookup"><span data-stu-id="1f77a-133">-NumberOfIPAddressesInTransition</span></span>
<span data-ttu-id="1f77a-134">전환 중인 IP 주소의 현재 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-134">The current number of IP addresses in transition.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f77a-135">-풀</span><span class="sxs-lookup"><span data-stu-id="1f77a-135">-Pool</span></span>
<span data-ttu-id="1f77a-136">이 리소스는 서브넷 내의 노드에 대해 주소가 할당 되는 IP 주소 범위를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-136">This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
<span data-ttu-id="1f77a-137">생성 하려면 풀 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-137">To construct, see NOTES section for POOL properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1f77a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f77a-138">-ResourceGroupName</span></span>
<span data-ttu-id="1f77a-139">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-139">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f77a-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="1f77a-140">-StartIPAddress</span></span>
<span data-ttu-id="1f77a-141">시작 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-141">The starting IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f77a-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f77a-142">-SubscriptionId</span></span>
<span data-ttu-id="1f77a-143">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1f77a-144">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f77a-145">태그</span><span class="sxs-lookup"><span data-stu-id="1f77a-145">-Tag</span></span>
<span data-ttu-id="1f77a-146">키-값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-146">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1f77a-147">-확인</span><span class="sxs-lookup"><span data-stu-id="1f77a-147">-Confirm</span></span>
<span data-ttu-id="1f77a-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f77a-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f77a-149">-WhatIf</span></span>
<span data-ttu-id="1f77a-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f77a-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f77a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f77a-152">CommonParameters</span></span>
<span data-ttu-id="1f77a-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f77a-154">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f77a-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f77a-155">입력</span><span class="sxs-lookup"><span data-stu-id="1f77a-155">INPUTS</span></span>

### <span data-ttu-id="1f77a-156">FabricAdmin. PowerShell. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="1f77a-156">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>

## <span data-ttu-id="1f77a-157">출력</span><span class="sxs-lookup"><span data-stu-id="1f77a-157">OUTPUTS</span></span>

### <span data-ttu-id="1f77a-158">FabricAdmin. PowerShell. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="1f77a-158">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="1f77a-159">상속자</span><span class="sxs-lookup"><span data-stu-id="1f77a-159">NOTES</span></span>

<span data-ttu-id="1f77a-160">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-160">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1f77a-161">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f77a-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1f77a-162">풀 <IIPPool> :이 리소스는 서브넷 내의 노드에 대해 주소가 할당 되는 IP 주소 범위를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-162">POOL <IIPPool>: This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
  - <span data-ttu-id="1f77a-163">`[Location <String>]`: 리소스가 있는 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-163">`[Location <String>]`: The region where the resource is located.</span></span>
  - <span data-ttu-id="1f77a-164">`[Tag <IResourceTags>]`: 키-값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-164">`[Tag <IResourceTags>]`: List of key-value pairs.</span></span>
    - <span data-ttu-id="1f77a-165">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-165">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="1f77a-166">`[AddressPrefix <String>]`: 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-166">`[AddressPrefix <String>]`: The address prefix.</span></span>
  - <span data-ttu-id="1f77a-167">`[EndIPAddress <String>]`: 종료 IP 주소</span><span class="sxs-lookup"><span data-stu-id="1f77a-167">`[EndIPAddress <String>]`: The ending IP address.</span></span>
  - <span data-ttu-id="1f77a-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: 현재 할당 된 IP 주소의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: The number of currently allocated IP addresses.</span></span>
  - <span data-ttu-id="1f77a-169">`[NumberOfIPAddresses <Int64?>]`: IP 주소의 총 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-169">`[NumberOfIPAddresses <Int64?>]`: The total number of IP addresses.</span></span>
  - <span data-ttu-id="1f77a-170">`[NumberOfIPAddressesInTransition <Int64?>]`: 전환 중인 IP 주소의 현재 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1f77a-170">`[NumberOfIPAddressesInTransition <Int64?>]`: The current number of IP addresses in transition.</span></span>
  - <span data-ttu-id="1f77a-171">`[StartIPAddress <String>]`: 시작 IP 주소</span><span class="sxs-lookup"><span data-stu-id="1f77a-171">`[StartIPAddress <String>]`: The starting IP address.</span></span>

## <span data-ttu-id="1f77a-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f77a-172">RELATED LINKS</span></span>


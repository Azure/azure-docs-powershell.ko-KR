---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 715234586df8383a2983b4f0459ae91ca457d684
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045368"
---
# <span data-ttu-id="75e80-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="75e80-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="75e80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75e80-102">SYNOPSIS</span></span>
<span data-ttu-id="75e80-103">기존 계산 할당량을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-103">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="75e80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75e80-104">SYNTAX</span></span>

### <span data-ttu-id="75e80-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="75e80-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="75e80-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="75e80-106">DeleteViaIdentity</span></span>
```
Remove-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="75e80-107">설명은</span><span class="sxs-lookup"><span data-stu-id="75e80-107">DESCRIPTION</span></span>
<span data-ttu-id="75e80-108">기존 계산 할당량을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-108">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="75e80-109">예제의</span><span class="sxs-lookup"><span data-stu-id="75e80-109">EXAMPLES</span></span>

### <span data-ttu-id="75e80-110">예제 1: 계산 할당량 제거</span><span class="sxs-lookup"><span data-stu-id="75e80-110">Example 1: Remove a Compute Quota</span></span>
```powershell
PS C:\> Remove-AzsComputeQuota -Name "AComputeQuota"
```

<span data-ttu-id="75e80-111">계산 할당량을 제거 하기 위해 성공적으로 호출 하면 출력이 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-111">A successful call to remove a compute quota will not return any output</span></span>

## <span data-ttu-id="75e80-112">변수</span><span class="sxs-lookup"><span data-stu-id="75e80-112">PARAMETERS</span></span>

### <span data-ttu-id="75e80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75e80-113">-DefaultProfile</span></span>
<span data-ttu-id="75e80-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75e80-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75e80-115">-InputObject</span></span>
<span data-ttu-id="75e80-116">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="75e80-117">-위치</span><span class="sxs-lookup"><span data-stu-id="75e80-117">-Location</span></span>
<span data-ttu-id="75e80-118">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-118">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75e80-119">-이름</span><span class="sxs-lookup"><span data-stu-id="75e80-119">-Name</span></span>
<span data-ttu-id="75e80-120">할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-120">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75e80-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75e80-121">-PassThru</span></span>
<span data-ttu-id="75e80-122">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="75e80-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75e80-123">-SubscriptionId</span></span>
<span data-ttu-id="75e80-124">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-124">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="75e80-125">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75e80-126">-확인</span><span class="sxs-lookup"><span data-stu-id="75e80-126">-Confirm</span></span>
<span data-ttu-id="75e80-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75e80-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75e80-128">-WhatIf</span></span>
<span data-ttu-id="75e80-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75e80-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75e80-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e80-131">CommonParameters</span></span>
<span data-ttu-id="75e80-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75e80-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="75e80-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e80-134">입력</span><span class="sxs-lookup"><span data-stu-id="75e80-134">INPUTS</span></span>

### <span data-ttu-id="75e80-135">IComputeAdminIdentity (Microsoft. PowerShell. t t t)</span><span class="sxs-lookup"><span data-stu-id="75e80-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="75e80-136">출력</span><span class="sxs-lookup"><span data-stu-id="75e80-136">OUTPUTS</span></span>

### <span data-ttu-id="75e80-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="75e80-137">System.Boolean</span></span>



## <span data-ttu-id="75e80-138">상속자</span><span class="sxs-lookup"><span data-stu-id="75e80-138">NOTES</span></span>

<span data-ttu-id="75e80-139">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="75e80-140">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="75e80-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="75e80-141">INPUTOBJECT <IComputeAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="75e80-141">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="75e80-142">`[DiskId <String>]`: 디스크 guid를 id로 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-142">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="75e80-143">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="75e80-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="75e80-144">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="75e80-145">`[MigrationId <String>]`: 마이그레이션 작업 guid 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-145">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="75e80-146">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-146">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="75e80-147">`[Publisher <String>]`: 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-147">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="75e80-148">`[QuotaName <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-148">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="75e80-149">`[Sku <String>]`: SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-149">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="75e80-150">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-150">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="75e80-151">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="75e80-152">`[Type <String>]`: 확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-152">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="75e80-153">`[Version <String>]`: 리소스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="75e80-153">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="75e80-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75e80-154">RELATED LINKS</span></span>


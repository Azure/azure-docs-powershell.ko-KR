---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsvmextension
schema: 2.0.0
ms.openlocfilehash: 0b2bca9555b14a391df69acc4abdb2fc8c95017c
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045366"
---
# <span data-ttu-id="afd69-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="afd69-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="afd69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afd69-102">SYNOPSIS</span></span>
<span data-ttu-id="afd69-103">지정 된 가상 컴퓨터 확장 이미지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-103">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="afd69-104">구문과</span><span class="sxs-lookup"><span data-stu-id="afd69-104">SYNTAX</span></span>

### <span data-ttu-id="afd69-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="afd69-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="afd69-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="afd69-106">DeleteViaIdentity</span></span>
```
Remove-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="afd69-107">설명은</span><span class="sxs-lookup"><span data-stu-id="afd69-107">DESCRIPTION</span></span>
<span data-ttu-id="afd69-108">지정 된 가상 컴퓨터 확장 이미지를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-108">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="afd69-109">예제의</span><span class="sxs-lookup"><span data-stu-id="afd69-109">EXAMPLES</span></span>

### <span data-ttu-id="afd69-110">예제 1: 존재 하는 VM 확장 제거</span><span class="sxs-lookup"><span data-stu-id="afd69-110">Example 1: Remove a VM Extension that Exists</span></span> 
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type MicroExtension -Version 0.1.0
```

<span data-ttu-id="afd69-111">계산 할당량을 제거 하기 위해 성공적으로 호출 하면 출력이 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-111">A successful call to remove a compute quota will not return any output</span></span>

### <span data-ttu-id="afd69-112">예제 2: 존재 하지 않는 VM 확장 제거</span><span class="sxs-lookup"><span data-stu-id="afd69-112">Example 2: Remove a VM Extension that Does Not Exist</span></span>
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type DoesntExist -Version 9.8.7
```

<span data-ttu-id="afd69-113">존재 하지 않는 플랫폼 이미지를 제거 하기 위해 성공적으로 호출 하면 출력이 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="afd69-114">변수</span><span class="sxs-lookup"><span data-stu-id="afd69-114">PARAMETERS</span></span>

### <span data-ttu-id="afd69-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd69-115">-DefaultProfile</span></span>
<span data-ttu-id="afd69-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afd69-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afd69-117">-InputObject</span></span>
<span data-ttu-id="afd69-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="afd69-119">-위치</span><span class="sxs-lookup"><span data-stu-id="afd69-119">-Location</span></span>
<span data-ttu-id="afd69-120">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-120">Location of the resource.</span></span>

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

### <span data-ttu-id="afd69-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afd69-121">-PassThru</span></span>
<span data-ttu-id="afd69-122">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="afd69-123">-Publisher</span><span class="sxs-lookup"><span data-stu-id="afd69-123">-Publisher</span></span>
<span data-ttu-id="afd69-124">게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-124">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="afd69-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="afd69-125">-SubscriptionId</span></span>
<span data-ttu-id="afd69-126">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="afd69-127">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="afd69-128">-Type</span><span class="sxs-lookup"><span data-stu-id="afd69-128">-Type</span></span>
<span data-ttu-id="afd69-129">확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-129">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="afd69-130">-버전</span><span class="sxs-lookup"><span data-stu-id="afd69-130">-Version</span></span>
<span data-ttu-id="afd69-131">리소스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-131">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="afd69-132">-확인</span><span class="sxs-lookup"><span data-stu-id="afd69-132">-Confirm</span></span>
<span data-ttu-id="afd69-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afd69-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afd69-134">-WhatIf</span></span>
<span data-ttu-id="afd69-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afd69-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afd69-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd69-137">CommonParameters</span></span>
<span data-ttu-id="afd69-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd69-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="afd69-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd69-140">입력</span><span class="sxs-lookup"><span data-stu-id="afd69-140">INPUTS</span></span>

### <span data-ttu-id="afd69-141">IComputeAdminIdentity (Microsoft. PowerShell. t t t)</span><span class="sxs-lookup"><span data-stu-id="afd69-141">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="afd69-142">출력</span><span class="sxs-lookup"><span data-stu-id="afd69-142">OUTPUTS</span></span>

### <span data-ttu-id="afd69-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="afd69-143">System.Boolean</span></span>



## <span data-ttu-id="afd69-144">상속자</span><span class="sxs-lookup"><span data-stu-id="afd69-144">NOTES</span></span>

<span data-ttu-id="afd69-145">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="afd69-146">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="afd69-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="afd69-147">INPUTOBJECT <IComputeAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="afd69-147">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="afd69-148">`[DiskId <String>]`: 디스크 guid를 id로 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-148">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="afd69-149">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="afd69-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="afd69-150">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-150">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="afd69-151">`[MigrationId <String>]`: 마이그레이션 작업 guid 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-151">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="afd69-152">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-152">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="afd69-153">`[Publisher <String>]`: 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-153">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="afd69-154">`[QuotaName <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-154">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="afd69-155">`[Sku <String>]`: SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-155">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="afd69-156">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-156">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="afd69-157">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="afd69-158">`[Type <String>]`: 확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-158">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="afd69-159">`[Version <String>]`: 리소스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="afd69-159">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="afd69-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="afd69-160">RELATED LINKS</span></span>


---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: ae4fc80c54aedf7f35ebfc6c0c5f16bb2e5028ee
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046727"
---
# <span data-ttu-id="6b89a-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="6b89a-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="6b89a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b89a-102">SYNOPSIS</span></span>
<span data-ttu-id="6b89a-103">플랫폼 이미지 삭제</span><span class="sxs-lookup"><span data-stu-id="6b89a-103">Delete a platform image</span></span>

## <span data-ttu-id="6b89a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6b89a-104">SYNTAX</span></span>

### <span data-ttu-id="6b89a-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6b89a-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="6b89a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6b89a-106">DeleteViaIdentity</span></span>
```
Remove-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6b89a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6b89a-107">DESCRIPTION</span></span>
<span data-ttu-id="6b89a-108">플랫폼 이미지 삭제</span><span class="sxs-lookup"><span data-stu-id="6b89a-108">Delete a platform image</span></span>

## <span data-ttu-id="6b89a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6b89a-109">EXAMPLES</span></span>

### <span data-ttu-id="6b89a-110">예제 1: 플랫폼 이미지 제거</span><span class="sxs-lookup"><span data-stu-id="6b89a-110">Example 1: Remove a Platform Image</span></span>
```powershell
PS C:\>Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.0.0
```

<span data-ttu-id="6b89a-111">플랫폼 이미지 제거를 성공적으로 호출 하면 출력이 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-111">A successful call to remove a platform image will not return any output</span></span>

### <span data-ttu-id="6b89a-112">예제 2: 플랫폼 이미지 제거 없음</span><span class="sxs-lookup"><span data-stu-id="6b89a-112">Example 2: Remove a Platform Image the Does Not Exist</span></span>
```powershell
PS C:\>  Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.1.6

```

<span data-ttu-id="6b89a-113">존재 하지 않는 플랫폼 이미지를 제거 하기 위해 성공적으로 호출 하면 출력이 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="6b89a-114">변수</span><span class="sxs-lookup"><span data-stu-id="6b89a-114">PARAMETERS</span></span>

### <span data-ttu-id="6b89a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b89a-115">-DefaultProfile</span></span>
<span data-ttu-id="6b89a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b89a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b89a-117">-InputObject</span></span>
<span data-ttu-id="6b89a-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6b89a-119">-위치</span><span class="sxs-lookup"><span data-stu-id="6b89a-119">-Location</span></span>
<span data-ttu-id="6b89a-120">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-120">Location of the resource.</span></span>

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

### <span data-ttu-id="6b89a-121">-제공</span><span class="sxs-lookup"><span data-stu-id="6b89a-121">-Offer</span></span>
<span data-ttu-id="6b89a-122">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-122">Name of the offer.</span></span>

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

### <span data-ttu-id="6b89a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b89a-123">-PassThru</span></span>
<span data-ttu-id="6b89a-124">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6b89a-125">-Publisher</span><span class="sxs-lookup"><span data-stu-id="6b89a-125">-Publisher</span></span>
<span data-ttu-id="6b89a-126">게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-126">Name of the publisher.</span></span>

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

### <span data-ttu-id="6b89a-127">-Sku</span><span class="sxs-lookup"><span data-stu-id="6b89a-127">-Sku</span></span>
<span data-ttu-id="6b89a-128">SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-128">Name of the SKU.</span></span>

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

### <span data-ttu-id="6b89a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b89a-129">-SubscriptionId</span></span>
<span data-ttu-id="6b89a-130">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6b89a-131">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6b89a-132">-버전</span><span class="sxs-lookup"><span data-stu-id="6b89a-132">-Version</span></span>
<span data-ttu-id="6b89a-133">리소스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-133">The version of the resource.</span></span>

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

### <span data-ttu-id="6b89a-134">-확인</span><span class="sxs-lookup"><span data-stu-id="6b89a-134">-Confirm</span></span>
<span data-ttu-id="6b89a-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b89a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b89a-136">-WhatIf</span></span>
<span data-ttu-id="6b89a-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b89a-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b89a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b89a-139">CommonParameters</span></span>
<span data-ttu-id="6b89a-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b89a-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6b89a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b89a-142">입력</span><span class="sxs-lookup"><span data-stu-id="6b89a-142">INPUTS</span></span>

### <span data-ttu-id="6b89a-143">IComputeAdminIdentity (Microsoft. PowerShell. t t t)</span><span class="sxs-lookup"><span data-stu-id="6b89a-143">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="6b89a-144">출력</span><span class="sxs-lookup"><span data-stu-id="6b89a-144">OUTPUTS</span></span>

### <span data-ttu-id="6b89a-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6b89a-145">System.Boolean</span></span>



## <span data-ttu-id="6b89a-146">상속자</span><span class="sxs-lookup"><span data-stu-id="6b89a-146">NOTES</span></span>

<span data-ttu-id="6b89a-147">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b89a-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="6b89a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6b89a-149">INPUTOBJECT <IComputeAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b89a-149">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6b89a-150">`[DiskId <String>]`: 디스크 guid를 id로 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-150">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="6b89a-151">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="6b89a-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6b89a-152">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="6b89a-153">`[MigrationId <String>]`: 마이그레이션 작업 guid 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-153">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="6b89a-154">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-154">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="6b89a-155">`[Publisher <String>]`: 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-155">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="6b89a-156">`[QuotaName <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-156">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="6b89a-157">`[Sku <String>]`: SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-157">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="6b89a-158">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-158">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6b89a-159">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="6b89a-160">`[Type <String>]`: 확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-160">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="6b89a-161">`[Version <String>]`: 리소스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="6b89a-161">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="6b89a-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b89a-162">RELATED LINKS</span></span>


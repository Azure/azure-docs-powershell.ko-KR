---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwarecluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareCluster.md
ms.openlocfilehash: 936ed70f7040f9558db891b4e75299759c647bf9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309377"
---
# <span data-ttu-id="ce508-101">Remove-AzVMWareCluster</span><span class="sxs-lookup"><span data-stu-id="ce508-101">Remove-AzVMWareCluster</span></span>

## <span data-ttu-id="ce508-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce508-102">SYNOPSIS</span></span>
<span data-ttu-id="ce508-103">사설 클라우드에서 클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="ce508-103">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="ce508-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce508-104">SYNTAX</span></span>

### <span data-ttu-id="ce508-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ce508-105">Delete (Default)</span></span>
```
Remove-AzVMWareCluster -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ce508-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ce508-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareCluster -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ce508-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ce508-107">DESCRIPTION</span></span>
<span data-ttu-id="ce508-108">사설 클라우드에서 클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="ce508-108">Delete a cluster in a private cloud</span></span>

## <span data-ttu-id="ce508-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ce508-109">EXAMPLES</span></span>

### <span data-ttu-id="ce508-110">예제 1: 사설 클라우드에서 클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="ce508-110">Example 1: Delete cluster in private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareCluster -Name azps-test-cluster -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="ce508-111">사설 클라우드에서 클러스터 삭제</span><span class="sxs-lookup"><span data-stu-id="ce508-111">Delete cluster in private cloud</span></span>

## <span data-ttu-id="ce508-112">변수</span><span class="sxs-lookup"><span data-stu-id="ce508-112">PARAMETERS</span></span>

### <span data-ttu-id="ce508-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce508-113">-AsJob</span></span>
<span data-ttu-id="ce508-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ce508-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ce508-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce508-115">-DefaultProfile</span></span>
<span data-ttu-id="ce508-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce508-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce508-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce508-117">-InputObject</span></span>
<span data-ttu-id="ce508-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce508-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce508-119">-이름</span><span class="sxs-lookup"><span data-stu-id="ce508-119">-Name</span></span>
<span data-ttu-id="ce508-120">사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="ce508-120">Name of the cluster in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce508-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ce508-121">-NoWait</span></span>
<span data-ttu-id="ce508-122">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ce508-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ce508-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce508-123">-PassThru</span></span>
<span data-ttu-id="ce508-124">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce508-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ce508-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="ce508-125">-PrivateCloudName</span></span>
<span data-ttu-id="ce508-126">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="ce508-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="ce508-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce508-127">-ResourceGroupName</span></span>
<span data-ttu-id="ce508-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce508-128">The name of the resource group.</span></span>
<span data-ttu-id="ce508-129">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce508-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ce508-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce508-130">-SubscriptionId</span></span>
<span data-ttu-id="ce508-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ce508-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ce508-132">-확인</span><span class="sxs-lookup"><span data-stu-id="ce508-132">-Confirm</span></span>
<span data-ttu-id="ce508-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce508-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce508-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce508-134">-WhatIf</span></span>
<span data-ttu-id="ce508-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce508-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce508-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce508-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce508-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce508-137">CommonParameters</span></span>
<span data-ttu-id="ce508-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce508-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce508-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ce508-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce508-140">입력</span><span class="sxs-lookup"><span data-stu-id="ce508-140">INPUTS</span></span>

### <span data-ttu-id="ce508-141">IVMWareIdentity (Microsoft. v.</span><span class="sxs-lookup"><span data-stu-id="ce508-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="ce508-142">출력</span><span class="sxs-lookup"><span data-stu-id="ce508-142">OUTPUTS</span></span>

### <span data-ttu-id="ce508-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ce508-143">System.Boolean</span></span>

## <span data-ttu-id="ce508-144">상속자</span><span class="sxs-lookup"><span data-stu-id="ce508-144">NOTES</span></span>

<span data-ttu-id="ce508-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="ce508-145">ALIASES</span></span>

<span data-ttu-id="ce508-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="ce508-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ce508-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce508-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ce508-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="ce508-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ce508-149">INPUTOBJECT <IVMWareIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ce508-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ce508-150">`[AuthorizationName <String>]`: 사설 클라우드의 Express 경로 권한 부여 이름</span><span class="sxs-lookup"><span data-stu-id="ce508-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="ce508-151">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="ce508-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="ce508-152">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름</span><span class="sxs-lookup"><span data-stu-id="ce508-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="ce508-153">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="ce508-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ce508-154">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="ce508-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="ce508-155">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="ce508-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="ce508-156">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce508-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ce508-157">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce508-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="ce508-158">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ce508-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="ce508-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce508-159">RELATED LINKS</span></span>


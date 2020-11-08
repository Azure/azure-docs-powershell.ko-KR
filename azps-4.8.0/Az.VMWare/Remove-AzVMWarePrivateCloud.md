---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
ms.openlocfilehash: accf225acfb05fdcaf49eb5dde4d1bae0332d300
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212459"
---
# <span data-ttu-id="7ede0-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="7ede0-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="7ede0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ede0-102">SYNOPSIS</span></span>
<span data-ttu-id="7ede0-103">사설 클라우드 삭제</span><span class="sxs-lookup"><span data-stu-id="7ede0-103">Delete a private cloud</span></span>

## <span data-ttu-id="7ede0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7ede0-104">SYNTAX</span></span>

### <span data-ttu-id="7ede0-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="7ede0-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7ede0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7ede0-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7ede0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7ede0-107">DESCRIPTION</span></span>
<span data-ttu-id="7ede0-108">사설 클라우드 삭제</span><span class="sxs-lookup"><span data-stu-id="7ede0-108">Delete a private cloud</span></span>

## <span data-ttu-id="7ede0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7ede0-109">EXAMPLES</span></span>

### <span data-ttu-id="7ede0-110">예제 1: 사설 클라우드 삭제</span><span class="sxs-lookup"><span data-stu-id="7ede0-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="7ede0-111">사설 클라우드 삭제</span><span class="sxs-lookup"><span data-stu-id="7ede0-111">Delete private cloud</span></span>

## <span data-ttu-id="7ede0-112">변수</span><span class="sxs-lookup"><span data-stu-id="7ede0-112">PARAMETERS</span></span>

### <span data-ttu-id="7ede0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ede0-113">-AsJob</span></span>
<span data-ttu-id="7ede0-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="7ede0-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7ede0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ede0-115">-DefaultProfile</span></span>
<span data-ttu-id="7ede0-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7ede0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ede0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ede0-117">-InputObject</span></span>
<span data-ttu-id="7ede0-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7ede0-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7ede0-119">-이름</span><span class="sxs-lookup"><span data-stu-id="7ede0-119">-Name</span></span>
<span data-ttu-id="7ede0-120">사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="7ede0-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ede0-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7ede0-121">-NoWait</span></span>
<span data-ttu-id="7ede0-122">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="7ede0-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7ede0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ede0-123">-PassThru</span></span>
<span data-ttu-id="7ede0-124">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ede0-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7ede0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ede0-125">-ResourceGroupName</span></span>
<span data-ttu-id="7ede0-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ede0-126">The name of the resource group.</span></span>
<span data-ttu-id="7ede0-127">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ede0-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7ede0-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ede0-128">-SubscriptionId</span></span>
<span data-ttu-id="7ede0-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7ede0-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7ede0-130">-확인</span><span class="sxs-lookup"><span data-stu-id="7ede0-130">-Confirm</span></span>
<span data-ttu-id="7ede0-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ede0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ede0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ede0-132">-WhatIf</span></span>
<span data-ttu-id="7ede0-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7ede0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ede0-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ede0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ede0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ede0-135">CommonParameters</span></span>
<span data-ttu-id="7ede0-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ede0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ede0-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ede0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ede0-138">입력</span><span class="sxs-lookup"><span data-stu-id="7ede0-138">INPUTS</span></span>

### <span data-ttu-id="7ede0-139">IVMWareIdentity (Microsoft. v.</span><span class="sxs-lookup"><span data-stu-id="7ede0-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="7ede0-140">출력</span><span class="sxs-lookup"><span data-stu-id="7ede0-140">OUTPUTS</span></span>

### <span data-ttu-id="7ede0-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7ede0-141">System.Boolean</span></span>

## <span data-ttu-id="7ede0-142">상속자</span><span class="sxs-lookup"><span data-stu-id="7ede0-142">NOTES</span></span>

<span data-ttu-id="7ede0-143">별칭과</span><span class="sxs-lookup"><span data-stu-id="7ede0-143">ALIASES</span></span>

<span data-ttu-id="7ede0-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="7ede0-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7ede0-145">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ede0-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7ede0-146">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="7ede0-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7ede0-147">INPUTOBJECT <IVMWareIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7ede0-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7ede0-148">`[AuthorizationName <String>]`: 사설 클라우드의 Express 경로 권한 부여 이름</span><span class="sxs-lookup"><span data-stu-id="7ede0-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="7ede0-149">`[ClusterName <String>]`: 사설 클라우드의 클러스터 이름</span><span class="sxs-lookup"><span data-stu-id="7ede0-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="7ede0-150">`[HcxEnterpriseSiteName <String>]`: 사설 클라우드의 HCX Enterprise 사이트의 이름</span><span class="sxs-lookup"><span data-stu-id="7ede0-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="7ede0-151">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="7ede0-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7ede0-152">`[Location <String>]`: Azure 지역</span><span class="sxs-lookup"><span data-stu-id="7ede0-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="7ede0-153">`[PrivateCloudName <String>]`: 사설 클라우드의 이름</span><span class="sxs-lookup"><span data-stu-id="7ede0-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="7ede0-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ede0-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7ede0-155">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ede0-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="7ede0-156">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7ede0-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="7ede0-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ede0-157">RELATED LINKS</span></span>


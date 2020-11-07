---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/remove-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: fe7c391b8f15e3389a9d61070b8f55d47af6d6ec
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876023"
---
# <span data-ttu-id="8e857-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="8e857-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="8e857-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e857-102">SYNOPSIS</span></span>
<span data-ttu-id="8e857-103">이름으로 할당량을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-103">Delete a quota by name.</span></span>

## <span data-ttu-id="8e857-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e857-104">SYNTAX</span></span>

### <span data-ttu-id="8e857-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8e857-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8e857-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8e857-106">DeleteViaIdentity</span></span>
```
Remove-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8e857-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8e857-107">DESCRIPTION</span></span>
<span data-ttu-id="8e857-108">이름으로 할당량을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-108">Delete a quota by name.</span></span>

## <span data-ttu-id="8e857-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8e857-109">EXAMPLES</span></span>

### <span data-ttu-id="8e857-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8e857-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="8e857-111">이름으로 네트워크 할당량을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="8e857-112">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="8e857-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="8e857-113">파이프를 사용 하 여 네트워크 할당량을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="8e857-114">--------------------------예제 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="8e857-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="8e857-115">네트워크 할당량을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-115">Remove a network quota.</span></span>

## <span data-ttu-id="8e857-116">변수</span><span class="sxs-lookup"><span data-stu-id="8e857-116">PARAMETERS</span></span>

### <span data-ttu-id="8e857-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e857-117">-AsJob</span></span>
<span data-ttu-id="8e857-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="8e857-118">Run the command as a job</span></span>

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

### <span data-ttu-id="8e857-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e857-119">-DefaultProfile</span></span>
<span data-ttu-id="8e857-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e857-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e857-121">-InputObject</span></span>
<span data-ttu-id="8e857-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8e857-123">-위치</span><span class="sxs-lookup"><span data-stu-id="8e857-123">-Location</span></span>
<span data-ttu-id="8e857-124">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8e857-125">-이름</span><span class="sxs-lookup"><span data-stu-id="8e857-125">-Name</span></span>
<span data-ttu-id="8e857-126">리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-126">Name of the resource.</span></span>

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

### <span data-ttu-id="8e857-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8e857-127">-NoWait</span></span>
<span data-ttu-id="8e857-128">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="8e857-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8e857-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e857-129">-PassThru</span></span>
<span data-ttu-id="8e857-130">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8e857-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e857-131">-SubscriptionId</span></span>
<span data-ttu-id="8e857-132">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8e857-133">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8e857-134">-확인</span><span class="sxs-lookup"><span data-stu-id="8e857-134">-Confirm</span></span>
<span data-ttu-id="8e857-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e857-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e857-136">-WhatIf</span></span>
<span data-ttu-id="8e857-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e857-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e857-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e857-139">CommonParameters</span></span>
<span data-ttu-id="8e857-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e857-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8e857-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e857-142">입력</span><span class="sxs-lookup"><span data-stu-id="8e857-142">INPUTS</span></span>

### <span data-ttu-id="8e857-143">INetworkAdminIdentity (Microsoft. PowerShell. 관리자.</span><span class="sxs-lookup"><span data-stu-id="8e857-143">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="8e857-144">출력</span><span class="sxs-lookup"><span data-stu-id="8e857-144">OUTPUTS</span></span>

### <span data-ttu-id="8e857-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8e857-145">System.Boolean</span></span>



## <span data-ttu-id="8e857-146">상속자</span><span class="sxs-lookup"><span data-stu-id="8e857-146">NOTES</span></span>

<span data-ttu-id="8e857-147">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8e857-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="8e857-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8e857-149">INPUTOBJECT <INetworkAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8e857-149">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8e857-150">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="8e857-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8e857-151">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="8e857-152">`[ResourceName <String>]`: 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-152">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="8e857-153">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8e857-154">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e857-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8e857-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e857-155">RELATED LINKS</span></span>


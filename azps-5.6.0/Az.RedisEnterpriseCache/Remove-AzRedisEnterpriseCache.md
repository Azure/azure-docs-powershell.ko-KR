---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/remove-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
ms.openlocfilehash: d6b030cfbc6233d917d252f2d271eb7d4bfe65bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000736"
---
# <span data-ttu-id="462fc-101">Remove-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="462fc-101">Remove-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="462fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="462fc-102">SYNOPSIS</span></span>
<span data-ttu-id="462fc-103">RedisEnterprise 캐시 클러스터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-103">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="462fc-104">구문</span><span class="sxs-lookup"><span data-stu-id="462fc-104">SYNTAX</span></span>

### <span data-ttu-id="462fc-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="462fc-105">Delete (Default)</span></span>
```
Remove-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="462fc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="462fc-106">DeleteViaIdentity</span></span>
```
Remove-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="462fc-107">설명</span><span class="sxs-lookup"><span data-stu-id="462fc-107">DESCRIPTION</span></span>
<span data-ttu-id="462fc-108">RedisEnterprise 캐시 클러스터를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-108">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="462fc-109">예제</span><span class="sxs-lookup"><span data-stu-id="462fc-109">EXAMPLES</span></span>

### <span data-ttu-id="462fc-110">예제 1: Redis Enterprise Cache를 제거하고 결과를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-110">Example 1: Remove a Redis Enterprise Cache and return the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -PassThru
True
```

<span data-ttu-id="462fc-111">이 명령은 Redis Enterprise Cache를 제거하고 작업이 성공한지 여부를 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-111">This command removes a Redis Enterprise Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="462fc-112">예제 2: Redis Enterprise Cache를 제거하고 결과를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-112">Example 2: Remove a Redis Enterprise Cache and do not display the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup"
```

<span data-ttu-id="462fc-113">이 명령은 Redis Enterprise Cache를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-113">This command removes a Redis Enterprise Cache.</span></span>
<span data-ttu-id="462fc-114">PassThru 매개 변수가 지정되지 않은 경우 작업의 결과가 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-114">Because the PassThru parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="462fc-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="462fc-115">PARAMETERS</span></span>

### <span data-ttu-id="462fc-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="462fc-116">-AsJob</span></span>
<span data-ttu-id="462fc-117">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-117">Run the command as a job</span></span>

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

### <span data-ttu-id="462fc-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="462fc-118">-ClusterName</span></span>
<span data-ttu-id="462fc-119">RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-119">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="462fc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="462fc-120">-DefaultProfile</span></span>
<span data-ttu-id="462fc-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="462fc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="462fc-122">-InputObject</span></span>
<span data-ttu-id="462fc-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="462fc-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="462fc-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="462fc-124">-NoWait</span></span>
<span data-ttu-id="462fc-125">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="462fc-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="462fc-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="462fc-126">-PassThru</span></span>
<span data-ttu-id="462fc-127">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="462fc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="462fc-128">-ResourceGroupName</span></span>
<span data-ttu-id="462fc-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="462fc-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="462fc-130">-SubscriptionId</span></span>
<span data-ttu-id="462fc-131">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="462fc-132">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="462fc-133">-확인</span><span class="sxs-lookup"><span data-stu-id="462fc-133">-Confirm</span></span>
<span data-ttu-id="462fc-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="462fc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="462fc-135">-WhatIf</span></span>
<span data-ttu-id="462fc-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="462fc-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="462fc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="462fc-138">CommonParameters</span></span>
<span data-ttu-id="462fc-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="462fc-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="462fc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="462fc-141">입력</span><span class="sxs-lookup"><span data-stu-id="462fc-141">INPUTS</span></span>

### <span data-ttu-id="462fc-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="462fc-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="462fc-143">출력</span><span class="sxs-lookup"><span data-stu-id="462fc-143">OUTPUTS</span></span>

### <span data-ttu-id="462fc-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="462fc-144">System.Boolean</span></span>

## <span data-ttu-id="462fc-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="462fc-145">NOTES</span></span>

<span data-ttu-id="462fc-146">별칭</span><span class="sxs-lookup"><span data-stu-id="462fc-146">ALIASES</span></span>

<span data-ttu-id="462fc-147">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="462fc-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="462fc-148">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="462fc-149">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="462fc-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="462fc-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="462fc-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="462fc-151">`[ClusterName <String>]`: RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-151">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="462fc-152">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-152">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="462fc-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="462fc-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="462fc-154">`[Location <String>]`: 작업이 있는 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-154">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="462fc-155">`[OperationId <String>]`: 작업의 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-155">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="462fc-156">`[PrivateEndpointConnectionName <String>]`: Azure 리소스와 연결된 개인 엔드포인트 연결의 이름</span><span class="sxs-lookup"><span data-stu-id="462fc-156">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="462fc-157">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="462fc-158">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="462fc-159">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="462fc-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="462fc-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="462fc-160">RELATED LINKS</span></span>


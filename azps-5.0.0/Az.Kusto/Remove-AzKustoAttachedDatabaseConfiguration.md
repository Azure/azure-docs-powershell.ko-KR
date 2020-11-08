---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 9d38b9c3297dc950cc12d46189bc940e27877d8a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218989"
---
# <span data-ttu-id="0fd3d-101">Remove-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="0fd3d-101">Remove-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="0fd3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fd3d-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd3d-103">지정 된 이름을 사용 하 여 연결 된 데이터베이스 구성을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-103">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="0fd3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0fd3d-104">SYNTAX</span></span>

### <span data-ttu-id="0fd3d-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="0fd3d-105">Delete (Default)</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0fd3d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0fd3d-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0fd3d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0fd3d-107">DESCRIPTION</span></span>
<span data-ttu-id="0fd3d-108">지정 된 이름을 사용 하 여 연결 된 데이터베이스 구성을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-108">Deletes the attached database configuration with the given name.</span></span>

## <span data-ttu-id="0fd3d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0fd3d-109">EXAMPLES</span></span>

### <span data-ttu-id="0fd3d-110">예제 1: 이름으로 기존 AttachedDatabaseConfiguration 삭제</span><span class="sxs-lookup"><span data-stu-id="0fd3d-110">Example 1: Delete an existing AttachedDatabaseConfiguration by name</span></span>
```powershell
PS C:\> Remove-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration"
```

<span data-ttu-id="0fd3d-111">위 명령은 "testnewkustoclusterf" AttachedDatabaseConfiguration "my configuration"에서 정의 된 종동체 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-111">The above command deletes the follower database defined in the AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="0fd3d-112">변수</span><span class="sxs-lookup"><span data-stu-id="0fd3d-112">PARAMETERS</span></span>

### <span data-ttu-id="0fd3d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fd3d-113">-AsJob</span></span>
<span data-ttu-id="0fd3d-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="0fd3d-114">Run the command as a job</span></span>

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

### <span data-ttu-id="0fd3d-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0fd3d-115">-ClusterName</span></span>
<span data-ttu-id="0fd3d-116">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="0fd3d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd3d-117">-DefaultProfile</span></span>
<span data-ttu-id="0fd3d-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fd3d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fd3d-119">-InputObject</span></span>
<span data-ttu-id="0fd3d-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd3d-121">-이름</span><span class="sxs-lookup"><span data-stu-id="0fd3d-121">-Name</span></span>
<span data-ttu-id="0fd3d-122">연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-122">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd3d-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0fd3d-123">-NoWait</span></span>
<span data-ttu-id="0fd3d-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="0fd3d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0fd3d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fd3d-125">-PassThru</span></span>
<span data-ttu-id="0fd3d-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0fd3d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fd3d-127">-ResourceGroupName</span></span>
<span data-ttu-id="0fd3d-128">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0fd3d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0fd3d-129">-SubscriptionId</span></span>
<span data-ttu-id="0fd3d-130">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-130">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0fd3d-131">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0fd3d-132">-확인</span><span class="sxs-lookup"><span data-stu-id="0fd3d-132">-Confirm</span></span>
<span data-ttu-id="0fd3d-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fd3d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fd3d-134">-WhatIf</span></span>
<span data-ttu-id="0fd3d-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fd3d-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fd3d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd3d-137">CommonParameters</span></span>
<span data-ttu-id="0fd3d-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd3d-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd3d-140">입력</span><span class="sxs-lookup"><span data-stu-id="0fd3d-140">INPUTS</span></span>

### <span data-ttu-id="0fd3d-141">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="0fd3d-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0fd3d-142">출력</span><span class="sxs-lookup"><span data-stu-id="0fd3d-142">OUTPUTS</span></span>

### <span data-ttu-id="0fd3d-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0fd3d-143">System.Boolean</span></span>

## <span data-ttu-id="0fd3d-144">상속자</span><span class="sxs-lookup"><span data-stu-id="0fd3d-144">NOTES</span></span>

<span data-ttu-id="0fd3d-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="0fd3d-145">ALIASES</span></span>

<span data-ttu-id="0fd3d-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="0fd3d-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0fd3d-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0fd3d-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0fd3d-149">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0fd3d-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0fd3d-150">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0fd3d-151">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0fd3d-152">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0fd3d-153">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0fd3d-154">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="0fd3d-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0fd3d-155">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0fd3d-156">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0fd3d-157">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0fd3d-158">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0fd3d-159">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0fd3d-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0fd3d-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0fd3d-160">RELATED LINKS</span></span>


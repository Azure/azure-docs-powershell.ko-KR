---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/remove-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDataConnection.md
ms.openlocfilehash: ac2eac129231f33a2f74732923652d3851debbd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974832"
---
# <span data-ttu-id="cdde8-101">Remove-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="cdde8-101">Remove-AzKustoDataConnection</span></span>

## <span data-ttu-id="cdde8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdde8-102">SYNOPSIS</span></span>
<span data-ttu-id="cdde8-103">지정한 이름으로 데이터 연결을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-103">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="cdde8-104">구문</span><span class="sxs-lookup"><span data-stu-id="cdde8-104">SYNTAX</span></span>

### <span data-ttu-id="cdde8-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="cdde8-105">Delete (Default)</span></span>
```
Remove-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cdde8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cdde8-106">DeleteViaIdentity</span></span>
```
Remove-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cdde8-107">설명</span><span class="sxs-lookup"><span data-stu-id="cdde8-107">DESCRIPTION</span></span>
<span data-ttu-id="cdde8-108">지정한 이름으로 데이터 연결을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-108">Deletes the data connection with the given name.</span></span>

## <span data-ttu-id="cdde8-109">예제</span><span class="sxs-lookup"><span data-stu-id="cdde8-109">EXAMPLES</span></span>

### <span data-ttu-id="cdde8-110">예제 1: 이름에 따라 기존 데이터 연결 삭제</span><span class="sxs-lookup"><span data-stu-id="cdde8-110">Example 1: Delete an existing data connection by name</span></span>
```powershell
PS C:\> Remove-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"
```

<span data-ttu-id="cdde8-111">위의 명령은 리소스 그룹 "testrg"에 있는 기존 클러스터 "testnewkustocluster"의 데이터베이스 "mykustodatabase"에서 "mykustodataconnection"이라는 데이터 연결을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-111">The above command deletes the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg"</span></span>

## <span data-ttu-id="cdde8-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cdde8-112">PARAMETERS</span></span>

### <span data-ttu-id="cdde8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cdde8-113">-AsJob</span></span>
<span data-ttu-id="cdde8-114">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-114">Run the command as a job</span></span>

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

### <span data-ttu-id="cdde8-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cdde8-115">-ClusterName</span></span>
<span data-ttu-id="cdde8-116">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="cdde8-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cdde8-117">-DatabaseName</span></span>
<span data-ttu-id="cdde8-118">Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="cdde8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdde8-119">-DefaultProfile</span></span>
<span data-ttu-id="cdde8-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdde8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdde8-121">-InputObject</span></span>
<span data-ttu-id="cdde8-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="cdde8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cdde8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="cdde8-123">-Name</span></span>
<span data-ttu-id="cdde8-124">데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-124">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdde8-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cdde8-125">-NoWait</span></span>
<span data-ttu-id="cdde8-126">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="cdde8-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cdde8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdde8-127">-PassThru</span></span>
<span data-ttu-id="cdde8-128">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cdde8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdde8-129">-ResourceGroupName</span></span>
<span data-ttu-id="cdde8-130">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="cdde8-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cdde8-131">-SubscriptionId</span></span>
<span data-ttu-id="cdde8-132">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cdde8-133">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cdde8-134">-확인</span><span class="sxs-lookup"><span data-stu-id="cdde8-134">-Confirm</span></span>
<span data-ttu-id="cdde8-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdde8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdde8-136">-WhatIf</span></span>
<span data-ttu-id="cdde8-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdde8-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdde8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdde8-139">CommonParameters</span></span>
<span data-ttu-id="cdde8-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdde8-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cdde8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdde8-142">입력</span><span class="sxs-lookup"><span data-stu-id="cdde8-142">INPUTS</span></span>

### <span data-ttu-id="cdde8-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="cdde8-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="cdde8-144">출력</span><span class="sxs-lookup"><span data-stu-id="cdde8-144">OUTPUTS</span></span>

### <span data-ttu-id="cdde8-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cdde8-145">System.Boolean</span></span>

## <span data-ttu-id="cdde8-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cdde8-146">NOTES</span></span>

<span data-ttu-id="cdde8-147">별칭</span><span class="sxs-lookup"><span data-stu-id="cdde8-147">ALIASES</span></span>

<span data-ttu-id="cdde8-148">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="cdde8-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cdde8-149">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cdde8-150">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cdde8-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cdde8-151">INPUTOBJECT <IKustoIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="cdde8-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cdde8-152">`[AttachedDatabaseConfigurationName <String>]`: 연결된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="cdde8-153">`[ClusterName <String>]`: Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="cdde8-154">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="cdde8-155">`[DatabaseName <String>]`: Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="cdde8-156">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="cdde8-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cdde8-157">`[Location <String>]`: Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="cdde8-158">`[PrincipalAssignmentName <String>]`: Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="cdde8-159">`[ResourceGroupName <String>]`: Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="cdde8-160">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cdde8-161">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="cdde8-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cdde8-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cdde8-162">RELATED LINKS</span></span>


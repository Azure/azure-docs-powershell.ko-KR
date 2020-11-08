---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 4becbb8285685c923fe6b0ec2174e7e84824a106
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219009"
---
# <span data-ttu-id="b0461-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="b0461-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="b0461-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0461-102">SYNOPSIS</span></span>
<span data-ttu-id="b0461-103">클러스터 데이터베이스 principalAssignment에 대 한 Kusto를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="b0461-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0461-104">SYNTAX</span></span>

### <span data-ttu-id="b0461-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b0461-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b0461-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="b0461-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b0461-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b0461-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0461-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b0461-108">DESCRIPTION</span></span>
<span data-ttu-id="b0461-109">클러스터 데이터베이스 principalAssignment에 대 한 Kusto를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="b0461-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b0461-110">EXAMPLES</span></span>

### <span data-ttu-id="b0461-111">예제 1: 이름으로 데이터베이스에 모든 PrincipalAssignment 배정 나열</span><span class="sxs-lookup"><span data-stu-id="b0461-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="b0461-112">위 명령은 "testnewkustocluster" 클러스터에서 찾은 "mykustodatabase" 데이터베이스의 모든 PrincipalAssignment을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="b0461-113">예제 2: 이름으로 데이터베이스에서 특정 PrincipalAssignment 가져오기</span><span class="sxs-lookup"><span data-stu-id="b0461-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="b0461-114">위 명령은 "testnewkustocluster" 데이터베이스에서 "kustoprincipal1" "이라는 모든 PrincipalAssignment을" mykustodatabase "(으)로 반환 했습니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="b0461-115">변수</span><span class="sxs-lookup"><span data-stu-id="b0461-115">PARAMETERS</span></span>

### <span data-ttu-id="b0461-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b0461-116">-ClusterName</span></span>
<span data-ttu-id="b0461-117">Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-117">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0461-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b0461-118">-DatabaseName</span></span>
<span data-ttu-id="b0461-119">Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-119">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0461-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0461-120">-DefaultProfile</span></span>
<span data-ttu-id="b0461-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0461-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0461-122">-InputObject</span></span>
<span data-ttu-id="b0461-123">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0461-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="b0461-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="b0461-125">Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-125">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0461-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0461-126">-ResourceGroupName</span></span>
<span data-ttu-id="b0461-127">Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-127">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0461-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b0461-128">-SubscriptionId</span></span>
<span data-ttu-id="b0461-129">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b0461-130">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0461-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0461-131">CommonParameters</span></span>
<span data-ttu-id="b0461-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0461-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0461-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0461-134">입력</span><span class="sxs-lookup"><span data-stu-id="b0461-134">INPUTS</span></span>

### <span data-ttu-id="b0461-135">IKustoIdentity (Microsoft. PowerShell. m a us</span><span class="sxs-lookup"><span data-stu-id="b0461-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="b0461-136">출력</span><span class="sxs-lookup"><span data-stu-id="b0461-136">OUTPUTS</span></span>

### <span data-ttu-id="b0461-137">Api20200614. IDatabasePrincipalAssignment의 a에 대 한 대입</span><span class="sxs-lookup"><span data-stu-id="b0461-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="b0461-138">상속자</span><span class="sxs-lookup"><span data-stu-id="b0461-138">NOTES</span></span>

<span data-ttu-id="b0461-139">별칭과</span><span class="sxs-lookup"><span data-stu-id="b0461-139">ALIASES</span></span>

<span data-ttu-id="b0461-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b0461-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b0461-141">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b0461-142">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="b0461-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b0461-143">INPUTOBJECT <IKustoIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b0461-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b0461-144">`[AttachedDatabaseConfigurationName <String>]`: 연결 된 데이터베이스 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="b0461-145">`[ClusterName <String>]`: Kusto의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="b0461-146">`[DataConnectionName <String>]`: 데이터 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="b0461-147">`[DatabaseName <String>]`: Kusto cluster의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="b0461-148">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="b0461-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b0461-149">`[Location <String>]`: Azure 위치.</span><span class="sxs-lookup"><span data-stu-id="b0461-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="b0461-150">`[PrincipalAssignmentName <String>]`:%에 대 한 Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="b0461-151">`[ResourceGroupName <String>]`: Kusto cluster를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="b0461-152">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b0461-153">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0461-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b0461-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0461-154">RELATED LINKS</span></span>


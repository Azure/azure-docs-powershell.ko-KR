---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
ms.openlocfilehash: b9f008d610729d1f1bc73affbb5b8f3eae04ecdd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044259"
---
# <span data-ttu-id="83701-101">Get-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="83701-101">Get-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="83701-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83701-102">SYNOPSIS</span></span>
<span data-ttu-id="83701-103">SQL 관리 되는 인스턴스의 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83701-103">Gets a SQL managed instance's operations.</span></span>

## <span data-ttu-id="83701-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83701-104">SYNTAX</span></span>

### <span data-ttu-id="83701-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="83701-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceOperation [-Name <Guid>] -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83701-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="83701-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstanceOperation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83701-107">ListByManagedInstanceParameterSet</span><span class="sxs-lookup"><span data-stu-id="83701-107">ListByManagedInstanceParameterSet</span></span>
```
Get-AzSqlInstanceOperation -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83701-108">설명은</span><span class="sxs-lookup"><span data-stu-id="83701-108">DESCRIPTION</span></span>
<span data-ttu-id="83701-109">Get-AzSqlInstanceOperation cmdlet은 SQL 관리 인스턴스에 대 한 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83701-109">The Get-AzSqlInstanceOperation cmdlet gets information about the operations on a SQL managed instance.</span></span> <span data-ttu-id="83701-110">관리 되는 인스턴스에서 모든 작업을 보거나 작업 이름을 제공 하 여 특정 작업을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="83701-110">You can view all operations on a managed instance or view a specific operation by providing the operation name.</span></span>

## <span data-ttu-id="83701-111">예제의</span><span class="sxs-lookup"><span data-stu-id="83701-111">EXAMPLES</span></span>

### <span data-ttu-id="83701-112">예제 1: 모든 인스턴스의 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="83701-112">Example 1: Get all instance's operations</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/79f2c91b-0080-4c14-b9b4-d9991c6e82dd
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 79f2c91b-0080-4c14-b9b4-d9991c6e82dd
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:19:53 AM
State                   : Cancelled
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
```

<span data-ttu-id="83701-113">이 명령은 모든 작업을 SQL 관리 되는 인스턴스로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83701-113">This command gets all operations a SQL managed instance.</span></span>

### <span data-ttu-id="83701-114">예제 2: 특정 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="83701-114">Example 2: Get a specific operation</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
```

<span data-ttu-id="83701-115">이 명령은 SQL 관리 인스턴스에서 이름이 ' 5870c6d8-6703-4b27-8ae4-687b4ca7caea ' 인 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83701-115">This command gets operation with name '5870c6d8-6703-4b27-8ae4-687b4ca7caea' on a SQL managed instance.</span></span>

### <span data-ttu-id="83701-116">예제 3: Using 작업 리소스 id</span><span class="sxs-lookup"><span data-stu-id="83701-116">Example 3: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
```

<span data-ttu-id="83701-117">이 명령은 id가 '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea ' 인 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83701-117">This command gets operation with id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span></span>

## <span data-ttu-id="83701-118">변수</span><span class="sxs-lookup"><span data-stu-id="83701-118">PARAMETERS</span></span>

### <span data-ttu-id="83701-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83701-119">-DefaultProfile</span></span>
<span data-ttu-id="83701-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83701-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83701-121">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="83701-121">-ManagedInstanceName</span></span>
<span data-ttu-id="83701-122">인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83701-122">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83701-123">-이름</span><span class="sxs-lookup"><span data-stu-id="83701-123">-Name</span></span>
<span data-ttu-id="83701-124">작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83701-124">The name of the operation.</span></span>

```yaml
Type: System.Guid
Parameter Sets: DefaultParameterSet
Aliases: OperationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83701-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83701-125">-ResourceGroupName</span></span>
<span data-ttu-id="83701-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83701-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83701-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83701-127">-ResourceId</span></span>
<span data-ttu-id="83701-128">관리 되는 인스턴스 작업 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="83701-128">The managed instance operation resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByManagedInstanceOperationResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83701-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83701-129">CommonParameters</span></span>
<span data-ttu-id="83701-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83701-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83701-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="83701-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83701-132">입력</span><span class="sxs-lookup"><span data-stu-id="83701-132">INPUTS</span></span>

### <span data-ttu-id="83701-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="83701-133">System.String</span></span>

## <span data-ttu-id="83701-134">출력</span><span class="sxs-lookup"><span data-stu-id="83701-134">OUTPUTS</span></span>

### <span data-ttu-id="83701-135">AzureSqlManagedInstanceOperationModel를 수행 하세요.. m m.</span><span class="sxs-lookup"><span data-stu-id="83701-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="83701-136">상속자</span><span class="sxs-lookup"><span data-stu-id="83701-136">NOTES</span></span>

## <span data-ttu-id="83701-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83701-137">RELATED LINKS</span></span>

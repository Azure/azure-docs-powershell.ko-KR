---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
ms.openlocfilehash: c57b704f54eacbd9b5cac808e69f9bbf289dc0cc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878721"
---
# <span data-ttu-id="481ad-101">Stop-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="481ad-101">Stop-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="481ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="481ad-102">SYNOPSIS</span></span>
<span data-ttu-id="481ad-103">SQL 관리 되는 인스턴스의 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="481ad-103">Stops a SQL managed instance's operations.</span></span>

## <span data-ttu-id="481ad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="481ad-104">SYNTAX</span></span>

### <span data-ttu-id="481ad-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="481ad-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Default)</span></span>
```
Stop-AzSqlInstanceOperation [-Name] <String> [-ManagedInstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="481ad-106">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="481ad-106">StopByResourceIdParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="481ad-107">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="481ad-107">StopByInputObjectParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-InputObject] <AzureSqlManagedInstanceOperationModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="481ad-108">설명은</span><span class="sxs-lookup"><span data-stu-id="481ad-108">DESCRIPTION</span></span>
<span data-ttu-id="481ad-109">Stop-AzSqlInstanceOperation cmdlet은 SQL 관리 인스턴스에서 제공 된 작업 이름을 사용 하 여 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="481ad-109">The Stop-AzSqlInstanceOperation cmdlet stops operation with provided operation name on a SQL managed instance.</span></span>

## <span data-ttu-id="481ad-110">예제의</span><span class="sxs-lookup"><span data-stu-id="481ad-110">EXAMPLES</span></span>

### <span data-ttu-id="481ad-111">예제 1: 특정 작업 가져오기</span><span class="sxs-lookup"><span data-stu-id="481ad-111">Example 1: Get a specific operation</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name d0f5bef5-e2b1-4ef8-bb42-2e54073874f9

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:49:53 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="481ad-112">이 명령은 SQL 관리 인스턴스에서 이름이 ' d0f5bef5-e2b1-4ef8-bb42-2e54073874f9 ' 인 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="481ad-112">This command stops operation with name 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' on a SQL managed instance.</span></span>

### <span data-ttu-id="481ad-113">예제 2: 작업 리소스 id 사용</span><span class="sxs-lookup"><span data-stu-id="481ad-113">Example 2: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 4253bf58-34f1-4499-80c6-198d94c659f7
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/4253bf58-34f1-4499-80c6-198d94c659f7
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 4253bf58-34f1-4499-80c6-198d94c659f7
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:47:32 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="481ad-114">이 명령은 리소스 id $managedInstanceOperation. i a i d에 대 한 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="481ad-114">This command stops operation with resource id $managedInstanceOperation.Id.</span></span>

### <span data-ttu-id="481ad-115">예제 3: Using 작업 개체</span><span class="sxs-lookup"><span data-stu-id="481ad-115">Example 3: Using operation object</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name b15a2b78-c42c-4e00-bf87-7ef4737552dc
PS C:\> Stop-AzSqlInstanceOperation -InputObject $managedInstanceOperation

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/b15a2b78-c42c-4e00-bf87-7ef4737552dc
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : b15a2b78-c42c-4e00-bf87-7ef4737552dc
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:44:57 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="481ad-116">이 명령은 $managedInstanceOperation 개체를 사용 하 여 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="481ad-116">This command stops operation with object $managedInstanceOperation.</span></span>

## <span data-ttu-id="481ad-117">변수</span><span class="sxs-lookup"><span data-stu-id="481ad-117">PARAMETERS</span></span>

### <span data-ttu-id="481ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="481ad-118">-DefaultProfile</span></span>
<span data-ttu-id="481ad-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="481ad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="481ad-120">-Force</span><span class="sxs-lookup"><span data-stu-id="481ad-120">-Force</span></span>
<span data-ttu-id="481ad-121">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="481ad-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="481ad-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="481ad-122">-InputObject</span></span>
<span data-ttu-id="481ad-123">취소할 작업</span><span class="sxs-lookup"><span data-stu-id="481ad-123">The operation to cancel</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel
Parameter Sets: StopByInputObjectParameterSet
Aliases: SqlInstanceOperation

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="481ad-124">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="481ad-124">-ManagedInstanceName</span></span>
<span data-ttu-id="481ad-125">인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="481ad-125">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481ad-126">-이름</span><span class="sxs-lookup"><span data-stu-id="481ad-126">-Name</span></span>
<span data-ttu-id="481ad-127">작업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="481ad-127">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases: OperationName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481ad-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="481ad-128">-ResourceGroupName</span></span>
<span data-ttu-id="481ad-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="481ad-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="481ad-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="481ad-130">-ResourceId</span></span>
<span data-ttu-id="481ad-131">중지할 작업 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="481ad-131">The resource id of operation object to stop</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="481ad-132">-확인</span><span class="sxs-lookup"><span data-stu-id="481ad-132">-Confirm</span></span>
<span data-ttu-id="481ad-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="481ad-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="481ad-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="481ad-134">-WhatIf</span></span>
<span data-ttu-id="481ad-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="481ad-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="481ad-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="481ad-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="481ad-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="481ad-137">CommonParameters</span></span>
<span data-ttu-id="481ad-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="481ad-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="481ad-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="481ad-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="481ad-140">입력</span><span class="sxs-lookup"><span data-stu-id="481ad-140">INPUTS</span></span>

### <span data-ttu-id="481ad-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="481ad-141">System.String</span></span>

### <span data-ttu-id="481ad-142">AzureSqlManagedInstanceOperationModel를 수행 하세요.. m m.</span><span class="sxs-lookup"><span data-stu-id="481ad-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="481ad-143">출력</span><span class="sxs-lookup"><span data-stu-id="481ad-143">OUTPUTS</span></span>

### <span data-ttu-id="481ad-144">AzureSqlManagedInstanceOperationModel를 수행 하세요.. m m.</span><span class="sxs-lookup"><span data-stu-id="481ad-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="481ad-145">상속자</span><span class="sxs-lookup"><span data-stu-id="481ad-145">NOTES</span></span>

## <span data-ttu-id="481ad-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="481ad-146">RELATED LINKS</span></span>

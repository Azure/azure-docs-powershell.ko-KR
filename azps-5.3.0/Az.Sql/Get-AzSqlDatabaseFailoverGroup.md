---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a2c7192fc1ce2055b05a4f943a0c04560f1e714e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375033"
---
# <span data-ttu-id="b23e6-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b23e6-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="b23e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b23e6-102">SYNOPSIS</span></span>
<span data-ttu-id="b23e6-103">Azure SQL 장애 조치(failover) 그룹을 만들거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b23e6-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="b23e6-104">구문</span><span class="sxs-lookup"><span data-stu-id="b23e6-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b23e6-105">설명</span><span class="sxs-lookup"><span data-stu-id="b23e6-105">DESCRIPTION</span></span>
<span data-ttu-id="b23e6-106">특정 Azure SQL 데이터베이스 장애 조치(failover) 그룹을 얻거나 서버에 장애 조치(failover) 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b23e6-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="b23e6-107">장애 조치 그룹의 서버 중 하나를 사용하여 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b23e6-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="b23e6-108">반환된 값은 장애 조치(failover) 그룹과 관련한 지정된 서버의 상태를 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="b23e6-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="b23e6-109">예제</span><span class="sxs-lookup"><span data-stu-id="b23e6-109">EXAMPLES</span></span>

### <span data-ttu-id="b23e6-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b23e6-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="b23e6-111">서버의 모든 장애 조치(failover) 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b23e6-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="b23e6-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="b23e6-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="b23e6-113">특정 장애 조치(failover) 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b23e6-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="b23e6-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="b23e6-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="b23e6-115">"fg"로 시작하는 서버의 모든 장애 조치(failover) 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b23e6-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="b23e6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b23e6-116">PARAMETERS</span></span>

### <span data-ttu-id="b23e6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b23e6-117">-DefaultProfile</span></span>
<span data-ttu-id="b23e6-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b23e6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b23e6-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="b23e6-119">-FailoverGroupName</span></span>
<span data-ttu-id="b23e6-120">검색할 Azure SQL 데이터베이스 장애 조치(failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b23e6-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b23e6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b23e6-121">-ResourceGroupName</span></span>
<span data-ttu-id="b23e6-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b23e6-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b23e6-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b23e6-123">-ServerName</span></span>
<span data-ttu-id="b23e6-124">장애 조치(failover) 그룹을 SQL 데이터베이스 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b23e6-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b23e6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b23e6-125">CommonParameters</span></span>
<span data-ttu-id="b23e6-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b23e6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b23e6-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b23e6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b23e6-128">입력</span><span class="sxs-lookup"><span data-stu-id="b23e6-128">INPUTS</span></span>

### <span data-ttu-id="b23e6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b23e6-129">System.String</span></span>

## <span data-ttu-id="b23e6-130">출력</span><span class="sxs-lookup"><span data-stu-id="b23e6-130">OUTPUTS</span></span>

### <span data-ttu-id="b23e6-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="b23e6-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="b23e6-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b23e6-132">NOTES</span></span>

## <span data-ttu-id="b23e6-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b23e6-133">RELATED LINKS</span></span>

[<span data-ttu-id="b23e6-134">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b23e6-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b23e6-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b23e6-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b23e6-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b23e6-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="b23e6-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b23e6-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="b23e6-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b23e6-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b23e6-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b23e6-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b23e6-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="b23e6-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

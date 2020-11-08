---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a2c7192fc1ce2055b05a4f943a0c04560f1e714e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048701"
---
# <span data-ttu-id="582be-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="582be-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="582be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="582be-102">SYNOPSIS</span></span>
<span data-ttu-id="582be-103">Azure SQL 데이터베이스 장애 조치 (Failover) 그룹을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="582be-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="582be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="582be-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="582be-105">설명은</span><span class="sxs-lookup"><span data-stu-id="582be-105">DESCRIPTION</span></span>
<span data-ttu-id="582be-106">특정 Azure SQL 데이터베이스 장애 조치 그룹을 가져오거나 서버의 장애 조치 (Failover) 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="582be-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="582be-107">장애 조치 (Failover) 그룹의 서버 중 하나를 사용 하 여 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="582be-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="582be-108">반환 된 값은 장애 조치 그룹과 관련 하 여 지정 된 서버의 상태를 반영 합니다.</span><span class="sxs-lookup"><span data-stu-id="582be-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="582be-109">예제의</span><span class="sxs-lookup"><span data-stu-id="582be-109">EXAMPLES</span></span>

### <span data-ttu-id="582be-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="582be-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="582be-111">서버의 모든 장애 조치 (Failover) 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="582be-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="582be-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="582be-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="582be-113">특정 장애 조치 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="582be-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="582be-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="582be-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="582be-115">"Fg"로 시작 하는 서버의 모든 장애 조치 (failover) 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="582be-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="582be-116">변수</span><span class="sxs-lookup"><span data-stu-id="582be-116">PARAMETERS</span></span>

### <span data-ttu-id="582be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="582be-117">-DefaultProfile</span></span>
<span data-ttu-id="582be-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="582be-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="582be-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="582be-119">-FailoverGroupName</span></span>
<span data-ttu-id="582be-120">검색할 Azure SQL Database 장애 조치 (Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="582be-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="582be-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="582be-121">-ResourceGroupName</span></span>
<span data-ttu-id="582be-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="582be-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="582be-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="582be-123">-ServerName</span></span>
<span data-ttu-id="582be-124">장애 조치 (Failover) 그룹을 검색할 Azure SQL 데이터베이스 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="582be-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="582be-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="582be-125">CommonParameters</span></span>
<span data-ttu-id="582be-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="582be-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="582be-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="582be-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="582be-128">입력</span><span class="sxs-lookup"><span data-stu-id="582be-128">INPUTS</span></span>

### <span data-ttu-id="582be-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="582be-129">System.String</span></span>

## <span data-ttu-id="582be-130">출력</span><span class="sxs-lookup"><span data-stu-id="582be-130">OUTPUTS</span></span>

### <span data-ttu-id="582be-131">AzureSqlFailoverGroupModel (\*. \*.)</span><span class="sxs-lookup"><span data-stu-id="582be-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="582be-132">상속자</span><span class="sxs-lookup"><span data-stu-id="582be-132">NOTES</span></span>

## <span data-ttu-id="582be-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="582be-133">RELATED LINKS</span></span>

[<span data-ttu-id="582be-134">새로운 AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="582be-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="582be-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="582be-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="582be-136">추가-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="582be-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="582be-137">제거-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="582be-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="582be-138">스위치-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="582be-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="582be-139">제거-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="582be-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="582be-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="582be-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

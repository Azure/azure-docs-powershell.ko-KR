---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
ms.openlocfilehash: 7dc07f1064837b710c246e4aafb4ceb008019e4e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327928"
---
# <span data-ttu-id="98105-101">Get-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="98105-101">Get-AzSqlSyncSchema</span></span>

## <span data-ttu-id="98105-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98105-102">SYNOPSIS</span></span>
<span data-ttu-id="98105-103">멤버 데이터베이스 또는 허브 데이터베이스의 동기화 SCHEMA에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="98105-103">Returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="98105-104">구문</span><span class="sxs-lookup"><span data-stu-id="98105-104">SYNTAX</span></span>

```
Get-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98105-105">설명</span><span class="sxs-lookup"><span data-stu-id="98105-105">DESCRIPTION</span></span>
<span data-ttu-id="98105-106">**Get-AzSqlSyncSchema** cmdlet은 멤버 데이터베이스 또는 허브 데이터베이스의 동기화 키에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="98105-106">The **Get-AzSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="98105-107">예제</span><span class="sxs-lookup"><span data-stu-id="98105-107">EXAMPLES</span></span>

### <span data-ttu-id="98105-108">예제 1: 허브 데이터베이스에 대한 동기화 SCHEMA를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="98105-108">Example 1: Get the sync schema for a hub database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="98105-109">이 명령은 동기화 그룹 syncGroup01에서 허브 데이터베이스에 대한 동기화 스마마를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="98105-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="98105-110">예제 2: 허브 데이터베이스에 대한 동기화 SCHEMA를 확정하고 테이블 확장</span><span class="sxs-lookup"><span data-stu-id="98105-110">Example 2: Get the sync schema for a hub database, and expand Tables</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
Columns    : {column1, column2}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_1
QuotedName : [dbo].[Table_1]

Columns    : {column2, column4}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_2
QuotedName : [dbo].[Table_2]
```

<span data-ttu-id="98105-111">이 명령은 동기화 그룹 syncGroup01에서 허브 데이터베이스에 대한 동기화 스마마를되고 테이블 속성을 확장합니다.</span><span class="sxs-lookup"><span data-stu-id="98105-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="98105-112">예제 3: 멤버 데이터베이스에 대한 동기화 SCHEMA를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="98105-112">Example 3: Get the sync schema for a member database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="98105-113">이 명령은 동기화 멤버 syncMember01에서 멤버 데이터베이스에 대한 동기화 스마마를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="98105-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="98105-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98105-114">PARAMETERS</span></span>

### <span data-ttu-id="98105-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="98105-115">-DatabaseName</span></span>
<span data-ttu-id="98105-116">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98105-116">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98105-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98105-117">-DefaultProfile</span></span>
<span data-ttu-id="98105-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="98105-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98105-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98105-119">-ResourceGroupName</span></span>
<span data-ttu-id="98105-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98105-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="98105-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="98105-121">-ServerName</span></span>
<span data-ttu-id="98105-122">The name of the Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="98105-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="98105-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="98105-123">-SyncGroupName</span></span>
<span data-ttu-id="98105-124">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98105-124">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98105-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="98105-125">-SyncMemberName</span></span>
<span data-ttu-id="98105-126">동기화 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98105-126">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98105-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98105-127">CommonParameters</span></span>
<span data-ttu-id="98105-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="98105-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98105-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="98105-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98105-130">입력</span><span class="sxs-lookup"><span data-stu-id="98105-130">INPUTS</span></span>

### <span data-ttu-id="98105-131">System.String</span><span class="sxs-lookup"><span data-stu-id="98105-131">System.String</span></span>

## <span data-ttu-id="98105-132">출력</span><span class="sxs-lookup"><span data-stu-id="98105-132">OUTPUTS</span></span>

### <span data-ttu-id="98105-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="98105-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="98105-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="98105-134">NOTES</span></span>

## <span data-ttu-id="98105-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98105-135">RELATED LINKS</span></span>

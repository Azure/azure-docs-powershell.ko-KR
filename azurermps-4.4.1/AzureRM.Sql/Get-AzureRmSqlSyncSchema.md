---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
ms.openlocfilehash: ef66de2b12cf0ea723540c392a296d2d1c482505
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527223"
---
# <span data-ttu-id="99741-101">Get-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="99741-101">Get-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="99741-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99741-102">SYNOPSIS</span></span>
<span data-ttu-id="99741-103">구성원 데이터베이스 또는 hub 데이터베이스의 동기화 스키마에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="99741-103">Returns information about the sync schema of a member database or a hub database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99741-104">구문과</span><span class="sxs-lookup"><span data-stu-id="99741-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99741-105">설명은</span><span class="sxs-lookup"><span data-stu-id="99741-105">DESCRIPTION</span></span>
<span data-ttu-id="99741-106">**Get-AzureRmSqlSyncSchema** cmdlet은 구성원 데이터베이스 또는 hub 데이터베이스의 동기화 스키마에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="99741-106">The **Get-AzureRmSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="99741-107">예제의</span><span class="sxs-lookup"><span data-stu-id="99741-107">EXAMPLES</span></span>

### <span data-ttu-id="99741-108">예제 1.1: hub 데이터베이스에 대 한 동기화 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="99741-108">Example 1.1: Get the sync schema for a hub database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="99741-109">이 명령은 동기화 그룹 syncGroup01의 hub 데이터베이스에 대 한 동기화 스키마를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="99741-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="99741-110">예제 1.2: hub 데이터베이스에 대 한 동기화 스키마 가져오기 및 테이블 확장</span><span class="sxs-lookup"><span data-stu-id="99741-110">Example 1.2: Get the sync schema for a hub database, and expand Tables</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
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

<span data-ttu-id="99741-111">이 명령은 그룹 syncGroup01 동기화 및 Tables 확장 속성에서 hub 데이터베이스에 대 한 동기화 스키마를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="99741-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="99741-112">예제 2: 구성원 데이터베이스에 대 한 동기화 스키마 가져오기</span><span class="sxs-lookup"><span data-stu-id="99741-112">Example 2: Get the sync schema for a member database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="99741-113">이 명령은 동기화 구성원 syncMember01의 구성원 데이터베이스에 대 한 동기화 스키마를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="99741-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="99741-114">변수</span><span class="sxs-lookup"><span data-stu-id="99741-114">PARAMETERS</span></span>

### <span data-ttu-id="99741-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="99741-115">-DatabaseName</span></span>
<span data-ttu-id="99741-116">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99741-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="99741-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99741-117">-ResourceGroupName</span></span>
<span data-ttu-id="99741-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99741-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="99741-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="99741-119">-ServerName</span></span>
<span data-ttu-id="99741-120">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99741-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="99741-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="99741-121">-SyncGroupName</span></span>
<span data-ttu-id="99741-122">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99741-122">The sync group name.</span></span>

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

### <span data-ttu-id="99741-123">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="99741-123">-SyncMemberName</span></span>
<span data-ttu-id="99741-124">동기화 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99741-124">The sync member name.</span></span>

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

### <span data-ttu-id="99741-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99741-125">-DefaultProfile</span></span>
<span data-ttu-id="99741-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99741-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99741-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99741-127">CommonParameters</span></span>
<span data-ttu-id="99741-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="99741-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99741-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99741-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99741-130">입력</span><span class="sxs-lookup"><span data-stu-id="99741-130">INPUTS</span></span>

## <span data-ttu-id="99741-131">출력</span><span class="sxs-lookup"><span data-stu-id="99741-131">OUTPUTS</span></span>

### <span data-ttu-id="99741-132">AzureSqlSyncFullSchemaModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="99741-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

### <span data-ttu-id="99741-133">표: Microsoft Azure. AzureSqlSyncFullSchemaTableModel를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="99741-133">Tables: Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaTableModel</span></span>

### <span data-ttu-id="99741-134">열: Microsoft Azure. AzureSqlSyncFullSchemaColumnModel를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="99741-134">Columns: Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaColumnModel</span></span>

## <span data-ttu-id="99741-135">상속자</span><span class="sxs-lookup"><span data-stu-id="99741-135">NOTES</span></span>

## <span data-ttu-id="99741-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99741-136">RELATED LINKS</span></span>


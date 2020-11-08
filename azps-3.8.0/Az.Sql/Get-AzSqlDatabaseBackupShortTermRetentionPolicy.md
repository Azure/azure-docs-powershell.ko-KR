---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d9e872ab11574f07aadfc02a4107c039e41e17e2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041557"
---
# <span data-ttu-id="dc745-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="dc745-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="dc745-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc745-102">SYNOPSIS</span></span>
<span data-ttu-id="dc745-103">단기 백업 기간 보존 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc745-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="dc745-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc745-104">SYNTAX</span></span>

### <span data-ttu-id="dc745-105">PolicyByResourceServerDatabaseSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="dc745-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc745-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dc745-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc745-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dc745-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc745-108">설명은</span><span class="sxs-lookup"><span data-stu-id="dc745-108">DESCRIPTION</span></span>
<span data-ttu-id="dc745-109">**AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet은이 데이터베이스에 등록 된 단기 보존 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc745-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="dc745-110">정책은 시간 지정 복원 백업의 보존 기간을 일 수로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc745-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="dc745-111">예제의</span><span class="sxs-lookup"><span data-stu-id="dc745-111">EXAMPLES</span></span>

### <span data-ttu-id="dc745-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="dc745-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="dc745-113">이 명령은 database01에 대 한 단기 보존 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc745-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="dc745-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="dc745-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="dc745-115">이 명령은 데이터베이스 개체에서 파이핑을 통해 database01에 대 한 단기 보존 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="dc745-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="dc745-116">변수</span><span class="sxs-lookup"><span data-stu-id="dc745-116">PARAMETERS</span></span>

### <span data-ttu-id="dc745-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="dc745-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="dc745-118">정책을 가져올 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="dc745-118">The database object to get the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc745-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dc745-119">-DatabaseName</span></span>
<span data-ttu-id="dc745-120">사용할 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc745-120">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc745-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc745-121">-DefaultProfile</span></span>
<span data-ttu-id="dc745-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc745-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc745-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc745-123">-ResourceGroupName</span></span>
<span data-ttu-id="dc745-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc745-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc745-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc745-125">-ResourceId</span></span>
<span data-ttu-id="dc745-126">단기 보존 정책 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="dc745-126">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc745-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dc745-127">-ServerName</span></span>
<span data-ttu-id="dc745-128">데이터베이스가 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc745-128">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc745-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc745-129">CommonParameters</span></span>
<span data-ttu-id="dc745-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc745-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc745-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dc745-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc745-132">입력</span><span class="sxs-lookup"><span data-stu-id="dc745-132">INPUTS</span></span>

### <span data-ttu-id="dc745-133">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="dc745-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="dc745-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dc745-134">System.String</span></span>

## <span data-ttu-id="dc745-135">출력</span><span class="sxs-lookup"><span data-stu-id="dc745-135">OUTPUTS</span></span>

### <span data-ttu-id="dc745-136">AzureSqlDatabaseBackupShortTermRetentionPolicyModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="dc745-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="dc745-137">상속자</span><span class="sxs-lookup"><span data-stu-id="dc745-137">NOTES</span></span>

## <span data-ttu-id="dc745-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc745-138">RELATED LINKS</span></span>

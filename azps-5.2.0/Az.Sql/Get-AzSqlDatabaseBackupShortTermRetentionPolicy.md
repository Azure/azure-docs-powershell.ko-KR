---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d9e872ab11574f07aadfc02a4107c039e41e17e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368565"
---
# <span data-ttu-id="36a25-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="36a25-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="36a25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36a25-102">SYNOPSIS</span></span>
<span data-ttu-id="36a25-103">백업 단기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="36a25-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="36a25-104">구문</span><span class="sxs-lookup"><span data-stu-id="36a25-104">SYNTAX</span></span>

### <span data-ttu-id="36a25-105">PolicyByResourceServerDatabaseSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="36a25-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36a25-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="36a25-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36a25-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="36a25-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36a25-108">설명</span><span class="sxs-lookup"><span data-stu-id="36a25-108">DESCRIPTION</span></span>
<span data-ttu-id="36a25-109">**Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet은 이 데이터베이스에 등록된 단기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="36a25-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="36a25-110">정책은 지정 시간 복원 백업의 보존 기간(일)입니다.</span><span class="sxs-lookup"><span data-stu-id="36a25-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="36a25-111">예제</span><span class="sxs-lookup"><span data-stu-id="36a25-111">EXAMPLES</span></span>

### <span data-ttu-id="36a25-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="36a25-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="36a25-113">이 명령은 database01에 대한 단기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="36a25-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="36a25-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="36a25-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="36a25-115">이 명령은 데이터베이스 개체의 파이핑을 통해 database01에 대한 단기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="36a25-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="36a25-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36a25-116">PARAMETERS</span></span>

### <span data-ttu-id="36a25-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="36a25-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="36a25-118">정책을 얻을 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="36a25-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="36a25-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="36a25-119">-DatabaseName</span></span>
<span data-ttu-id="36a25-120">사용할 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36a25-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="36a25-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a25-121">-DefaultProfile</span></span>
<span data-ttu-id="36a25-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36a25-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36a25-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36a25-123">-ResourceGroupName</span></span>
<span data-ttu-id="36a25-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36a25-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="36a25-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36a25-125">-ResourceId</span></span>
<span data-ttu-id="36a25-126">단기 보존 정책 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="36a25-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="36a25-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="36a25-127">-ServerName</span></span>
<span data-ttu-id="36a25-128">데이터베이스가 있는 azure SQL Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36a25-128">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="36a25-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a25-129">CommonParameters</span></span>
<span data-ttu-id="36a25-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36a25-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a25-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="36a25-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a25-132">입력</span><span class="sxs-lookup"><span data-stu-id="36a25-132">INPUTS</span></span>

### <span data-ttu-id="36a25-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="36a25-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="36a25-134">System.String</span><span class="sxs-lookup"><span data-stu-id="36a25-134">System.String</span></span>

## <span data-ttu-id="36a25-135">출력</span><span class="sxs-lookup"><span data-stu-id="36a25-135">OUTPUTS</span></span>

### <span data-ttu-id="36a25-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="36a25-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="36a25-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36a25-137">NOTES</span></span>

## <span data-ttu-id="36a25-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36a25-138">RELATED LINKS</span></span>

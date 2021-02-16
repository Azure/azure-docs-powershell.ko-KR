---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d9e872ab11574f07aadfc02a4107c039e41e17e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183356"
---
# <span data-ttu-id="adc0d-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="adc0d-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="adc0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adc0d-102">SYNOPSIS</span></span>
<span data-ttu-id="adc0d-103">백업 단기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="adc0d-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="adc0d-104">구문</span><span class="sxs-lookup"><span data-stu-id="adc0d-104">SYNTAX</span></span>

### <span data-ttu-id="adc0d-105">PolicyByResourceServerDatabaseSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="adc0d-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adc0d-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="adc0d-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adc0d-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="adc0d-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="adc0d-108">설명</span><span class="sxs-lookup"><span data-stu-id="adc0d-108">DESCRIPTION</span></span>
<span data-ttu-id="adc0d-109">**Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet은 이 데이터베이스에 등록된 단기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="adc0d-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="adc0d-110">정책은 지정 시간 복원 백업의 보존 기간(일)입니다.</span><span class="sxs-lookup"><span data-stu-id="adc0d-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="adc0d-111">예제</span><span class="sxs-lookup"><span data-stu-id="adc0d-111">EXAMPLES</span></span>

### <span data-ttu-id="adc0d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="adc0d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="adc0d-113">이 명령은 database01에 대한 단기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="adc0d-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="adc0d-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="adc0d-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="adc0d-115">이 명령은 데이터베이스 개체의 파이핑을 통해 database01에 대한 단기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="adc0d-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="adc0d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adc0d-116">PARAMETERS</span></span>

### <span data-ttu-id="adc0d-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="adc0d-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="adc0d-118">정책을 얻을 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="adc0d-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="adc0d-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="adc0d-119">-DatabaseName</span></span>
<span data-ttu-id="adc0d-120">사용할 Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adc0d-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="adc0d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc0d-121">-DefaultProfile</span></span>
<span data-ttu-id="adc0d-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="adc0d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adc0d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adc0d-123">-ResourceGroupName</span></span>
<span data-ttu-id="adc0d-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adc0d-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="adc0d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adc0d-125">-ResourceId</span></span>
<span data-ttu-id="adc0d-126">단기 보존 정책 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="adc0d-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="adc0d-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="adc0d-127">-ServerName</span></span>
<span data-ttu-id="adc0d-128">데이터베이스가 있는 azure SQL Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adc0d-128">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="adc0d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc0d-129">CommonParameters</span></span>
<span data-ttu-id="adc0d-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="adc0d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc0d-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="adc0d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc0d-132">입력</span><span class="sxs-lookup"><span data-stu-id="adc0d-132">INPUTS</span></span>

### <span data-ttu-id="adc0d-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="adc0d-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="adc0d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="adc0d-134">System.String</span></span>

## <span data-ttu-id="adc0d-135">출력</span><span class="sxs-lookup"><span data-stu-id="adc0d-135">OUTPUTS</span></span>

### <span data-ttu-id="adc0d-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="adc0d-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="adc0d-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="adc0d-137">NOTES</span></span>

## <span data-ttu-id="adc0d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="adc0d-138">RELATED LINKS</span></span>

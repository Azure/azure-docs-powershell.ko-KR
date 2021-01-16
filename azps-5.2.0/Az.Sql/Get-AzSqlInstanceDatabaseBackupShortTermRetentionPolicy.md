---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 3666fd9c790f5445f83c3a068e7423b64a172c5f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325793"
---
# <span data-ttu-id="4ae0c-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="4ae0c-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="4ae0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ae0c-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae0c-103">백업 단기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="4ae0c-104">구문</span><span class="sxs-lookup"><span data-stu-id="4ae0c-104">SYNTAX</span></span>

### <span data-ttu-id="4ae0c-105">PolicyByResourceInstanceDatabaseSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4ae0c-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ae0c-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4ae0c-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ae0c-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4ae0c-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ae0c-108">설명</span><span class="sxs-lookup"><span data-stu-id="4ae0c-108">DESCRIPTION</span></span>
<span data-ttu-id="4ae0c-109">**Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet은 이 데이터베이스에 등록된 단기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="4ae0c-110">정책은 지정 시간 복원 백업의 보존 기간(일)입니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="4ae0c-111">예제</span><span class="sxs-lookup"><span data-stu-id="4ae0c-111">EXAMPLES</span></span>

### <span data-ttu-id="4ae0c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="4ae0c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="4ae0c-113">이 명령은 database01에 대한 단기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="4ae0c-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="4ae0c-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="4ae0c-115">이 명령은 데이터베이스 개체의 파이핑을 통해 database01에 대한 단기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="4ae0c-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="4ae0c-116">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 7

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 7
```

<span data-ttu-id="4ae0c-117">이 명령은 삭제된 데이터베이스 개체의 파이핑을 통해 database01이라는 모든 삭제된 데이터베이스에 대한 단기 보존 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="4ae0c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ae0c-118">PARAMETERS</span></span>

### <span data-ttu-id="4ae0c-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4ae0c-119">-DatabaseName</span></span>
<span data-ttu-id="4ae0c-120">백업을 검색할 Azure SQL Instance 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae0c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae0c-121">-DefaultProfile</span></span>
<span data-ttu-id="4ae0c-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ae0c-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="4ae0c-123">-DeletionDate</span></span>
<span data-ttu-id="4ae0c-124">밀리초 정밀도(예: 2016-02-23T00:21:22.847Z)를 사용하여 백업을 검색할 Azure SQL Instance Database의 지운 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae0c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ae0c-125">-InputObject</span></span>
<span data-ttu-id="4ae0c-126">정책을 얻거나 설정할 라이브 또는 삭제된 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-126">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae0c-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4ae0c-127">-InstanceName</span></span>
<span data-ttu-id="4ae0c-128">데이터베이스가 있는 Azure SQL Managed Instance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae0c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ae0c-129">-ResourceGroupName</span></span>
<span data-ttu-id="4ae0c-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ae0c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ae0c-131">-ResourceId</span></span>
<span data-ttu-id="4ae0c-132">단기 보존 정책 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-132">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="4ae0c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae0c-133">CommonParameters</span></span>
<span data-ttu-id="4ae0c-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae0c-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4ae0c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae0c-136">입력</span><span class="sxs-lookup"><span data-stu-id="4ae0c-136">INPUTS</span></span>

### <span data-ttu-id="4ae0c-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="4ae0c-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="4ae0c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4ae0c-138">System.String</span></span>

## <span data-ttu-id="4ae0c-139">출력</span><span class="sxs-lookup"><span data-stu-id="4ae0c-139">OUTPUTS</span></span>

### <span data-ttu-id="4ae0c-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="4ae0c-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="4ae0c-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4ae0c-141">NOTES</span></span>

## <span data-ttu-id="4ae0c-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ae0c-142">RELATED LINKS</span></span>

---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045423"
---
# <span data-ttu-id="01228-101">Start-AzureSqlDatabaseRecovery</span><span class="sxs-lookup"><span data-stu-id="01228-101">Start-AzureSqlDatabaseRecovery</span></span>

## <span data-ttu-id="01228-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01228-102">SYNOPSIS</span></span>
<span data-ttu-id="01228-103">데이터베이스에 대 한 복원 요청을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-103">Initiates a restore request for a database.</span></span>

## <span data-ttu-id="01228-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01228-104">SYNTAX</span></span>

### <span data-ttu-id="01228-105">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="01228-105">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="01228-106">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="01228-106">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="01228-107">설명은</span><span class="sxs-lookup"><span data-stu-id="01228-107">DESCRIPTION</span></span>
<span data-ttu-id="01228-108">**AzureSqlDatabaseRecovery** cmdlet은 활성 또는 삭제 된 데이터베이스에 대 한 복원 요청을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-108">The **Start-AzureSqlDatabaseRecovery** cmdlet initiates a restore request for a live or dropped database.</span></span>
<span data-ttu-id="01228-109">이 cmdlet은 데이터베이스에 대해 마지막으로 사용 가능한 백업을 사용 하는 기본 복구를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-109">This cmdlet supports basic recovery that uses the last known available backup for the database.</span></span>
<span data-ttu-id="01228-110">복구 작업에서 새 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01228-110">The recovery operation creates a new database.</span></span>
<span data-ttu-id="01228-111">동일한 서버에서 라이브 데이터베이스를 복구 하는 경우 새 데이터베이스에 대해 다른 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-111">If you recover a live database on the same server, you must specify a different name for the new database.</span></span>

<span data-ttu-id="01228-112">데이터베이스에 대 한 특정 시점 복원을 수행 하려면 **AzureSqlDatabaseRestore** cmdlet을 대신 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-112">To do a point in time restore for a database, use the **Start-AzureSqlDatabaseRestore** cmdlet instead.</span></span>

## <span data-ttu-id="01228-113">예제의</span><span class="sxs-lookup"><span data-stu-id="01228-113">EXAMPLES</span></span>

### <span data-ttu-id="01228-114">예제 1: 개체로 지정 된 데이터베이스 복구</span><span class="sxs-lookup"><span data-stu-id="01228-114">Example 1: Recover a database specified as an object</span></span>
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="01228-115">첫 번째 명령은 **AzureSqlRecoverableDatabase** cmdlet을 사용 하 여 데이터베이스 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="01228-115">The first command gets a database object by using the **Get-AzureSqlRecoverableDatabase** cmdlet.</span></span>
<span data-ttu-id="01228-116">명령이 $Database 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-116">The command stores that object in the $Database variable.</span></span>

<span data-ttu-id="01228-117">두 번째 명령은 $Database에 저장 된 데이터베이스를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-117">The second command recovers the database stored in $Database.</span></span>

### <span data-ttu-id="01228-118">예제 2: 이름으로 지정 된 데이터베이스 복구</span><span class="sxs-lookup"><span data-stu-id="01228-118">Example 2: Recover a database specified by name</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

<span data-ttu-id="01228-119">이 명령은 데이터베이스 이름을 사용 하 여 데이터베이스를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-119">This command recovers a database using the database name.</span></span>

## <span data-ttu-id="01228-120">변수</span><span class="sxs-lookup"><span data-stu-id="01228-120">PARAMETERS</span></span>

### <span data-ttu-id="01228-121">-프로필</span><span class="sxs-lookup"><span data-stu-id="01228-121">-Profile</span></span>
<span data-ttu-id="01228-122">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="01228-123">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="01228-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01228-124">-원본 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="01228-124">-SourceDatabase</span></span>
<span data-ttu-id="01228-125">이 cmdlet이 복구 하는 데이터베이스를 나타내는 database 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-125">Specifies the database object that represents the database that this cmdlet recovers.</span></span>

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01228-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="01228-126">-SourceDatabaseName</span></span>
<span data-ttu-id="01228-127">이 cmdlet이 복구 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-127">Specifies the name of the database that this cmdlet recovers.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01228-128">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="01228-128">-SourceServerName</span></span>
<span data-ttu-id="01228-129">원본 데이터베이스가 실시간으로 실행 되는 서버의 이름을 지정 하거나 원본 데이터베이스를 삭제 하기 전에 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-129">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01228-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="01228-130">-TargetDatabaseName</span></span>
<span data-ttu-id="01228-131">복구 된 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-131">Specifies the name of the recovered database.</span></span>
<span data-ttu-id="01228-132">원본 데이터베이스가 여전히 활성 상태인 경우 동일한 서버로 복구 하려면 원본 데이터베이스 이름과 다른 이름을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-132">If the source database is still live, in order to recover it to the same server, you must specify a name that differs from the source database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01228-133">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="01228-133">-TargetServerName</span></span>
<span data-ttu-id="01228-134">데이터베이스를 복원할 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-134">Specifies the name of the server to which to restore a database.</span></span>
<span data-ttu-id="01228-135">데이터베이스를 동일한 서버나 다른 서버로 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="01228-135">You can restore a database to the same server or to a different server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01228-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01228-136">CommonParameters</span></span>
<span data-ttu-id="01228-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01228-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01228-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01228-139">입력</span><span class="sxs-lookup"><span data-stu-id="01228-139">INPUTS</span></span>

### <span data-ttu-id="01228-140">WindowsAzure를 RecoverableDatabase 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-140">Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase</span></span>

## <span data-ttu-id="01228-141">출력</span><span class="sxs-lookup"><span data-stu-id="01228-141">OUTPUTS</span></span>

### <span data-ttu-id="01228-142">WindowsAzure를 RecoverDatabaseOperation 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-142">Microsoft.WindowsAzure.Management.Sql.Models.RecoverDatabaseOperation</span></span>

## <span data-ttu-id="01228-143">상속자</span><span class="sxs-lookup"><span data-stu-id="01228-143">NOTES</span></span>
* <span data-ttu-id="01228-144">이 cmdlet을 실행 하려면 인증서 기반 인증을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-144">You must use certificate-based authentication to run this cmdlet.</span></span> <span data-ttu-id="01228-145">이 cmdlet을 실행 하는 컴퓨터에서 다음 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="01228-145">Run the following commands on the computer where you run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="01228-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01228-146">RELATED LINKS</span></span>

[<span data-ttu-id="01228-147">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="01228-147">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="01228-148">데이터베이스 복구 요청 만들기</span><span class="sxs-lookup"><span data-stu-id="01228-148">Create Database Recovery Request</span></span>](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[<span data-ttu-id="01228-149">Azure SQL 데이터베이스의 지리적 복제</span><span class="sxs-lookup"><span data-stu-id="01228-149">Geo-Replication in Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[<span data-ttu-id="01228-150">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="01228-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="01228-151">Get-AzureSqlRecoverableDatabase</span><span class="sxs-lookup"><span data-stu-id="01228-151">Get-AzureSqlRecoverableDatabase</span></span>](./Get-AzureSqlRecoverableDatabase.md)

[<span data-ttu-id="01228-152">시작-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="01228-152">Start-AzureSqlDatabaseRestore</span></span>](./Start-AzureSqlDatabaseRestore.md)



---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7716587787515221a6e016436a6e3d030c1ab0eb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405621"
---
# <span data-ttu-id="445aa-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="445aa-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="445aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="445aa-102">SYNOPSIS</span></span>
<span data-ttu-id="445aa-103">연속 복사 관계를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="445aa-104">구문</span><span class="sxs-lookup"><span data-stu-id="445aa-104">SYNTAX</span></span>

### <span data-ttu-id="445aa-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="445aa-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="445aa-106">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="445aa-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="445aa-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="445aa-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="445aa-108">설명</span><span class="sxs-lookup"><span data-stu-id="445aa-108">DESCRIPTION</span></span>
<span data-ttu-id="445aa-109">**Stop-AzureSqlDatabaseCopy** cmdlet은 연속 복사 관계를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="445aa-110">이 cmdlet은 원본 데이터베이스와 보조 또는 대상 데이터베이스 간의 데이터 이동을 중지한 다음 보조 데이터베이스의 상태를 독립 실행형 온라인 데이터베이스로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="445aa-111">데이터 손실이 가능한 경우 연속 복사 관계, 종료 또는 계획된 종료 및 강제 종료를 종료하는 두 가지 방법이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="445aa-112">원본 데이터베이스를 호스트하는 서버에서 종료 또는 강제 종료 모드에서 이 cmdlet을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="445aa-113">보조 데이터베이스를 호스트하는 서버에서 강제 종료 모드를 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="445aa-114">계획된 종료는 cmdlet을 실행할 때 원본 데이터베이스의 모든 커밋된 트랜잭션이 보조 데이터베이스에 복제될 때까지 대기합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="445aa-115">강제 종료는 미해결 커밋된 트랜잭션의 복제를 기다릴 수 없습니다. 보조 데이터베이스에서 가능한 데이터 손실이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="445aa-116">복제 상태가 보류 중인 동안 강제 종료만 연속 복사 관계를 성공적으로 종료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="445aa-117">복제 상태가 보류 중이면 강제로 종료되지 않는 종료는 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="445aa-118">예제</span><span class="sxs-lookup"><span data-stu-id="445aa-118">EXAMPLES</span></span>

### <span data-ttu-id="445aa-119">예제 1: 연속 복사 관계 종료</span><span class="sxs-lookup"><span data-stu-id="445aa-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="445aa-120">이 명령은 lpqd0zbr8y라는 서버에서 Orders라는 데이터베이스의 연속 복사 관계를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="445aa-121">bk0b8kf658이라는 서버는 보조 데이터베이스를 호스트합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="445aa-122">예제 2: 연속 복사 관계의 종료</span><span class="sxs-lookup"><span data-stu-id="445aa-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="445aa-123">첫 번째 명령은 lpqd0zbr8y라는 서버에서 Orders라는 데이터베이스에 대한 데이터베이스 복사 관계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="445aa-124">두 번째 명령은 보조 데이터베이스를 호스트하는 서버에서 연속 복사 관계를 억지로 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="445aa-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="445aa-125">PARAMETERS</span></span>

### <span data-ttu-id="445aa-126">-Database</span><span class="sxs-lookup"><span data-stu-id="445aa-126">-Database</span></span>
<span data-ttu-id="445aa-127">원본 Azure SQL 데이터베이스를 나타내는 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="445aa-128">이 cmdlet은 이 매개 변수가 지정하는 데이터베이스의 연속 복사 관계를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="445aa-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="445aa-129">-DatabaseCopy</span></span>
<span data-ttu-id="445aa-130">데이터베이스를 나타내는 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="445aa-131">이 cmdlet은 이 매개 변수가 지정하는 데이터베이스의 연속 복사 관계를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="445aa-132">이 매개 변수는 파이프라인 입력을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-132">This parameter accepts pipeline input.</span></span>

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="445aa-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="445aa-133">-DatabaseName</span></span>
<span data-ttu-id="445aa-134">데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-134">Specifies the name of a database.</span></span>
<span data-ttu-id="445aa-135">이 cmdlet은 이 매개 변수가 지정하는 데이터베이스의 연속 복사 관계를 종료합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445aa-136">-Force</span><span class="sxs-lookup"><span data-stu-id="445aa-136">-Force</span></span>
<span data-ttu-id="445aa-137">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-137">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445aa-138">-ForcedTermination</span><span class="sxs-lookup"><span data-stu-id="445aa-138">-ForcedTermination</span></span>
<span data-ttu-id="445aa-139">이 cmdlet이 강제로 연속 복사 관계가 종료되는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="445aa-140">강제 종료로 인해 데이터 손실이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="445aa-141">대상 데이터베이스를 호스트하는 서버에서 이 cmdlet을 실행하려면 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="445aa-142">원본 데이터베이스를 호스트하는 서버에서 이 cmdlet을 실행하려면 보조 데이터베이스를 사용할 수 없는 경우 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445aa-143">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="445aa-143">-PartnerDatabase</span></span>
<span data-ttu-id="445aa-144">보조 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="445aa-145">이름을 지정하는 경우 원본 데이터베이스의 이름과 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-145">If you specify a name, it must match the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445aa-146">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="445aa-146">-PartnerServer</span></span>
<span data-ttu-id="445aa-147">대상 데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-147">Specifies the name of the server that hosts the target database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445aa-148">-Profile</span><span class="sxs-lookup"><span data-stu-id="445aa-148">-Profile</span></span>
<span data-ttu-id="445aa-149">이 cmdlet이 읽을 Azure 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="445aa-150">프로필을 지정하지 않으면 이 cmdlet은 로컬 기본 프로필에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="445aa-151">-ServerName</span><span class="sxs-lookup"><span data-stu-id="445aa-151">-ServerName</span></span>
<span data-ttu-id="445aa-152">원본 데이터베이스가 있는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-152">Specifies the name of the server on which the source database resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="445aa-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="445aa-153">-Confirm</span></span>
<span data-ttu-id="445aa-154">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445aa-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="445aa-155">-WhatIf</span></span>
<span data-ttu-id="445aa-156">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="445aa-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="445aa-157">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445aa-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="445aa-158">CommonParameters</span></span>
<span data-ttu-id="445aa-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="445aa-160">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="445aa-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="445aa-161">입력</span><span class="sxs-lookup"><span data-stu-id="445aa-161">INPUTS</span></span>

### <span data-ttu-id="445aa-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="445aa-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="445aa-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="445aa-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="445aa-164">출력</span><span class="sxs-lookup"><span data-stu-id="445aa-164">OUTPUTS</span></span>

### <span data-ttu-id="445aa-165">없음</span><span class="sxs-lookup"><span data-stu-id="445aa-165">None</span></span>

## <span data-ttu-id="445aa-166">참고 사항</span><span class="sxs-lookup"><span data-stu-id="445aa-166">NOTES</span></span>
* <span data-ttu-id="445aa-167">인증: 이 cmdlet에는 인증서 기반 인증이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="445aa-168">인증서 기반 인증을 사용하여 현재 구독을 설정하는 방법의 예제는 **New-AzureSqlDatabaseServerContext** cmdlet을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="445aa-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="445aa-169">제한 사항: 보조 데이터베이스를 호스트하는 서버에서 강제 종료만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="445aa-170">이전 보조 데이터베이스에 대한 종료의 영향: 종료 후 보조 데이터베이스는 독립 데이터베이스가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="445aa-171">보조 데이터베이스에서 이미 시드가 완료된 경우 종료 후 이 데이터베이스가 전체 액세스에 대해 열려 있습니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="445aa-172">원본 데이터베이스가 읽기-쓰기 데이터베이스인 경우 이전 보조 데이터베이스도 읽기-쓰기 데이터베이스가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="445aa-173">시드가 현재 진행 중인 경우 시드가 중단되고 이전 보조 데이터베이스는 보조 데이터베이스를 호스트하는 서버에서 표시되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="445aa-174">원본 데이터베이스를 읽기 전용 모드로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="445aa-175">이렇게 하면 종료 후 원본 및 보조 데이터베이스가 동기화될 수 있으며 종료하는 동안 트랜잭션이 커밋되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="445aa-176">종료가 완료되면 원본을 다시 읽기-쓰기 모드로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="445aa-177">선택적으로 이전 보조 데이터베이스를 읽기-쓰기 모드로 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="445aa-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="445aa-178">모니터링: 연속 복사 관계의 원본 및 대상 모두에서 작업의 상태를 확인하기 위해 **Get-AzureSqlDatabaseOperation** cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="445aa-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="445aa-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="445aa-179">RELATED LINKS</span></span>

[<span data-ttu-id="445aa-180">Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="445aa-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="445aa-181">Azure SQL 데이터베이스에 대한 작업</span><span class="sxs-lookup"><span data-stu-id="445aa-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="445aa-182">데이터베이스 복사 중지</span><span class="sxs-lookup"><span data-stu-id="445aa-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)



[<span data-ttu-id="445aa-183">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="445aa-183">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="445aa-184">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="445aa-184">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)



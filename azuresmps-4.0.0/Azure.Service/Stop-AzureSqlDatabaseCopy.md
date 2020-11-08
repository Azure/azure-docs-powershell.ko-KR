---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046403"
---
# <span data-ttu-id="caffa-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="caffa-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="caffa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caffa-102">SYNOPSIS</span></span>
<span data-ttu-id="caffa-103">연속 복사 관계를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="caffa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="caffa-104">SYNTAX</span></span>

### <span data-ttu-id="caffa-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="caffa-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caffa-106">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="caffa-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="caffa-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="caffa-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="caffa-108">설명은</span><span class="sxs-lookup"><span data-stu-id="caffa-108">DESCRIPTION</span></span>
<span data-ttu-id="caffa-109">**AzureSqlDatabaseCopy** cmdlet은 연속 복사 관계를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="caffa-110">이 cmdlet은 원본 데이터베이스와 보조 또는 대상 데이터베이스 간의 데이터 이동을 중지 한 다음 보조 데이터베이스의 상태를 독립 실행형 온라인 데이터베이스로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="caffa-111">연속 복사 관계, 종료 또는 계획 된 종료 및 데이터 손실 가능성을 가진 강제 종료를 두 가지 방법으로 끝낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="caffa-112">원본 데이터베이스를 호스트 하는 서버에서이 cmdlet을 종료 또는 강제 종료 모드에서 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="caffa-113">보조 데이터베이스를 호스팅하는 서버에서 강제 종료 모드를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="caffa-114">계획 된 종료는 cmdlet을 실행할 때 원본 데이터베이스에서 커밋된 모든 트랜잭션이 보조 데이터베이스로 복제 될 때까지 대기 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="caffa-115">강제 종료는 처리 되지 않은 커밋된 거래의 복제를 기다리지 않으며 보조 데이터베이스에서 가능한 데이터 손실을 유발할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="caffa-116">복제 상태가 보류 중 이지만 강제 종료는 연속 복사 관계를 성공적으로 종료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="caffa-117">복제 상태가 보류 중인 경우 강제 적용 되지 않는 종료는 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="caffa-118">예제의</span><span class="sxs-lookup"><span data-stu-id="caffa-118">EXAMPLES</span></span>

### <span data-ttu-id="caffa-119">예제 1: 연속 복사 관계 종료</span><span class="sxs-lookup"><span data-stu-id="caffa-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="caffa-120">이 명령은 lpqd0zbr8y 이라는 서버에서 Order 라는 데이터베이스의 연속 복사 관계를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="caffa-121">Bk0b8kf658 라는 서버는 보조 데이터베이스를 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="caffa-122">예제 2: 연속 복사 관계 강제 종료</span><span class="sxs-lookup"><span data-stu-id="caffa-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="caffa-123">첫 번째 명령은 lpqd0zbr8y 이라는 서버에서 Order 라는 데이터베이스의 데이터베이스 복사 관계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="caffa-124">두 번째 명령은 보조 데이터베이스를 호스트 하는 서버에서 연속 복사 관계를 강제로 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="caffa-125">변수</span><span class="sxs-lookup"><span data-stu-id="caffa-125">PARAMETERS</span></span>

### <span data-ttu-id="caffa-126">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="caffa-126">-Database</span></span>
<span data-ttu-id="caffa-127">원본 Azure SQL 데이터베이스를 나타내는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="caffa-128">이 cmdlet은이 매개 변수에서 지정 하는 데이터베이스의 연속 복사 관계를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="caffa-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="caffa-129">-DatabaseCopy</span></span>
<span data-ttu-id="caffa-130">데이터베이스를 나타내는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="caffa-131">이 cmdlet은이 매개 변수에서 지정 하는 데이터베이스의 연속 복사 관계를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="caffa-132">이 매개 변수는 파이프라인 입력을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-132">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="caffa-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="caffa-133">-DatabaseName</span></span>
<span data-ttu-id="caffa-134">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-134">Specifies the name of a database.</span></span>
<span data-ttu-id="caffa-135">이 cmdlet은이 매개 변수에서 지정 하는 데이터베이스의 연속 복사 관계를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="caffa-136">-Force</span><span class="sxs-lookup"><span data-stu-id="caffa-136">-Force</span></span>
<span data-ttu-id="caffa-137">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-137">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="caffa-138">-ForcedTermination</span><span class="sxs-lookup"><span data-stu-id="caffa-138">-ForcedTermination</span></span>
<span data-ttu-id="caffa-139">이 cmdlet이 연속 복사 관계의 강제 종료를 발생 시키는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="caffa-140">강제 종료로 인해 데이터가 손실 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="caffa-141">대상 데이터베이스를 호스트 하는 서버에서이 cmdlet을 실행 하려면이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="caffa-142">원본 데이터베이스를 호스트 하는 서버에서이 cmdlet을 실행 하려면 보조 데이터베이스를 사용할 수 없는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

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

### <span data-ttu-id="caffa-143">-데이터 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="caffa-143">-PartnerDatabase</span></span>
<span data-ttu-id="caffa-144">보조 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="caffa-145">이름을 지정 하는 경우에는 원본 데이터베이스의 이름과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-145">If you specify a name, it must match the name of the source database.</span></span>

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

### <span data-ttu-id="caffa-146">-또는 서버</span><span class="sxs-lookup"><span data-stu-id="caffa-146">-PartnerServer</span></span>
<span data-ttu-id="caffa-147">대상 데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-147">Specifies the name of the server that hosts the target database.</span></span>

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

### <span data-ttu-id="caffa-148">-프로필</span><span class="sxs-lookup"><span data-stu-id="caffa-148">-Profile</span></span>
<span data-ttu-id="caffa-149">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="caffa-150">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="caffa-151">-ServerName</span><span class="sxs-lookup"><span data-stu-id="caffa-151">-ServerName</span></span>
<span data-ttu-id="caffa-152">원본 데이터베이스가 상주 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-152">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="caffa-153">-확인</span><span class="sxs-lookup"><span data-stu-id="caffa-153">-Confirm</span></span>
<span data-ttu-id="caffa-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caffa-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caffa-155">-WhatIf</span></span>
<span data-ttu-id="caffa-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caffa-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caffa-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caffa-158">CommonParameters</span></span>
<span data-ttu-id="caffa-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caffa-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caffa-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caffa-161">입력</span><span class="sxs-lookup"><span data-stu-id="caffa-161">INPUTS</span></span>

### <span data-ttu-id="caffa-162">WindowsAzure. SqlDatabase. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="caffa-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="caffa-163">WindowsAzure. SqlDatabase. \* 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="caffa-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="caffa-164">출력</span><span class="sxs-lookup"><span data-stu-id="caffa-164">OUTPUTS</span></span>

### <span data-ttu-id="caffa-165">않아야</span><span class="sxs-lookup"><span data-stu-id="caffa-165">None</span></span>

## <span data-ttu-id="caffa-166">상속자</span><span class="sxs-lookup"><span data-stu-id="caffa-166">NOTES</span></span>
* <span data-ttu-id="caffa-167">인증:이 cmdlet을 사용 하려면 인증서 기반 인증이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="caffa-168">인증서 기반 인증을 사용 하 여 현재 구독을 설정 하는 방법의 예는 **AzureSqlDatabaseServerContext** cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="caffa-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="caffa-169">제한: 보조 데이터베이스를 호스트 하는 서버에서 강제 종료만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="caffa-170">이전 보조 데이터베이스의 종료에 대 한 영향: 종료 후 보조 데이터베이스가 독립 데이터베이스가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="caffa-171">보조 데이터베이스에서 시드가 이미 완료 된 경우이 데이터베이스는 전체 액세스 권한이 열려 있습니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="caffa-172">원본 데이터베이스가 읽기-쓰기 데이터베이스인 경우 이전 보조 데이터베이스도 읽기/쓰기 데이터베이스가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="caffa-173">현재 시드가 진행 중인 경우 시드가 중단 되 고, 보조 데이터베이스를 호스트 하는 서버에 이전 보조 데이터베이스가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="caffa-174">원본 데이터베이스를 읽기 전용 모드로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="caffa-175">이렇게 하면 원본 및 보조 데이터베이스가 종료 된 후에 동기화 되며 종료 중에 트랜잭션이 커밋되지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="caffa-176">종료가 완료 되 면 원본을 읽기-쓰기 모드로 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="caffa-177">필요에 따라 이전 보조 데이터베이스를 읽기-쓰기 모드로 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="caffa-178">모니터링: 연속 복사 관계의 원본 및 대상 모두에서 작업의 상태를 확인 하려면 **AzureSqlDatabaseOperation** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="caffa-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="caffa-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="caffa-179">RELATED LINKS</span></span>

[<span data-ttu-id="caffa-180">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="caffa-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="caffa-181">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="caffa-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="caffa-182">데이터베이스 복사본 중지</span><span class="sxs-lookup"><span data-stu-id="caffa-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[<span data-ttu-id="caffa-183">Azure SQL 데이터베이스 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="caffa-183">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="caffa-184">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="caffa-184">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="caffa-185">시작-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="caffa-185">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)



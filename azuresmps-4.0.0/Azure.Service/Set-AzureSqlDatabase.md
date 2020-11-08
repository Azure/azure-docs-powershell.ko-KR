---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 82F4DB8F-8DAF-40D2-8031-3EDBF5D08417
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6274d3851042c15791707807471ae1bc6a2733ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045865"
---
# <span data-ttu-id="32645-101">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="32645-101">Set-AzureSqlDatabase</span></span>

## <span data-ttu-id="32645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32645-102">SYNOPSIS</span></span>
<span data-ttu-id="32645-103">Azure SQL 데이터베이스에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-103">Sets properties for an Azure SQL Database.</span></span>

## <span data-ttu-id="32645-104">구문과</span><span class="sxs-lookup"><span data-stu-id="32645-104">SYNTAX</span></span>

### <span data-ttu-id="32645-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="32645-105">ByNameWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32645-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="32645-106">ByObjectWithConnectionContext</span></span>
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32645-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="32645-107">ByNameWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32645-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="32645-108">ByObjectWithServerName</span></span>
```
Set-AzureSqlDatabase -ServerName <String> -Database <Database> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32645-109">설명은</span><span class="sxs-lookup"><span data-stu-id="32645-109">DESCRIPTION</span></span>
<span data-ttu-id="32645-110">**Set-AzureSqlDatabase** Cmdlet은 Azure SQL 데이터베이스의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-110">The **Set-AzureSqlDatabase** cmdlet sets properties for an Azure SQL Database.</span></span>
<span data-ttu-id="32645-111">이름을 기준으로 데이터베이스를 지정 하거나 파이프라인을 통해 Azure SQL 데이터베이스 개체를 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32645-111">You can specify the database by name, or pass an Azure SQL Database object through the pipeline.</span></span>
<span data-ttu-id="32645-112">이름을 기준으로 서버를 지정 하거나 Azure SQL 데이터베이스 서버 연결 컨텍스트를 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32645-112">You can specify the server by name, or pass an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="32645-113">**새 AzureSqlDatabaseServerContext** cmdlet을 실행 하 여 연결 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32645-113">Create a connection context by running the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="32645-114">서버를 이름으로 지정 하는 경우 cmdlet은 현재 Azure 구독 정보를 사용 하 여 요청을 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-114">If you specify the server by name, the cmdlet uses the current Azure subscription information to authenticate the request.</span></span>

## <span data-ttu-id="32645-115">예제의</span><span class="sxs-lookup"><span data-stu-id="32645-115">EXAMPLES</span></span>

### <span data-ttu-id="32645-116">예제 1: 연결 컨텍스트를 사용 하 여 데이터베이스 크기 변경</span><span class="sxs-lookup"><span data-stu-id="32645-116">Example 1: Change the size of a database by using a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ConnectionContext $Context -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="32645-117">이 예제에서는 Azure SQL 데이터베이스 서버 연결 컨텍스트 $Context에서 Database01 이라는 데이터베이스의 크기를 20gb로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-117">This example changes the size of the database named Database01 to 20 GB, in the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="32645-118">예제 2: 서버 이름을 사용 하 여 데이터베이스 크기 변경</span><span class="sxs-lookup"><span data-stu-id="32645-118">Example 2: Change the size of a database by using a server name</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ServerName "lpqd0zbr8y" -Database $Database01 -MaxSizeGB 20
```

<span data-ttu-id="32645-119">이 예제에서는 lpqd0zbr8y 이라는 서버에서 Database01 이라는 데이터베이스의 크기를 20gb로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-119">This example changes the size of the database named Database01 to 20 GB in the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="32645-120">변수</span><span class="sxs-lookup"><span data-stu-id="32645-120">PARAMETERS</span></span>

### <span data-ttu-id="32645-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="32645-121">-ConnectionContext</span></span>
<span data-ttu-id="32645-122">서버의 연결 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-122">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32645-123">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="32645-123">-Database</span></span>
<span data-ttu-id="32645-124">이 cmdlet이 수정 하는 Azure SQL 데이터베이스를 나타내는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-124">Specifies an object that represents the Azure SQL Database that this cmdlet modifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32645-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="32645-125">-DatabaseName</span></span>
<span data-ttu-id="32645-126">이 cmdlet이 수정 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-126">Specifies the name of the database that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32645-127">-에디션</span><span class="sxs-lookup"><span data-stu-id="32645-127">-Edition</span></span>
<span data-ttu-id="32645-128">Azure SQL 데이터베이스에 대 한 새 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-128">Specifies the new edition for the Azure SQL Database.</span></span>
<span data-ttu-id="32645-129">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="32645-129">Valid values are:</span></span> 

- <span data-ttu-id="32645-130">않아야</span><span class="sxs-lookup"><span data-stu-id="32645-130">None</span></span>
- <span data-ttu-id="32645-131">웹</span><span class="sxs-lookup"><span data-stu-id="32645-131">Web</span></span>
- <span data-ttu-id="32645-132">조직</span><span class="sxs-lookup"><span data-stu-id="32645-132">Business</span></span>
- <span data-ttu-id="32645-133">기본적</span><span class="sxs-lookup"><span data-stu-id="32645-133">Basic</span></span>
- <span data-ttu-id="32645-134">표준이</span><span class="sxs-lookup"><span data-stu-id="32645-134">Standard</span></span>
-  <span data-ttu-id="32645-135">Premium</span><span class="sxs-lookup"><span data-stu-id="32645-135">Premium</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32645-136">-Force</span><span class="sxs-lookup"><span data-stu-id="32645-136">-Force</span></span>
<span data-ttu-id="32645-137">확인 메시지를 표시 하지 않고 작업을 완료할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32645-137">Allows the action to complete without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="32645-138">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="32645-138">-MaxSizeBytes</span></span>
<span data-ttu-id="32645-139">데이터베이스의 새로운 최대 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-139">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="32645-140">이 매개 변수 또는 *Maxsizegb* 매개 변수 중 하나를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32645-140">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="32645-141">에디션에 기반 하 여 허용 되는 값은 *Maxsizegb* 매개 변수를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="32645-141">See the *MaxSizeGB* parameter for acceptable values based on edition.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32645-142">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="32645-142">-MaxSizeGB</span></span>
<span data-ttu-id="32645-143">데이터베이스의 새 최대 크기 (기가바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-143">Specifies the new maximum size for the database in gigabytes.</span></span>
<span data-ttu-id="32645-144">이 매개 변수 또는 *Maxsizebytes* 매개 변수 중 하나를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32645-144">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="32645-145">허용 되는 값은 버전에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="32645-145">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="32645-146">기본 에디션 값: 1 또는 2</span><span class="sxs-lookup"><span data-stu-id="32645-146">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="32645-147">스탠더드 버전 값: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 또는 250</span><span class="sxs-lookup"><span data-stu-id="32645-147">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="32645-148">Premium Edition 값: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, 500</span><span class="sxs-lookup"><span data-stu-id="32645-148">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="32645-149">웹 버전 값: 1 또는 5</span><span class="sxs-lookup"><span data-stu-id="32645-149">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="32645-150">Business Edition values: 10, 20, 30, 40, 50, 100 또는 150</span><span class="sxs-lookup"><span data-stu-id="32645-150">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32645-151">-NewDatabaseName</span><span class="sxs-lookup"><span data-stu-id="32645-151">-NewDatabaseName</span></span>
<span data-ttu-id="32645-152">데이터베이스의 새 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-152">Specifies the new name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32645-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32645-153">-PassThru</span></span>
<span data-ttu-id="32645-154">업데이트 된 Azure SQL 데이터베이스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-154">Returns the updated Azure SQL Database.</span></span>

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

### <span data-ttu-id="32645-155">-프로필</span><span class="sxs-lookup"><span data-stu-id="32645-155">-Profile</span></span>
<span data-ttu-id="32645-156">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="32645-157">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="32645-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="32645-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="32645-158">-ServerName</span></span>
<span data-ttu-id="32645-159">이 cmdlet이 수정 하는 데이터베이스를 포함 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-159">Specifies the name of the server that contains the database that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32645-160">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="32645-160">-ServiceObjective</span></span>
<span data-ttu-id="32645-161">이 데이터베이스에 대 한 새 서비스 목표 (성능 수준)를 나타내는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-161">Specifies an object representing the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="32645-162">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="32645-162">Valid values are:</span></span> 

- <span data-ttu-id="32645-163">기본: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span><span class="sxs-lookup"><span data-stu-id="32645-163">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c</span></span>
- <span data-ttu-id="32645-164">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span><span class="sxs-lookup"><span data-stu-id="32645-164">Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b</span></span>
- <span data-ttu-id="32645-165">표준 (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span><span class="sxs-lookup"><span data-stu-id="32645-165">Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928</span></span>
- <span data-ttu-id="32645-166">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span><span class="sxs-lookup"><span data-stu-id="32645-166">Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7</span></span>
- <span data-ttu-id="32645-167">\* Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span><span class="sxs-lookup"><span data-stu-id="32645-167">\*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40</span></span>
- <span data-ttu-id="32645-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span><span class="sxs-lookup"><span data-stu-id="32645-168">Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d</span></span>
- <span data-ttu-id="32645-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span><span class="sxs-lookup"><span data-stu-id="32645-169">Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0</span></span>
- <span data-ttu-id="32645-170">프리미엄 (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span><span class="sxs-lookup"><span data-stu-id="32645-170">Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="32645-171">\* 표준 (S3)은 최신 SQL Database 업데이트 V12 (preview)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="32645-171">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="32645-172">자세한 내용은 Azure SQL Database V12 Preview의 새로운 기능을 참조 하세요 https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="32645-172">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32645-173">-동기화</span><span class="sxs-lookup"><span data-stu-id="32645-173">-Sync</span></span>
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

### <span data-ttu-id="32645-174">-확인</span><span class="sxs-lookup"><span data-stu-id="32645-174">-Confirm</span></span>
<span data-ttu-id="32645-175">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32645-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32645-176">-WhatIf</span></span>
<span data-ttu-id="32645-177">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="32645-177">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32645-178">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32645-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32645-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32645-179">CommonParameters</span></span>
<span data-ttu-id="32645-180">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32645-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32645-181">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32645-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32645-182">입력</span><span class="sxs-lookup"><span data-stu-id="32645-182">INPUTS</span></span>

### <span data-ttu-id="32645-183">WindowsAzure. SqlDatabase. \* 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="32645-183">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="32645-184">출력</span><span class="sxs-lookup"><span data-stu-id="32645-184">OUTPUTS</span></span>

### <span data-ttu-id="32645-185">WindowsAzure. SqlDatabase. \* 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="32645-185">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="32645-186">상속자</span><span class="sxs-lookup"><span data-stu-id="32645-186">NOTES</span></span>

## <span data-ttu-id="32645-187">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32645-187">RELATED LINKS</span></span>

[<span data-ttu-id="32645-188">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="32645-188">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="32645-189">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="32645-189">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="32645-190">데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="32645-190">Update Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505718.aspx)

[<span data-ttu-id="32645-191">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="32645-191">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="32645-192">새로운 AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="32645-192">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="32645-193">제거-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="32645-193">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="32645-194">새로운 AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="32645-194">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)



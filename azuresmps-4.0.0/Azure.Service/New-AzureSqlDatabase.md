---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045973"
---
# <span data-ttu-id="43342-101">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="43342-101">New-AzureSqlDatabase</span></span>

## <span data-ttu-id="43342-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43342-102">SYNOPSIS</span></span>
<span data-ttu-id="43342-103">Azure SQL 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43342-103">Creates an Azure SQL Database.</span></span>

## <span data-ttu-id="43342-104">구문과</span><span class="sxs-lookup"><span data-stu-id="43342-104">SYNTAX</span></span>

### <span data-ttu-id="43342-105">ByConnectionContext</span><span class="sxs-lookup"><span data-stu-id="43342-105">ByConnectionContext</span></span>
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43342-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="43342-106">ByServerName</span></span>
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43342-107">설명은</span><span class="sxs-lookup"><span data-stu-id="43342-107">DESCRIPTION</span></span>
<span data-ttu-id="43342-108">**AzureSqlDatabase** Cmdlet은 Azure SQL 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43342-108">The **New-AzureSqlDatabase** cmdlet creates an Azure SQL Database.</span></span>
<span data-ttu-id="43342-109">**새 AzureSqlDatabaseServerContext** cmdlet을 사용 하 여 만든 Azure SQL 데이터베이스 서버 연결 컨텍스트를 사용 하 여 서버를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43342-109">You can specify the server by using an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="43342-110">또는 서버 이름을 지정 하는 경우 cmdlet은 현재 Azure 구독 정보를 사용 하 여 서버에 대 한 액세스 요청을 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="43342-110">Or, if you specify the server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="43342-111">Azure SQL 데이터베이스 서버를 지정 하 여 새 데이터베이스를 만들면 **새 AzureSqlDatabase** cmdlet이 지정 된 서버 이름과 현재 Azure 구독 정보를 사용 하 여 임시 연결 컨텍스트를 만들어 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="43342-111">When you create a new database by specifying an Azure SQL Database server, the **New-AzureSqlDatabase** cmdlet creates a temporary connection context using the specified server name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="43342-112">예제의</span><span class="sxs-lookup"><span data-stu-id="43342-112">EXAMPLES</span></span>

### <span data-ttu-id="43342-113">예제 1: 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="43342-113">Example 1: Create a database</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="43342-114">이 명령은 Azure SQL 데이터베이스 서버 연결 컨텍스트 $Context에 Database1 이라는 Azure SQL 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43342-114">This command creates an Azure SQL Database named Database1, for the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="43342-115">예제 2: 현재 구독에서 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="43342-115">Example 2: Create a database in the current subscription</span></span>
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="43342-116">이 예제에서는 lpqd0zbr8y 이라는 지정 된 Azure SQL 데이터베이스 서버에 Database1 이라는 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43342-116">This example creates a database named Database1, in the specified Azure SQL Database server named lpqd0zbr8y.</span></span>
<span data-ttu-id="43342-117">Cmdlet은 현재 Azure 구독 정보를 사용 하 여 서버에 대 한 요청을 인증 합니다.</span><span class="sxs-lookup"><span data-stu-id="43342-117">The cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

## <span data-ttu-id="43342-118">변수</span><span class="sxs-lookup"><span data-stu-id="43342-118">PARAMETERS</span></span>

### <span data-ttu-id="43342-119">-데이터 정렬</span><span class="sxs-lookup"><span data-stu-id="43342-119">-Collation</span></span>
<span data-ttu-id="43342-120">새 데이터베이스에 대 한 데이터 정렬을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43342-120">Specifies a collation for the new database.</span></span>

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

### <span data-ttu-id="43342-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="43342-121">-ConnectionContext</span></span>
<span data-ttu-id="43342-122">이 cmdlet이 데이터베이스를 만드는 서버의 연결 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43342-122">Specifies the connection context of a server where this cmdlet creates a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43342-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="43342-123">-DatabaseName</span></span>
<span data-ttu-id="43342-124">새 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43342-124">Specifies the name of the new database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43342-125">-에디션</span><span class="sxs-lookup"><span data-stu-id="43342-125">-Edition</span></span>
<span data-ttu-id="43342-126">새 Azure SQL 데이터베이스의 에디션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43342-126">Specifies the edition for the new Azure SQL Database.</span></span>
<span data-ttu-id="43342-127">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="43342-127">Valid values are:</span></span> 

- <span data-ttu-id="43342-128">않아야</span><span class="sxs-lookup"><span data-stu-id="43342-128">None</span></span>
- <span data-ttu-id="43342-129">웹</span><span class="sxs-lookup"><span data-stu-id="43342-129">Web</span></span>
- <span data-ttu-id="43342-130">조직</span><span class="sxs-lookup"><span data-stu-id="43342-130">Business</span></span>
- <span data-ttu-id="43342-131">기본적</span><span class="sxs-lookup"><span data-stu-id="43342-131">Basic</span></span>
- <span data-ttu-id="43342-132">표준이</span><span class="sxs-lookup"><span data-stu-id="43342-132">Standard</span></span>
-  <span data-ttu-id="43342-133">Premium</span><span class="sxs-lookup"><span data-stu-id="43342-133">Premium</span></span>

<span data-ttu-id="43342-134">기본값은 웹용 값입니다.</span><span class="sxs-lookup"><span data-stu-id="43342-134">The default value is Web.</span></span>

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

### <span data-ttu-id="43342-135">-Force</span><span class="sxs-lookup"><span data-stu-id="43342-135">-Force</span></span>
<span data-ttu-id="43342-136">사용자에 게 확인 메시지를 표시 하지 않고 작업을 완료할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="43342-136">Allows the action to complete without prompting the user for confirmation.</span></span>

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

### <span data-ttu-id="43342-137">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="43342-137">-MaxSizeBytes</span></span>
<span data-ttu-id="43342-138">데이터베이스의 최대 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43342-138">Specifies the maximum size of the database in bytes.</span></span>
<span data-ttu-id="43342-139">이 매개 변수 또는 *Maxsizegb* 매개 변수 중 하나를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43342-139">You can specify either this parameter or the *MaxSizeGB* parameter.</span></span>
<span data-ttu-id="43342-140">에디션에 기반 하 여 허용 되는 값에 대 한 *Maxsizegb* 매개 변수 설명을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="43342-140">See the *MaxSizeGB* parameter description for acceptable values based on edition.</span></span>

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

### <span data-ttu-id="43342-141">-MaxSizeGB</span><span class="sxs-lookup"><span data-stu-id="43342-141">-MaxSizeGB</span></span>
<span data-ttu-id="43342-142">데이터베이스의 최대 크기 (기가바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43342-142">Specifies the maximum size of the database in gigabytes.</span></span>
<span data-ttu-id="43342-143">이 매개 변수 또는 *Maxsizebytes* 매개 변수 중 하나를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43342-143">You can specify either this parameter or the *MaxSizeBytes* parameter.</span></span>
<span data-ttu-id="43342-144">허용 되는 값은 버전에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="43342-144">The acceptable values differ based on edition.</span></span>

<span data-ttu-id="43342-145">기본 에디션 값: 1 또는 2</span><span class="sxs-lookup"><span data-stu-id="43342-145">Basic Edition values: 1 or 2</span></span>

<span data-ttu-id="43342-146">스탠더드 버전 값: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 또는 250</span><span class="sxs-lookup"><span data-stu-id="43342-146">Standard Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, or 250</span></span>

<span data-ttu-id="43342-147">Premium Edition 값: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, 500</span><span class="sxs-lookup"><span data-stu-id="43342-147">Premium Edition values: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, or 500</span></span>

<span data-ttu-id="43342-148">웹 버전 값: 1 또는 5</span><span class="sxs-lookup"><span data-stu-id="43342-148">Web Edition values: 1 or 5</span></span>

<span data-ttu-id="43342-149">Business Edition values: 10, 20, 30, 40, 50, 100 또는 150</span><span class="sxs-lookup"><span data-stu-id="43342-149">Business Edition values: 10, 20, 30, 40, 50, 100, or 150</span></span>

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

### <span data-ttu-id="43342-150">-프로필</span><span class="sxs-lookup"><span data-stu-id="43342-150">-Profile</span></span>
<span data-ttu-id="43342-151">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43342-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="43342-152">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="43342-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="43342-153">-ServerName</span><span class="sxs-lookup"><span data-stu-id="43342-153">-ServerName</span></span>
<span data-ttu-id="43342-154">새 데이터베이스를 포함할 Azure SQL 데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43342-154">Specifies the name of the Azure SQL Database server to contain the new database.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43342-155">-ServiceObjective</span><span class="sxs-lookup"><span data-stu-id="43342-155">-ServiceObjective</span></span>
<span data-ttu-id="43342-156">이 데이터베이스에 대 한 새 서비스 목표 (성능 수준)를 나타내는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="43342-156">Specifies an object that represent the new service objective (performance level) for this database.</span></span>
<span data-ttu-id="43342-157">이 값은이 데이터베이스에 할당 된 리소스 수준을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="43342-157">This value represents the level of resources assigned to this database.</span></span>
<span data-ttu-id="43342-158">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="43342-158">Valid values are:</span></span> 

<span data-ttu-id="43342-159">기본: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 \* Standard (S3): 89681b8-7203483a-c4fb-4304-9e9f-17c71c904f5d 10-4eb0-bdf2-e0b050601b40premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d premium (P1): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446 Premium (P3):</span><span class="sxs-lookup"><span data-stu-id="43342-159">Basic: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 \*Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446</span></span>

<span data-ttu-id="43342-160">\* 표준 (S3)은 최신 SQL Database 업데이트 V12 (preview)의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="43342-160">\*Standard (S3) is part of the Latest SQL Database Update V12 (preview).</span></span>
<span data-ttu-id="43342-161">자세한 내용은 Azure SQL Database V12 Preview의 새로운 기능을 참조 하세요 https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .</span><span class="sxs-lookup"><span data-stu-id="43342-161">For more information, see What's New in the Azure SQL Database V12 Previewhttps://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/.</span></span>

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

### <span data-ttu-id="43342-162">-확인</span><span class="sxs-lookup"><span data-stu-id="43342-162">-Confirm</span></span>
<span data-ttu-id="43342-163">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="43342-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43342-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43342-164">-WhatIf</span></span>
<span data-ttu-id="43342-165">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="43342-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43342-166">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43342-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43342-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43342-167">CommonParameters</span></span>
<span data-ttu-id="43342-168">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="43342-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43342-169">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43342-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43342-170">입력</span><span class="sxs-lookup"><span data-stu-id="43342-170">INPUTS</span></span>

## <span data-ttu-id="43342-171">출력</span><span class="sxs-lookup"><span data-stu-id="43342-171">OUTPUTS</span></span>

### <span data-ttu-id="43342-172">WindowsAzure. SqlDatabase. \* 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="43342-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="43342-173">상속자</span><span class="sxs-lookup"><span data-stu-id="43342-173">NOTES</span></span>
* <span data-ttu-id="43342-174">**새 AzureSqlDatabase** 에서 만든 데이터베이스를 삭제 하려면 Remove-AzureSqlDatabase cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="43342-174">To delete a database that was created by **New-AzureSqlDatabase** , use the Remove-AzureSqlDatabase cmdlet.</span></span>

## <span data-ttu-id="43342-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43342-175">RELATED LINKS</span></span>

[<span data-ttu-id="43342-176">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="43342-176">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="43342-177">데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="43342-177">Create Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[<span data-ttu-id="43342-178">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="43342-178">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="43342-179">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="43342-179">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="43342-180">새로운 AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="43342-180">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="43342-181">제거-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="43342-181">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="43342-182">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="43342-182">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)



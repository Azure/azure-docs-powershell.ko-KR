---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B3813F54-E5B7-4605-BB1C-67417FDDB076
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3f9817ebe556bc80364d012040387cca72c56c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046108"
---
# <span data-ttu-id="23cb6-101">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="23cb6-101">Remove-AzureSqlDatabase</span></span>

## <span data-ttu-id="23cb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="23cb6-103">Azure SQL 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-103">Deletes an Azure SQL Database.</span></span>

## <span data-ttu-id="23cb6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23cb6-104">SYNTAX</span></span>

### <span data-ttu-id="23cb6-105">ByNameWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="23cb6-105">ByNameWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23cb6-106">ByObjectWithConnectionContext</span><span class="sxs-lookup"><span data-stu-id="23cb6-106">ByObjectWithConnectionContext</span></span>
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23cb6-107">ByNameWithServerName</span><span class="sxs-lookup"><span data-stu-id="23cb6-107">ByNameWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23cb6-108">ByObjectWithServerName</span><span class="sxs-lookup"><span data-stu-id="23cb6-108">ByObjectWithServerName</span></span>
```
Remove-AzureSqlDatabase -ServerName <String> -Database <Database> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23cb6-109">설명은</span><span class="sxs-lookup"><span data-stu-id="23cb6-109">DESCRIPTION</span></span>
<span data-ttu-id="23cb6-110">**AzureSqlDatabase** cmdlet은 서버 연결 컨텍스트 또는 서버 이름으로 Azure SQL 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-110">The **Remove-AzureSqlDatabase** cmdlet deletes an Azure SQL Database by server connection context or server name.</span></span>
<span data-ttu-id="23cb6-111">**새 AzureSqlDatabaseServerContext** cmdlet을 사용 하 여 Azure SQL 데이터베이스 서버 연결 컨텍스트를 만든 다음이 cmdlet에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-111">You can create an Azure SQL Database server connection context using the **New-AzureSqlDatabaseServerContext** cmdlet, and then use it with this cmdlet.</span></span>

<span data-ttu-id="23cb6-112">Azure SQL 데이터베이스 서버 이름을 지정 하 여 데이터베이스를 삭제 하는 경우 **AzureSqlDatabase** cmdlet은 이름과 현재 Azure 구독 정보를 사용 하 여 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-112">When you delete a database by specifying an Azure SQL Database server name, the **Remove-AzureSqlDatabase** cmdlet uses the name and the current Azure subscription information to perform the operation.</span></span>

## <span data-ttu-id="23cb6-113">예제의</span><span class="sxs-lookup"><span data-stu-id="23cb6-113">EXAMPLES</span></span>

### <span data-ttu-id="23cb6-114">예제 1: 데이터베이스 제거</span><span class="sxs-lookup"><span data-stu-id="23cb6-114">Example 1: Remove a database</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="23cb6-115">이 명령은 Azure SQL 데이터베이스 서버 연결 컨텍스트 $Context에서 Database01 이라는 데이터베이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-115">This command removes the database named Database01 from the Azure SQL Database server connection context $Context.</span></span>

### <span data-ttu-id="23cb6-116">예제 2: 서버 이름을 사용 하 여 데이터베이스 제거</span><span class="sxs-lookup"><span data-stu-id="23cb6-116">Example 2: Remove a database by using a server name</span></span>
```
PS C:\> Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="23cb6-117">이 명령은 lpqd0zbr8y 이라는 Azure SQL 데이터베이스 서버에서 Database01 이라는 데이터베이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-117">This command removes the database named Database01 from the Azure SQL Database server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="23cb6-118">예제 3: 파이프라인을 사용 하 여 데이터베이스 제거</span><span class="sxs-lookup"><span data-stu-id="23cb6-118">Example 3: Remove a database by using the pipeline</span></span>
```
PS C:\> $Database01 | Remove-AzureSqlDatabase -ConnectionContext $Context
PS C:\> $Database01 | Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="23cb6-119">이 예제에서는 파이프라인을 통해 데이터베이스 개체를 전달 하는 다른 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-119">This example demonstrates the alternative method of passing the database object through the pipeline.</span></span>

## <span data-ttu-id="23cb6-120">변수</span><span class="sxs-lookup"><span data-stu-id="23cb6-120">PARAMETERS</span></span>

### <span data-ttu-id="23cb6-121">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="23cb6-121">-ConnectionContext</span></span>
<span data-ttu-id="23cb6-122">이 cmdlet이 데이터베이스를 제거할 서버의 연결 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-122">Specifies the connection context of a server from which this cmdlet removes a database.</span></span>

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

### <span data-ttu-id="23cb6-123">-데이터베이스</span><span class="sxs-lookup"><span data-stu-id="23cb6-123">-Database</span></span>
<span data-ttu-id="23cb6-124">이 cmdlet이 제거 하는 데이터베이스를 나타내는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-124">Specifies an object that represents the database that this cmdlet removes.</span></span>

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23cb6-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="23cb6-125">-DatabaseName</span></span>
<span data-ttu-id="23cb6-126">이 cmdlet이 제거 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-126">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="23cb6-127">-Force</span><span class="sxs-lookup"><span data-stu-id="23cb6-127">-Force</span></span>
<span data-ttu-id="23cb6-128">사용자에 게 확인 메시지를 표시 하지 않고 작업을 완료할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-128">Allows the action to complete without prompting the user for confirmation.</span></span>

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

### <span data-ttu-id="23cb6-129">-프로필</span><span class="sxs-lookup"><span data-stu-id="23cb6-129">-Profile</span></span>
<span data-ttu-id="23cb6-130">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="23cb6-131">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23cb6-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="23cb6-132">-ServerName</span></span>
<span data-ttu-id="23cb6-133">이 cmdlet이 데이터베이스를 삭제 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-133">Specifies the name of the server on which this cmdlet deletes the database.</span></span>

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

### <span data-ttu-id="23cb6-134">-확인</span><span class="sxs-lookup"><span data-stu-id="23cb6-134">-Confirm</span></span>
<span data-ttu-id="23cb6-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23cb6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23cb6-136">-WhatIf</span></span>
<span data-ttu-id="23cb6-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23cb6-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23cb6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23cb6-139">CommonParameters</span></span>
<span data-ttu-id="23cb6-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23cb6-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23cb6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23cb6-142">입력</span><span class="sxs-lookup"><span data-stu-id="23cb6-142">INPUTS</span></span>

### <span data-ttu-id="23cb6-143">WindowsAzure. SqlDatabase. \* 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="23cb6-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="23cb6-144">출력</span><span class="sxs-lookup"><span data-stu-id="23cb6-144">OUTPUTS</span></span>

## <span data-ttu-id="23cb6-145">상속자</span><span class="sxs-lookup"><span data-stu-id="23cb6-145">NOTES</span></span>
* <span data-ttu-id="23cb6-146">작업의 심각성 때문에이 cmdlet은 기본적으로 확인을 요청 하는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-146">Because of the severity of the operation, by default, this cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="23cb6-147">확인을 건너뛰려면 *Force* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23cb6-147">To skip confirmation, specify the *Force* parameter.</span></span>

## <span data-ttu-id="23cb6-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23cb6-148">RELATED LINKS</span></span>

[<span data-ttu-id="23cb6-149">Azure SQL 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="23cb6-149">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="23cb6-150">데이터베이스 삭제</span><span class="sxs-lookup"><span data-stu-id="23cb6-150">Delete Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505705.aspx)

[<span data-ttu-id="23cb6-151">Azure SQL 데이터베이스에 대 한 작업</span><span class="sxs-lookup"><span data-stu-id="23cb6-151">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="23cb6-152">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="23cb6-152">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="23cb6-153">새로운 AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="23cb6-153">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="23cb6-154">새로운 AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="23cb6-154">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="23cb6-155">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="23cb6-155">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)



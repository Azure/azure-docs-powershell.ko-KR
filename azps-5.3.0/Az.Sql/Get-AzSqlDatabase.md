---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
ms.openlocfilehash: 4f90d6d0c33874750bf2f32ae7f65bf32457f63c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375187"
---
# <span data-ttu-id="86489-101">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="86489-101">Get-AzSqlDatabase</span></span>

## <span data-ttu-id="86489-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86489-102">SYNOPSIS</span></span>
<span data-ttu-id="86489-103">하나 이상의 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="86489-103">Gets one or more databases.</span></span>

## <span data-ttu-id="86489-104">구문</span><span class="sxs-lookup"><span data-stu-id="86489-104">SYNTAX</span></span>

```
Get-AzSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86489-105">설명</span><span class="sxs-lookup"><span data-stu-id="86489-105">DESCRIPTION</span></span>
<span data-ttu-id="86489-106">**Get-AzSqlDatabase** cmdlet은 Azure SQL Database Server에서 하나 이상의 Azure SQL 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="86489-106">The **Get-AzSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>
<span data-ttu-id="86489-107">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서도 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="86489-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="86489-108">예제</span><span class="sxs-lookup"><span data-stu-id="86489-108">EXAMPLES</span></span>

### <span data-ttu-id="86489-109">예제 1: 서버에서 모든 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="86489-109">Example 1: Get all databases on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : master
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="86489-110">이 명령은 server01이라는 서버의 모든 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="86489-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="86489-111">예제 2: 서버에서 이름으로 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="86489-111">Example 2: Get a database by name on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="86489-112">이 명령은 Server01이라는 서버에서 Database02라는 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="86489-112">This command gets a database named Database02 from a server named Server01.</span></span>

### <span data-ttu-id="86489-113">예제 3: 필터링을 사용하여 서버의 모든 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="86489-113">Example 3: Get all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database*"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="86489-114">이 명령은 "database"로 시작하는 server01이라는 서버의 모든 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="86489-114">This command gets all databases on the server named server01 that start with "database".</span></span>

## <span data-ttu-id="86489-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86489-115">PARAMETERS</span></span>

### <span data-ttu-id="86489-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="86489-116">-DatabaseName</span></span>
<span data-ttu-id="86489-117">검색할 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="86489-117">Specifies the name of the database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86489-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86489-118">-DefaultProfile</span></span>
<span data-ttu-id="86489-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="86489-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86489-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86489-120">-ResourceGroupName</span></span>
<span data-ttu-id="86489-121">데이터베이스 서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="86489-121">Specifies the name of the resource group to which the database server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86489-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="86489-122">-ServerName</span></span>
<span data-ttu-id="86489-123">데이터베이스가 할당된 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="86489-123">Specifies the name of the server to which the database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86489-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86489-124">-Confirm</span></span>
<span data-ttu-id="86489-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="86489-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86489-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86489-126">-WhatIf</span></span>
<span data-ttu-id="86489-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="86489-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86489-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86489-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86489-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86489-129">CommonParameters</span></span>
<span data-ttu-id="86489-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="86489-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86489-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="86489-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86489-132">입력</span><span class="sxs-lookup"><span data-stu-id="86489-132">INPUTS</span></span>

### <span data-ttu-id="86489-133">System.String</span><span class="sxs-lookup"><span data-stu-id="86489-133">System.String</span></span>

## <span data-ttu-id="86489-134">출력</span><span class="sxs-lookup"><span data-stu-id="86489-134">OUTPUTS</span></span>

### <span data-ttu-id="86489-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="86489-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="86489-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="86489-136">NOTES</span></span>

## <span data-ttu-id="86489-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86489-137">RELATED LINKS</span></span>

[<span data-ttu-id="86489-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="86489-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="86489-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="86489-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="86489-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="86489-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="86489-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="86489-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="86489-142">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="86489-142">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)



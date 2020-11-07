---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
ms.openlocfilehash: bcaa1c5d57fea979e227fa8890cac6ac0b3f8a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873545"
---
# <span data-ttu-id="1dd8d-101">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1dd8d-101">Get-AzSqlDatabase</span></span>

## <span data-ttu-id="1dd8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dd8d-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd8d-103">하나 이상의 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-103">Gets one or more databases.</span></span>

## <span data-ttu-id="1dd8d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1dd8d-104">SYNTAX</span></span>

```
Get-AzSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dd8d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1dd8d-105">DESCRIPTION</span></span>
<span data-ttu-id="1dd8d-106">**AzSqlDatabase** Cmdlet은 Azure Sql 데이터베이스 서버에서 하나 이상의 azure sql 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-106">The **Get-AzSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>
<span data-ttu-id="1dd8d-107">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1dd8d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="1dd8d-108">EXAMPLES</span></span>

### <span data-ttu-id="1dd8d-109">예제 1: 서버의 모든 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="1dd8d-109">Example 1: Get all databases on a server</span></span>
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

<span data-ttu-id="1dd8d-110">이 명령은 server01 이라는 서버의 모든 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="1dd8d-111">예제 2: 서버에서 이름으로 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="1dd8d-111">Example 2: Get a database by name on a server</span></span>
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

<span data-ttu-id="1dd8d-112">이 명령은 Server01 라는 서버에서 Database02 이라는 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-112">This command gets a database named Database02 from a server named Server01.</span></span>

### <span data-ttu-id="1dd8d-113">예제 3: 필터링을 사용 하 여 서버의 모든 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="1dd8d-113">Example 3: Get all databases on a server using filtering</span></span>
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

<span data-ttu-id="1dd8d-114">이 명령은 server01 이라는 서버에서 "database"로 시작 하는 모든 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-114">This command gets all databases on the server named server01 that start with "database".</span></span>

## <span data-ttu-id="1dd8d-115">변수</span><span class="sxs-lookup"><span data-stu-id="1dd8d-115">PARAMETERS</span></span>

### <span data-ttu-id="1dd8d-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1dd8d-116">-DatabaseName</span></span>
<span data-ttu-id="1dd8d-117">검색할 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-117">Specifies the name of the database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1dd8d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd8d-118">-DefaultProfile</span></span>
<span data-ttu-id="1dd8d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1dd8d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dd8d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dd8d-120">-ResourceGroupName</span></span>
<span data-ttu-id="1dd8d-121">데이터베이스 서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-121">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="1dd8d-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1dd8d-122">-ServerName</span></span>
<span data-ttu-id="1dd8d-123">데이터베이스가 할당 된 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-123">Specifies the name of the server to which the database is assigned.</span></span>

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

### <span data-ttu-id="1dd8d-124">-확인</span><span class="sxs-lookup"><span data-stu-id="1dd8d-124">-Confirm</span></span>
<span data-ttu-id="1dd8d-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dd8d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dd8d-126">-WhatIf</span></span>
<span data-ttu-id="1dd8d-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dd8d-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dd8d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd8d-129">CommonParameters</span></span>
<span data-ttu-id="1dd8d-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd8d-131">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd8d-132">입력</span><span class="sxs-lookup"><span data-stu-id="1dd8d-132">INPUTS</span></span>

### <span data-ttu-id="1dd8d-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1dd8d-133">System.String</span></span>

## <span data-ttu-id="1dd8d-134">출력</span><span class="sxs-lookup"><span data-stu-id="1dd8d-134">OUTPUTS</span></span>

### <span data-ttu-id="1dd8d-135">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="1dd8d-136">상속자</span><span class="sxs-lookup"><span data-stu-id="1dd8d-136">NOTES</span></span>

## <span data-ttu-id="1dd8d-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1dd8d-137">RELATED LINKS</span></span>

[<span data-ttu-id="1dd8d-138">새로운 AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1dd8d-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="1dd8d-139">제거-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1dd8d-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="1dd8d-140">이력서-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1dd8d-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="1dd8d-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1dd8d-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="1dd8d-142">일시 중단-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1dd8d-142">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)



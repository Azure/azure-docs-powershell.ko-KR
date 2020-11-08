---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
ms.openlocfilehash: 79577b9812f743035d90b2c4fe112dd9f2468fd2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226157"
---
# <span data-ttu-id="10f98-101">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="10f98-101">Get-AzSqlServer</span></span>

## <span data-ttu-id="10f98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10f98-102">SYNOPSIS</span></span>
<span data-ttu-id="10f98-103">SQL 데이터베이스 서버에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="10f98-103">Returns information about SQL Database servers.</span></span>

## <span data-ttu-id="10f98-104">구문과</span><span class="sxs-lookup"><span data-stu-id="10f98-104">SYNTAX</span></span>

```
Get-AzSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10f98-105">설명은</span><span class="sxs-lookup"><span data-stu-id="10f98-105">DESCRIPTION</span></span>
<span data-ttu-id="10f98-106">**AzSqlServer** cmdlet은 하나 이상의 Azure SQL 데이터베이스 서버에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="10f98-106">The **Get-AzSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="10f98-107">해당 서버에 대 한 정보를 볼 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10f98-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="10f98-108">예제의</span><span class="sxs-lookup"><span data-stu-id="10f98-108">EXAMPLES</span></span>

### <span data-ttu-id="10f98-109">예제 1: 리소스 그룹에 할당 된 SQL Server의 모든 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="10f98-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="10f98-110">이 명령은 리소스 그룹 ResourceGroup01에 할당 된 모든 Azure SQL 데이터베이스 서버에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10f98-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="10f98-111">예제 2: Azure SQL 데이터베이스 서버에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="10f98-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="10f98-112">이 명령은 Server01 이라는 Azure SQL 데이터베이스 서버에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10f98-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="10f98-113">예제 3: 구독에서 SQL Server의 모든 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="10f98-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server03.database.windows.net
```

<span data-ttu-id="10f98-114">이 명령은 현재 구독의 모든 Azure SQL 데이터베이스 서버에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10f98-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

### <span data-ttu-id="10f98-115">예제 4: 필터링을 사용 하 여 리소스 그룹에 할당 된 SQL Server의 모든 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="10f98-115">Example 4: Get all instances of SQL Server assigned to a resource group using filtering</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "server*"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="10f98-116">이 명령은 "server"로 시작 하는 리소스 그룹 ResourceGroup01에 할당 된 모든 Azure SQL 데이터베이스 서버에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10f98-116">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01 that start with "server".</span></span>

## <span data-ttu-id="10f98-117">변수</span><span class="sxs-lookup"><span data-stu-id="10f98-117">PARAMETERS</span></span>

### <span data-ttu-id="10f98-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10f98-118">-DefaultProfile</span></span>
<span data-ttu-id="10f98-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="10f98-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10f98-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10f98-120">-ResourceGroupName</span></span>
<span data-ttu-id="10f98-121">서버가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10f98-121">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f98-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="10f98-122">-ServerName</span></span>
<span data-ttu-id="10f98-123">이 cmdlet이 가져오는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10f98-123">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f98-124">-확인</span><span class="sxs-lookup"><span data-stu-id="10f98-124">-Confirm</span></span>
<span data-ttu-id="10f98-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="10f98-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10f98-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10f98-126">-WhatIf</span></span>
<span data-ttu-id="10f98-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="10f98-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10f98-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10f98-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10f98-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10f98-129">CommonParameters</span></span>
<span data-ttu-id="10f98-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="10f98-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10f98-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="10f98-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10f98-132">입력</span><span class="sxs-lookup"><span data-stu-id="10f98-132">INPUTS</span></span>

### <span data-ttu-id="10f98-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="10f98-133">System.String</span></span>

## <span data-ttu-id="10f98-134">출력</span><span class="sxs-lookup"><span data-stu-id="10f98-134">OUTPUTS</span></span>

### <span data-ttu-id="10f98-135">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="10f98-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="10f98-136">상속자</span><span class="sxs-lookup"><span data-stu-id="10f98-136">NOTES</span></span>

## <span data-ttu-id="10f98-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10f98-137">RELATED LINKS</span></span>

[<span data-ttu-id="10f98-138">새로운 AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="10f98-138">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="10f98-139">제거-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="10f98-139">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="10f98-140">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="10f98-140">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="10f98-141">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="10f98-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



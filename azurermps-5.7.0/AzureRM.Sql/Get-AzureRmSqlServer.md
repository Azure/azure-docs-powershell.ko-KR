---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
ms.openlocfilehash: a3af56ab78cd31dde30939901eaff12fff78ffa2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533603"
---
# <span data-ttu-id="0d815-101">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="0d815-101">Get-AzureRmSqlServer</span></span>

## <span data-ttu-id="0d815-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d815-102">SYNOPSIS</span></span>
<span data-ttu-id="0d815-103">SQL 데이터베이스 서버에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d815-103">Returns information about SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d815-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d815-104">SYNTAX</span></span>

```
Get-AzureRmSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d815-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0d815-105">DESCRIPTION</span></span>
<span data-ttu-id="0d815-106">**AzureRmSqlServer** cmdlet은 하나 이상의 Azure SQL 데이터베이스 서버에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d815-106">The **Get-AzureRmSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="0d815-107">해당 서버에 대 한 정보를 볼 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d815-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="0d815-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0d815-108">EXAMPLES</span></span>

### <span data-ttu-id="0d815-109">예제 1: 리소스 그룹에 할당 된 SQL Server의 모든 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="0d815-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="0d815-110">이 명령은 리소스 그룹 ResourceGroup01에 할당 된 모든 Azure SQL 데이터베이스 서버에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d815-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="0d815-111">예제 2: Azure SQL 데이터베이스 서버에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="0d815-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="0d815-112">이 명령은 Server01 이라는 Azure SQL 데이터베이스 서버에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d815-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="0d815-113">예제 3: 구독에서 SQL Server의 모든 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="0d815-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmSqlServer
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

<span data-ttu-id="0d815-114">이 명령은 현재 구독의 모든 Azure SQL 데이터베이스 서버에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0d815-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

## <span data-ttu-id="0d815-115">변수</span><span class="sxs-lookup"><span data-stu-id="0d815-115">PARAMETERS</span></span>

### <span data-ttu-id="0d815-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d815-116">-DefaultProfile</span></span>
<span data-ttu-id="0d815-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0d815-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d815-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d815-118">-ResourceGroupName</span></span>
<span data-ttu-id="0d815-119">서버가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d815-119">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d815-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0d815-120">-ServerName</span></span>
<span data-ttu-id="0d815-121">이 cmdlet이 가져오는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d815-121">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d815-122">-확인</span><span class="sxs-lookup"><span data-stu-id="0d815-122">-Confirm</span></span>
<span data-ttu-id="0d815-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d815-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d815-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d815-124">-WhatIf</span></span>
<span data-ttu-id="0d815-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0d815-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d815-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d815-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d815-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d815-127">CommonParameters</span></span>
<span data-ttu-id="0d815-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d815-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d815-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d815-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d815-130">입력</span><span class="sxs-lookup"><span data-stu-id="0d815-130">INPUTS</span></span>

### <span data-ttu-id="0d815-131">않아야</span><span class="sxs-lookup"><span data-stu-id="0d815-131">None</span></span>
<span data-ttu-id="0d815-132">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d815-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0d815-133">출력</span><span class="sxs-lookup"><span data-stu-id="0d815-133">OUTPUTS</span></span>

### <span data-ttu-id="0d815-134">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="0d815-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="0d815-135">상속자</span><span class="sxs-lookup"><span data-stu-id="0d815-135">NOTES</span></span>

## <span data-ttu-id="0d815-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d815-136">RELATED LINKS</span></span>

[<span data-ttu-id="0d815-137">새로운 AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="0d815-137">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="0d815-138">제거-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="0d815-138">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="0d815-139">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="0d815-139">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="0d815-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="0d815-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



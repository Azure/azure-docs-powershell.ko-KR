---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServer.md
ms.openlocfilehash: f2d687ce10edf56fc424c03873c733971f70e546
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533823"
---
# <span data-ttu-id="91430-101">Get-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="91430-101">Get-AzureRmSqlServer</span></span>

## <span data-ttu-id="91430-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91430-102">SYNOPSIS</span></span>
<span data-ttu-id="91430-103">SQL 데이터베이스 서버에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="91430-103">Returns information about SQL Database servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91430-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91430-104">SYNTAX</span></span>

```
Get-AzureRmSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91430-105">설명은</span><span class="sxs-lookup"><span data-stu-id="91430-105">DESCRIPTION</span></span>
<span data-ttu-id="91430-106">**AzureRmSqlServer** cmdlet은 하나 이상의 Azure SQL 데이터베이스 서버에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="91430-106">The **Get-AzureRmSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="91430-107">해당 서버에 대 한 정보를 볼 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91430-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="91430-108">예제의</span><span class="sxs-lookup"><span data-stu-id="91430-108">EXAMPLES</span></span>

### <span data-ttu-id="91430-109">예제 1: 리소스 그룹에 할당 된 SQL Server의 모든 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="91430-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLoginSqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="91430-110">이 명령은 리소스 그룹 ResourceGroup01에 할당 된 모든 Azure SQL 데이터베이스 서버에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91430-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="91430-111">예제 2: Azure SQL 데이터베이스 서버에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="91430-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="91430-112">이 명령은 Server01 이라는 Azure SQL 데이터베이스 서버에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91430-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="91430-113">예제 3: 구독에서 SQL Server의 모든 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="91430-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     : 

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword : 
ServerVersion            : 12.0
Tags                     :
```

<span data-ttu-id="91430-114">이 명령은 현재 구독의 모든 Azure SQL 데이터베이스 서버에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91430-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

## <span data-ttu-id="91430-115">변수</span><span class="sxs-lookup"><span data-stu-id="91430-115">PARAMETERS</span></span>

### <span data-ttu-id="91430-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91430-116">-ResourceGroupName</span></span>
<span data-ttu-id="91430-117">서버가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91430-117">Specifies the name of the resource group to which servers are assigned.</span></span>

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

### <span data-ttu-id="91430-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="91430-118">-ServerName</span></span>
<span data-ttu-id="91430-119">이 cmdlet이 가져오는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91430-119">Specifies the name of the server that this cmdlet gets.</span></span>

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

### <span data-ttu-id="91430-120">-확인</span><span class="sxs-lookup"><span data-stu-id="91430-120">-Confirm</span></span>
<span data-ttu-id="91430-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="91430-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91430-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91430-122">-WhatIf</span></span>
<span data-ttu-id="91430-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="91430-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91430-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91430-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91430-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91430-125">-DefaultProfile</span></span>
<span data-ttu-id="91430-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91430-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91430-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91430-127">CommonParameters</span></span>
<span data-ttu-id="91430-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91430-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91430-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91430-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91430-130">입력</span><span class="sxs-lookup"><span data-stu-id="91430-130">INPUTS</span></span>

## <span data-ttu-id="91430-131">출력</span><span class="sxs-lookup"><span data-stu-id="91430-131">OUTPUTS</span></span>

### <span data-ttu-id="91430-132">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="91430-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="91430-133">상속자</span><span class="sxs-lookup"><span data-stu-id="91430-133">NOTES</span></span>

## <span data-ttu-id="91430-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91430-134">RELATED LINKS</span></span>

[<span data-ttu-id="91430-135">새로운 AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="91430-135">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="91430-136">제거-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="91430-136">Remove-AzureRmSqlServer</span></span>](./Remove-AzureRmSqlServer.md)

[<span data-ttu-id="91430-137">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="91430-137">Set-AzureRmSqlServer</span></span>](./Set-AzureRmSqlServer.md)

[<span data-ttu-id="91430-138">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="91430-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



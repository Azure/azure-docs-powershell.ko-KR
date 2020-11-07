---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaserestorepoints
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
ms.openlocfilehash: c1e4c22392087793e6fbfa0e3959a8b92767ad04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703433"
---
# <span data-ttu-id="70b76-101">Get-AzureRmSqlDatabaseRestorePoints</span><span class="sxs-lookup"><span data-stu-id="70b76-101">Get-AzureRmSqlDatabaseRestorePoints</span></span>

## <span data-ttu-id="70b76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70b76-102">SYNOPSIS</span></span>
<span data-ttu-id="70b76-103">SQL 데이터 웨어하우스를 복원할 수 있는 고유한 복원 지점을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b76-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70b76-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70b76-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseRestorePoints [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70b76-105">설명은</span><span class="sxs-lookup"><span data-stu-id="70b76-105">DESCRIPTION</span></span>
<span data-ttu-id="70b76-106">**AzureRmSqlDatabaseRestorePoints** Cmdlet은 Azure SQL 데이터 웨어하우스가 복원 될 수 있는 개별 복원 지점을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b76-106">The **Get-AzureRmSqlDatabaseRestorePoints** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="70b76-107">Azure SQL 데이터베이스의 경우 복원 창은 계속 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70b76-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="70b76-108">즉, 데이터베이스의 백업 보존 기간에 있는 모든 시점을 복원 시점으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="70b76-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>
<span data-ttu-id="70b76-109">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="70b76-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="70b76-110">예제의</span><span class="sxs-lookup"><span data-stu-id="70b76-110">EXAMPLES</span></span>

### <span data-ttu-id="70b76-111">예제 1: 모든 복원 지점 가져오기</span><span class="sxs-lookup"><span data-stu-id="70b76-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseRestorePoints -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="70b76-112">이 명령은 Database01 이라는 Azure SQL 데이터베이스에 대해 사용 가능한 모든 복원 지점을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b76-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="70b76-113">변수</span><span class="sxs-lookup"><span data-stu-id="70b76-113">PARAMETERS</span></span>

### <span data-ttu-id="70b76-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="70b76-114">-DatabaseName</span></span>
<span data-ttu-id="70b76-115">SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b76-115">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70b76-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70b76-116">-DefaultProfile</span></span>
<span data-ttu-id="70b76-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="70b76-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70b76-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70b76-118">-ResourceGroupName</span></span>
<span data-ttu-id="70b76-119">SQL 데이터베이스를 할당할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b76-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="70b76-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="70b76-120">-ServerName</span></span>
<span data-ttu-id="70b76-121">데이터베이스를 호스트 하는 AzureSQL 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b76-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="70b76-122">-확인</span><span class="sxs-lookup"><span data-stu-id="70b76-122">-Confirm</span></span>
<span data-ttu-id="70b76-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b76-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70b76-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70b76-124">-WhatIf</span></span>
<span data-ttu-id="70b76-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="70b76-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70b76-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="70b76-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70b76-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70b76-127">CommonParameters</span></span>
<span data-ttu-id="70b76-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70b76-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70b76-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70b76-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70b76-130">입력</span><span class="sxs-lookup"><span data-stu-id="70b76-130">INPUTS</span></span>

### <span data-ttu-id="70b76-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="70b76-131">System.String</span></span>

## <span data-ttu-id="70b76-132">출력</span><span class="sxs-lookup"><span data-stu-id="70b76-132">OUTPUTS</span></span>

### <span data-ttu-id="70b76-133">AzureSqlDatabaseRestorePointModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="70b76-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="70b76-134">상속자</span><span class="sxs-lookup"><span data-stu-id="70b76-134">NOTES</span></span>

## <span data-ttu-id="70b76-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70b76-135">RELATED LINKS</span></span>

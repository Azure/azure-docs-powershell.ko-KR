---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 9765afd55ea94bda672d5e1ce43ac3d8d535510d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341258"
---
# <span data-ttu-id="572e2-101">Get-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="572e2-101">Get-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="572e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="572e2-102">SYNOPSIS</span></span>
<span data-ttu-id="572e2-103">데이터 웨어하우스를 복원할 수 있는 SQL 복원 지점을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="572e2-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

## <span data-ttu-id="572e2-104">구문</span><span class="sxs-lookup"><span data-stu-id="572e2-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRestorePoint [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="572e2-105">설명</span><span class="sxs-lookup"><span data-stu-id="572e2-105">DESCRIPTION</span></span>
<span data-ttu-id="572e2-106">**Get-AzSqlDatabaseRestorePoint** cmdlet은 Azure SQL Data Warehouse를 복원할 수 있는 고유한 복원 지점을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="572e2-106">The **Get-AzSqlDatabaseRestorePoint** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="572e2-107">Azure SQL 데이터베이스의 경우 복원 창이 연속됩니다.</span><span class="sxs-lookup"><span data-stu-id="572e2-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="572e2-108">즉, 데이터베이스의 백업 보존 기간에 있는 모든 시점을 복원 지점으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="572e2-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>
<span data-ttu-id="572e2-109">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서도 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="572e2-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="572e2-110">예제</span><span class="sxs-lookup"><span data-stu-id="572e2-110">EXAMPLES</span></span>

### <span data-ttu-id="572e2-111">예제 1: 모든 복원 지점을 얻게</span><span class="sxs-lookup"><span data-stu-id="572e2-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="572e2-112">이 명령은 Database01이라는 Azure SQL 사용 가능한 모든 복원 지점을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="572e2-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="572e2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="572e2-113">PARAMETERS</span></span>

### <span data-ttu-id="572e2-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="572e2-114">-DatabaseName</span></span>
<span data-ttu-id="572e2-115">SQL 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="572e2-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="572e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="572e2-116">-DefaultProfile</span></span>
<span data-ttu-id="572e2-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="572e2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="572e2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="572e2-118">-ResourceGroupName</span></span>
<span data-ttu-id="572e2-119">SQL 데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="572e2-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="572e2-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="572e2-120">-ServerName</span></span>
<span data-ttu-id="572e2-121">데이터베이스를 호스트하는 AzureSQL 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="572e2-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="572e2-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="572e2-122">-Confirm</span></span>
<span data-ttu-id="572e2-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="572e2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="572e2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="572e2-124">-WhatIf</span></span>
<span data-ttu-id="572e2-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="572e2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="572e2-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="572e2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="572e2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="572e2-127">CommonParameters</span></span>
<span data-ttu-id="572e2-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="572e2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="572e2-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="572e2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="572e2-130">입력</span><span class="sxs-lookup"><span data-stu-id="572e2-130">INPUTS</span></span>

### <span data-ttu-id="572e2-131">System.String</span><span class="sxs-lookup"><span data-stu-id="572e2-131">System.String</span></span>

## <span data-ttu-id="572e2-132">출력</span><span class="sxs-lookup"><span data-stu-id="572e2-132">OUTPUTS</span></span>

### <span data-ttu-id="572e2-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="572e2-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="572e2-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="572e2-134">NOTES</span></span>

## <span data-ttu-id="572e2-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="572e2-135">RELATED LINKS</span></span>

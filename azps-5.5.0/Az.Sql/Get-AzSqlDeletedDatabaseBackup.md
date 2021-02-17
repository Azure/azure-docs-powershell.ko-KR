---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
ms.openlocfilehash: d534ddc9c076d0e7c2ea611d6fdb15ae22e84846
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207904"
---
# <span data-ttu-id="a9eb6-101">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="a9eb6-101">Get-AzSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="a9eb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="a9eb6-103">복원할 수 있는 삭제된 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="a9eb6-104">구문</span><span class="sxs-lookup"><span data-stu-id="a9eb6-104">SYNTAX</span></span>

```
Get-AzSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>] [[-DeletionDate] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9eb6-105">설명</span><span class="sxs-lookup"><span data-stu-id="a9eb6-105">DESCRIPTION</span></span>
<span data-ttu-id="a9eb6-106">**Get-AzSqlDeletedDatabaseBackup** cmdlet은 복원할 수 있는 지정된 삭제된 SQL 데이터베이스 백업 또는 복원할 수 있는 모든 삭제된 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-106">The **Get-AzSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="a9eb6-107">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서도 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a9eb6-108">예제</span><span class="sxs-lookup"><span data-stu-id="a9eb6-108">EXAMPLES</span></span>

### <span data-ttu-id="a9eb6-109">예제 1: 서버에서 모든 삭제된 데이터베이스 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="a9eb6-110">이 명령은 서버에서 삭제된 모든 데이터베이스 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="a9eb6-111">예제 2: 지정된 삭제된 데이터베이스 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="a9eb6-112">이 명령은 ContosoDatabase에 대한 삭제된 데이터베이스 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="a9eb6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9eb6-113">PARAMETERS</span></span>

### <span data-ttu-id="a9eb6-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a9eb6-114">-DatabaseName</span></span>
<span data-ttu-id="a9eb6-115">데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-115">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9eb6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9eb6-116">-DefaultProfile</span></span>
<span data-ttu-id="a9eb6-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a9eb6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9eb6-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="a9eb6-118">-DeletionDate</span></span>
<span data-ttu-id="a9eb6-119">데이터베이스가 삭제된 날짜를 **DateTime** 개체로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="a9eb6-120">**DateTime 개체를** 얻습니다. Get-Date cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9eb6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9eb6-121">-ResourceGroupName</span></span>
<span data-ttu-id="a9eb6-122">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a9eb6-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a9eb6-123">-ServerName</span></span>
<span data-ttu-id="a9eb6-124">데이터베이스 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="a9eb6-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9eb6-125">-Confirm</span></span>
<span data-ttu-id="a9eb6-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9eb6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9eb6-127">-WhatIf</span></span>
<span data-ttu-id="a9eb6-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a9eb6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9eb6-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9eb6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9eb6-130">CommonParameters</span></span>
<span data-ttu-id="a9eb6-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9eb6-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a9eb6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9eb6-133">입력</span><span class="sxs-lookup"><span data-stu-id="a9eb6-133">INPUTS</span></span>

### <span data-ttu-id="a9eb6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a9eb6-134">System.String</span></span>

### <span data-ttu-id="a9eb6-135">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a9eb6-135">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a9eb6-136">출력</span><span class="sxs-lookup"><span data-stu-id="a9eb6-136">OUTPUTS</span></span>

### <span data-ttu-id="a9eb6-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="a9eb6-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="a9eb6-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a9eb6-138">NOTES</span></span>

## <span data-ttu-id="a9eb6-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9eb6-139">RELATED LINKS</span></span>

[<span data-ttu-id="a9eb6-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a9eb6-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="a9eb6-141">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="a9eb6-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

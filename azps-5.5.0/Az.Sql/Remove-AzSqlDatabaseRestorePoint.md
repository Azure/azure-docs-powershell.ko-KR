---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 2e98f832bd13509a853d85037a413b6fd5895695
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196036"
---
# <span data-ttu-id="7e03b-101">Remove-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="7e03b-101">Remove-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="7e03b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e03b-102">SYNOPSIS</span></span>
<span data-ttu-id="7e03b-103">데이터베이스의 복원 지점에서 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7e03b-103">Removes given restore point from a SQL Database.</span></span>

## <span data-ttu-id="7e03b-104">구문</span><span class="sxs-lookup"><span data-stu-id="7e03b-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e03b-105">설명</span><span class="sxs-lookup"><span data-stu-id="7e03b-105">DESCRIPTION</span></span>
<span data-ttu-id="7e03b-106">**Remove-AzSqlDatabaseRestorePoint** cmdlet은 Azure SQL 데이터베이스에서 복원 지점을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7e03b-106">The **Remove-AzSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="7e03b-107">이 cmdlet은 현재 Azure SQL Database의 SQL Server Datawarehouse 서비스에서 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e03b-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="7e03b-108">예제</span><span class="sxs-lookup"><span data-stu-id="7e03b-108">EXAMPLES</span></span>

### <span data-ttu-id="7e03b-109">예제 1: 복원 지점 제거</span><span class="sxs-lookup"><span data-stu-id="7e03b-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="7e03b-110">이 명령은 Azure SQL 데이터베이스의 복원 지점을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7e03b-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="7e03b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e03b-111">PARAMETERS</span></span>

### <span data-ttu-id="7e03b-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7e03b-112">-DatabaseName</span></span>
<span data-ttu-id="7e03b-113">SQL 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e03b-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="7e03b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e03b-114">-DefaultProfile</span></span>
<span data-ttu-id="7e03b-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7e03b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e03b-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e03b-116">-PassThru</span></span>
<span data-ttu-id="7e03b-117">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="7e03b-117">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e03b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e03b-118">-ResourceGroupName</span></span>
<span data-ttu-id="7e03b-119">SQL 데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e03b-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="7e03b-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="7e03b-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="7e03b-121">복원 지점 만들기 날짜를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e03b-121">Specifies the restore point creation date.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e03b-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7e03b-122">-ServerName</span></span>
<span data-ttu-id="7e03b-123">데이터베이스를 호스트하는 AzureSQL 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e03b-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="7e03b-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e03b-124">-Confirm</span></span>
<span data-ttu-id="7e03b-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e03b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e03b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e03b-126">-WhatIf</span></span>
<span data-ttu-id="7e03b-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7e03b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e03b-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e03b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e03b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e03b-129">CommonParameters</span></span>
<span data-ttu-id="7e03b-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7e03b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e03b-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7e03b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e03b-132">입력</span><span class="sxs-lookup"><span data-stu-id="7e03b-132">INPUTS</span></span>

### <span data-ttu-id="7e03b-133">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="7e03b-133">System.DateTime</span></span>

### <span data-ttu-id="7e03b-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7e03b-134">System.String</span></span>

## <span data-ttu-id="7e03b-135">출력</span><span class="sxs-lookup"><span data-stu-id="7e03b-135">OUTPUTS</span></span>

### <span data-ttu-id="7e03b-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="7e03b-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="7e03b-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7e03b-137">NOTES</span></span>

## <span data-ttu-id="7e03b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e03b-138">RELATED LINKS</span></span>

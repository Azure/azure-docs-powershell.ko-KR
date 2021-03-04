---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 476340114ae2bc6e436301f37a0a9aeaf9fa5e92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957920"
---
# <span data-ttu-id="c370f-101">Remove-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="c370f-101">Remove-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="c370f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c370f-102">SYNOPSIS</span></span>
<span data-ttu-id="c370f-103">데이터베이스에서 주어진 복원 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c370f-103">Removes given restore point from a SQL Database.</span></span>

## <span data-ttu-id="c370f-104">구문</span><span class="sxs-lookup"><span data-stu-id="c370f-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c370f-105">설명</span><span class="sxs-lookup"><span data-stu-id="c370f-105">DESCRIPTION</span></span>
<span data-ttu-id="c370f-106">**Remove-AzSqlDatabaseRestorePoint** cmdlet은 Azure SQL 복원 지점을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c370f-106">The **Remove-AzSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>
<span data-ttu-id="c370f-107">이 cmdlet은 현재 Azure SQL Server 데이터베이스의 SQL Server Datawarehouse 서비스에서 SQL 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c370f-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="c370f-108">예제</span><span class="sxs-lookup"><span data-stu-id="c370f-108">EXAMPLES</span></span>

### <span data-ttu-id="c370f-109">예제 1: 복원 지점 제거</span><span class="sxs-lookup"><span data-stu-id="c370f-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="c370f-110">이 명령은 생성 날짜가 주어진 Azure SQL 데이터베이스의 복원 지점을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c370f-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="c370f-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c370f-111">PARAMETERS</span></span>

### <span data-ttu-id="c370f-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c370f-112">-DatabaseName</span></span>
<span data-ttu-id="c370f-113">데이터베이스의 이름을 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c370f-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="c370f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c370f-114">-DefaultProfile</span></span>
<span data-ttu-id="c370f-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c370f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c370f-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c370f-116">-PassThru</span></span>
<span data-ttu-id="c370f-117">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c370f-117">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c370f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c370f-118">-ResourceGroupName</span></span>
<span data-ttu-id="c370f-119">데이터베이스가 할당된 리소스 그룹의 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c370f-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="c370f-120">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="c370f-120">-RestorePointCreationDate</span></span>
<span data-ttu-id="c370f-121">복원 지점 만들기 날짜를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c370f-121">Specifies the restore point creation date.</span></span>

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

### <span data-ttu-id="c370f-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c370f-122">-ServerName</span></span>
<span data-ttu-id="c370f-123">데이터베이스를 호스트하는 AzureSQL 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c370f-123">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="c370f-124">-확인</span><span class="sxs-lookup"><span data-stu-id="c370f-124">-Confirm</span></span>
<span data-ttu-id="c370f-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c370f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c370f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c370f-126">-WhatIf</span></span>
<span data-ttu-id="c370f-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c370f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c370f-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c370f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c370f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c370f-129">CommonParameters</span></span>
<span data-ttu-id="c370f-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c370f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c370f-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c370f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c370f-132">입력</span><span class="sxs-lookup"><span data-stu-id="c370f-132">INPUTS</span></span>

### <span data-ttu-id="c370f-133">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="c370f-133">System.DateTime</span></span>

### <span data-ttu-id="c370f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c370f-134">System.String</span></span>

## <span data-ttu-id="c370f-135">출력</span><span class="sxs-lookup"><span data-stu-id="c370f-135">OUTPUTS</span></span>

### <span data-ttu-id="c370f-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="c370f-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="c370f-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c370f-137">NOTES</span></span>

## <span data-ttu-id="c370f-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c370f-138">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: caca08a5a9390d3e80fdef8309244a8a4d29aec0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196065"
---
# <span data-ttu-id="1526c-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="1526c-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="1526c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1526c-102">SYNOPSIS</span></span>
<span data-ttu-id="1526c-103">Azure SQL 데이터베이스의 감사 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1526c-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="1526c-104">구문</span><span class="sxs-lookup"><span data-stu-id="1526c-104">SYNTAX</span></span>

### <span data-ttu-id="1526c-105">DatabaseParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1526c-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1526c-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1526c-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1526c-107">설명</span><span class="sxs-lookup"><span data-stu-id="1526c-107">DESCRIPTION</span></span>
<span data-ttu-id="1526c-108">**Remove-AzSqlDatabaseAudit cmdlet은** Azure SQL 데이터베이스의 감사 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1526c-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="1526c-109">cmdlet을 사용하려면 *ResourceGroupName,* *ServerName* 및 *DatabaseName* 매개 변수를 사용하여 데이터베이스를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="1526c-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="1526c-110">예제</span><span class="sxs-lookup"><span data-stu-id="1526c-110">EXAMPLES</span></span>

### <span data-ttu-id="1526c-111">예제 1: Azure SQL 데이터베이스의 감사 설정 제거</span><span class="sxs-lookup"><span data-stu-id="1526c-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="1526c-112">예제 2: 파이프라인을 통해 Azure SQL 데이터베이스의 감사 설정 제거</span><span class="sxs-lookup"><span data-stu-id="1526c-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="1526c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1526c-113">PARAMETERS</span></span>

### <span data-ttu-id="1526c-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1526c-114">-DatabaseName</span></span>
<span data-ttu-id="1526c-115">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1526c-115">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1526c-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="1526c-116">-DatabaseObject</span></span>
<span data-ttu-id="1526c-117">감사 정책을 관리하는 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1526c-117">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1526c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1526c-118">-DefaultProfile</span></span>
<span data-ttu-id="1526c-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1526c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1526c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1526c-120">-ResourceGroupName</span></span>
<span data-ttu-id="1526c-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1526c-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1526c-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1526c-122">-ServerName</span></span>
<span data-ttu-id="1526c-123">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1526c-123">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1526c-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1526c-124">-Confirm</span></span>
<span data-ttu-id="1526c-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1526c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1526c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1526c-126">-WhatIf</span></span>
<span data-ttu-id="1526c-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1526c-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1526c-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1526c-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1526c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1526c-129">CommonParameters</span></span>
<span data-ttu-id="1526c-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1526c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1526c-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1526c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1526c-132">입력</span><span class="sxs-lookup"><span data-stu-id="1526c-132">INPUTS</span></span>

### <span data-ttu-id="1526c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1526c-133">System.String</span></span>

### <span data-ttu-id="1526c-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1526c-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="1526c-135">출력</span><span class="sxs-lookup"><span data-stu-id="1526c-135">OUTPUTS</span></span>

### <span data-ttu-id="1526c-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1526c-136">System.Boolean</span></span>

## <span data-ttu-id="1526c-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1526c-137">NOTES</span></span>

## <span data-ttu-id="1526c-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1526c-138">RELATED LINKS</span></span>

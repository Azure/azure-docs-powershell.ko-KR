---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
ms.openlocfilehash: b6b6ca6bea6dd980b429ee17e69fb86556dd6ce0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183361"
---
# <span data-ttu-id="13ffd-101">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="13ffd-101">Get-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="13ffd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="13ffd-103">Azure SQL 데이터베이스의 감사 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13ffd-103">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="13ffd-104">구문</span><span class="sxs-lookup"><span data-stu-id="13ffd-104">SYNTAX</span></span>

### <span data-ttu-id="13ffd-105">DatabaseParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="13ffd-105">DatabaseParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13ffd-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="13ffd-106">DatabaseObjectParameterSet</span></span>
```
Get-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13ffd-107">설명</span><span class="sxs-lookup"><span data-stu-id="13ffd-107">DESCRIPTION</span></span>
<span data-ttu-id="13ffd-108">**Get-AzSqlDatabaseAudit** cmdlet은 Azure SQL 데이터베이스의 감사 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13ffd-108">The **Get-AzSqlDatabaseAudit** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="13ffd-109">cmdlet을 사용하려면 *ResourceGroupName,* *ServerName* 및 *DatabaseName* 매개 변수를 사용하여 데이터베이스를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="13ffd-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="13ffd-110">예제</span><span class="sxs-lookup"><span data-stu-id="13ffd-110">EXAMPLES</span></span>

### <span data-ttu-id="13ffd-111">예제 1: Azure SQL 데이터베이스의 감사 설정</span><span class="sxs-lookup"><span data-stu-id="13ffd-111">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="13ffd-112">예제 2: 파이프라인을 통해 Azure SQL 데이터베이스의 감사 설정</span><span class="sxs-lookup"><span data-stu-id="13ffd-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAudit
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="13ffd-113">예제 3: Azure SQL 데이터베이스의 감사 설정</span><span class="sxs-lookup"><span data-stu-id="13ffd-113">Example 3: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Disabled
WorkspaceResourceId                 :
```

## <span data-ttu-id="13ffd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13ffd-114">PARAMETERS</span></span>

### <span data-ttu-id="13ffd-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="13ffd-115">-DatabaseName</span></span>
<span data-ttu-id="13ffd-116">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13ffd-116">SQL Database name.</span></span>

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

### <span data-ttu-id="13ffd-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="13ffd-117">-DatabaseObject</span></span>
<span data-ttu-id="13ffd-118">감사 정책을 관리하는 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="13ffd-118">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="13ffd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ffd-119">-DefaultProfile</span></span>
<span data-ttu-id="13ffd-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13ffd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13ffd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13ffd-121">-ResourceGroupName</span></span>
<span data-ttu-id="13ffd-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13ffd-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="13ffd-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="13ffd-123">-ServerName</span></span>
<span data-ttu-id="13ffd-124">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13ffd-124">SQL server name.</span></span>

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

### <span data-ttu-id="13ffd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ffd-125">CommonParameters</span></span>
<span data-ttu-id="13ffd-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13ffd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ffd-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="13ffd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ffd-128">입력</span><span class="sxs-lookup"><span data-stu-id="13ffd-128">INPUTS</span></span>

### <span data-ttu-id="13ffd-129">System.String</span><span class="sxs-lookup"><span data-stu-id="13ffd-129">System.String</span></span>

### <span data-ttu-id="13ffd-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="13ffd-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="13ffd-131">출력</span><span class="sxs-lookup"><span data-stu-id="13ffd-131">OUTPUTS</span></span>

### <span data-ttu-id="13ffd-132">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="13ffd-132">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="13ffd-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="13ffd-133">NOTES</span></span>

## <span data-ttu-id="13ffd-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13ffd-134">RELATED LINKS</span></span>

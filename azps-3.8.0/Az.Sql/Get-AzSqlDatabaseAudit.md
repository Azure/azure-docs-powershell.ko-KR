---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
ms.openlocfilehash: b6b6ca6bea6dd980b429ee17e69fb86556dd6ce0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041564"
---
# <span data-ttu-id="f172b-101">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="f172b-101">Get-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="f172b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f172b-102">SYNOPSIS</span></span>
<span data-ttu-id="f172b-103">Azure SQL 데이터베이스의 감사 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f172b-103">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="f172b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f172b-104">SYNTAX</span></span>

### <span data-ttu-id="f172b-105">DatabaseParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f172b-105">DatabaseParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f172b-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f172b-106">DatabaseObjectParameterSet</span></span>
```
Get-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f172b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f172b-107">DESCRIPTION</span></span>
<span data-ttu-id="f172b-108">**AzSqlDatabaseAudit** Cmdlet은 Azure SQL 데이터베이스의 감사 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f172b-108">The **Get-AzSqlDatabaseAudit** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="f172b-109">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="f172b-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="f172b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f172b-110">EXAMPLES</span></span>

### <span data-ttu-id="f172b-111">예제 1: Azure SQL 데이터베이스의 감사 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="f172b-111">Example 1: Get the auditing settings of an Azure SQL database</span></span>
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

### <span data-ttu-id="f172b-112">예제 2: Azure SQL 데이터베이스의 감사 설정, 파이프라인 가져오기</span><span class="sxs-lookup"><span data-stu-id="f172b-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL database</span></span>
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

### <span data-ttu-id="f172b-113">예제 3: Azure SQL 데이터베이스의 감사 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="f172b-113">Example 3: Get the auditing settings of an Azure SQL database</span></span>
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

## <span data-ttu-id="f172b-114">변수</span><span class="sxs-lookup"><span data-stu-id="f172b-114">PARAMETERS</span></span>

### <span data-ttu-id="f172b-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f172b-115">-DatabaseName</span></span>
<span data-ttu-id="f172b-116">SQL 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f172b-116">SQL Database name.</span></span>

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

### <span data-ttu-id="f172b-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="f172b-117">-DatabaseObject</span></span>
<span data-ttu-id="f172b-118">감사 정책을 관리 하는 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f172b-118">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="f172b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f172b-119">-DefaultProfile</span></span>
<span data-ttu-id="f172b-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f172b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f172b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f172b-121">-ResourceGroupName</span></span>
<span data-ttu-id="f172b-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f172b-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="f172b-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f172b-123">-ServerName</span></span>
<span data-ttu-id="f172b-124">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f172b-124">SQL server name.</span></span>

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

### <span data-ttu-id="f172b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f172b-125">CommonParameters</span></span>
<span data-ttu-id="f172b-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f172b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f172b-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f172b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f172b-128">입력</span><span class="sxs-lookup"><span data-stu-id="f172b-128">INPUTS</span></span>

### <span data-ttu-id="f172b-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f172b-129">System.String</span></span>

### <span data-ttu-id="f172b-130">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="f172b-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f172b-131">출력</span><span class="sxs-lookup"><span data-stu-id="f172b-131">OUTPUTS</span></span>

### <span data-ttu-id="f172b-132">Microsoft. .Sql. 감사. DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="f172b-132">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="f172b-133">상속자</span><span class="sxs-lookup"><span data-stu-id="f172b-133">NOTES</span></span>

## <span data-ttu-id="f172b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f172b-134">RELATED LINKS</span></span>

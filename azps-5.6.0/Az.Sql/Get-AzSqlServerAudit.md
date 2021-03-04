---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Get-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
ms.openlocfilehash: 4c9311bfba05862b1c073be5ec5b07106d8b19a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982123"
---
# <span data-ttu-id="c9c69-101">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="c9c69-101">Get-AzSqlServerAudit</span></span>

## <span data-ttu-id="c9c69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9c69-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c69-103">Azure 서버의 감사 설정을 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c69-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="c9c69-104">구문</span><span class="sxs-lookup"><span data-stu-id="c9c69-104">SYNTAX</span></span>

### <span data-ttu-id="c9c69-105">ServerParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c9c69-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9c69-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9c69-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9c69-107">설명</span><span class="sxs-lookup"><span data-stu-id="c9c69-107">DESCRIPTION</span></span>
<span data-ttu-id="c9c69-108">**Get-AzSqlServerAudit** cmdlet은 Azure SQL 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9c69-108">The **Get-AzSqlServerAudit** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="c9c69-109">*Server를 식별하기 위해 ResourceGroupName* 및 *ServerName* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c69-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="c9c69-110">예제</span><span class="sxs-lookup"><span data-stu-id="c9c69-110">EXAMPLES</span></span>

### <span data-ttu-id="c9c69-111">예제 1: Azure 서버의 감사 SQL</span><span class="sxs-lookup"><span data-stu-id="c9c69-111">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
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

### <span data-ttu-id="c9c69-112">예제 2: 파이프라인을 통해 Azure 서버의 감사 설정 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c69-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAudit
ServerName                          : server01
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

### <span data-ttu-id="c9c69-113">예제 3: Azure 서버의 감사 SQL</span><span class="sxs-lookup"><span data-stu-id="c9c69-113">Example 3: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
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

## <span data-ttu-id="c9c69-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c9c69-114">PARAMETERS</span></span>

### <span data-ttu-id="c9c69-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9c69-115">-AsJob</span></span>
<span data-ttu-id="c9c69-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c9c69-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9c69-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c69-117">-DefaultProfile</span></span>
<span data-ttu-id="c9c69-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9c69-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9c69-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9c69-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9c69-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9c69-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c69-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c9c69-121">-ServerName</span></span>
<span data-ttu-id="c9c69-122">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9c69-122">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c69-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="c9c69-123">-ServerObject</span></span>
<span data-ttu-id="c9c69-124">서버 개체는 감사 정책을 관리합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c69-124">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c69-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c69-125">CommonParameters</span></span>
<span data-ttu-id="c9c69-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9c69-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c69-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9c69-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c69-128">입력</span><span class="sxs-lookup"><span data-stu-id="c9c69-128">INPUTS</span></span>

### <span data-ttu-id="c9c69-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c9c69-129">System.String</span></span>

### <span data-ttu-id="c9c69-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="c9c69-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="c9c69-131">출력</span><span class="sxs-lookup"><span data-stu-id="c9c69-131">OUTPUTS</span></span>

### <span data-ttu-id="c9c69-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="c9c69-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="c9c69-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c9c69-133">NOTES</span></span>

## <span data-ttu-id="c9c69-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9c69-134">RELATED LINKS</span></span>

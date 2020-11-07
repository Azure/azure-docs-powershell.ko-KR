---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
ms.openlocfilehash: eda8123b9ff309f4834f6e954e5e0b1e01b3f1e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873635"
---
# <span data-ttu-id="2be73-101">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2be73-101">Get-AzSqlServerAudit</span></span>

## <span data-ttu-id="2be73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2be73-102">SYNOPSIS</span></span>
<span data-ttu-id="2be73-103">Azure SQL server의 감사 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2be73-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="2be73-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2be73-104">SYNTAX</span></span>

### <span data-ttu-id="2be73-105">ServerParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2be73-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2be73-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2be73-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2be73-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2be73-107">DESCRIPTION</span></span>
<span data-ttu-id="2be73-108">**AzSqlServerAudit** Cmdlet은 Azure SQL server의 감사 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2be73-108">The **Get-AzSqlServerAudit** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="2be73-109">서버를 식별 하는 *ResourceGroupName* 및 *ServerName* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2be73-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="2be73-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2be73-110">EXAMPLES</span></span>

### <span data-ttu-id="2be73-111">예제 1: Azure SQL server의 감사 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="2be73-111">Example 1: Get the auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="2be73-112">예제 2: Azure SQL server의 감사 설정, 파이프라인 가져오기</span><span class="sxs-lookup"><span data-stu-id="2be73-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL server</span></span>
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

### <span data-ttu-id="2be73-113">예제 3: Azure SQL server의 감사 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="2be73-113">Example 3: Get the auditing settings of an Azure SQL server</span></span>
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

## <span data-ttu-id="2be73-114">변수</span><span class="sxs-lookup"><span data-stu-id="2be73-114">PARAMETERS</span></span>

### <span data-ttu-id="2be73-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2be73-115">-AsJob</span></span>
<span data-ttu-id="2be73-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2be73-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2be73-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be73-117">-DefaultProfile</span></span>
<span data-ttu-id="2be73-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2be73-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2be73-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2be73-119">-ResourceGroupName</span></span>
<span data-ttu-id="2be73-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2be73-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="2be73-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2be73-121">-ServerName</span></span>
<span data-ttu-id="2be73-122">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2be73-122">SQL server name.</span></span>

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

### <span data-ttu-id="2be73-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="2be73-123">-ServerObject</span></span>
<span data-ttu-id="2be73-124">감사 정책을 관리 하는 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2be73-124">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="2be73-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be73-125">CommonParameters</span></span>
<span data-ttu-id="2be73-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2be73-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2be73-127">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2be73-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be73-128">입력</span><span class="sxs-lookup"><span data-stu-id="2be73-128">INPUTS</span></span>

### <span data-ttu-id="2be73-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2be73-129">System.String</span></span>

### <span data-ttu-id="2be73-130">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="2be73-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="2be73-131">출력</span><span class="sxs-lookup"><span data-stu-id="2be73-131">OUTPUTS</span></span>

### <span data-ttu-id="2be73-132">Microsoft. .Sql. 감사. ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="2be73-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="2be73-133">상속자</span><span class="sxs-lookup"><span data-stu-id="2be73-133">NOTES</span></span>

## <span data-ttu-id="2be73-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2be73-134">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: c4f3687b2e520783c4b0392e1711dcea976e0c05
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489335"
---
# <span data-ttu-id="93eed-101">Get-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="93eed-101">Get-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="93eed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93eed-102">SYNOPSIS</span></span>
<span data-ttu-id="93eed-103">Azure SQL 서버의 Microsoft 지원 작업 감사 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="93eed-103">Gets the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="93eed-104">구문</span><span class="sxs-lookup"><span data-stu-id="93eed-104">SYNTAX</span></span>

### <span data-ttu-id="93eed-105">ServerParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="93eed-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93eed-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93eed-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93eed-107">설명</span><span class="sxs-lookup"><span data-stu-id="93eed-107">DESCRIPTION</span></span>
<span data-ttu-id="93eed-108">**Get-AzSqlServerMSSupportAudit** cmdlet은 Azure SQL 서버의 Microsoft 지원 작업 감사 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="93eed-108">The **Get-AzSqlServerMSSupportAudit** cmdlet gets the Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="93eed-109">서버를 식별하는 *ResourceGroupName* 및 *ServerName* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="93eed-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="93eed-110">예제</span><span class="sxs-lookup"><span data-stu-id="93eed-110">EXAMPLES</span></span>

### <span data-ttu-id="93eed-111">예제 1: Azure SQL 서버의 Microsoft 지원 작업 감사 설정 다운로드</span><span class="sxs-lookup"><span data-stu-id="93eed-111">Example 1: Get the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerMSSupportAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="93eed-112">예제 2: 파이프라인을 통해 Microsoft에서 Azure SQL 서버의 작업 감사 설정을 지원</span><span class="sxs-lookup"><span data-stu-id="93eed-112">Example 2: Get, through pipeline, the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerMSSupportAudit
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="93eed-113">예제 3: Azure SQL 서버의 Microsoft 지원 작업 감사 설정 다운로드</span><span class="sxs-lookup"><span data-stu-id="93eed-113">Example 3: Get the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerMSSupportAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Disabled
WorkspaceResourceId                 :
```

## <span data-ttu-id="93eed-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93eed-114">PARAMETERS</span></span>

### <span data-ttu-id="93eed-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93eed-115">-AsJob</span></span>
<span data-ttu-id="93eed-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="93eed-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93eed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93eed-117">-DefaultProfile</span></span>
<span data-ttu-id="93eed-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93eed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93eed-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93eed-119">-ResourceGroupName</span></span>
<span data-ttu-id="93eed-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93eed-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="93eed-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="93eed-121">-ServerName</span></span>
<span data-ttu-id="93eed-122">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93eed-122">SQL server name.</span></span>

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

### <span data-ttu-id="93eed-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="93eed-123">-ServerObject</span></span>
<span data-ttu-id="93eed-124">감사 정책을 관리하는 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="93eed-124">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="93eed-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93eed-125">CommonParameters</span></span>
<span data-ttu-id="93eed-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="93eed-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93eed-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="93eed-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93eed-128">입력</span><span class="sxs-lookup"><span data-stu-id="93eed-128">INPUTS</span></span>

### <span data-ttu-id="93eed-129">System.String</span><span class="sxs-lookup"><span data-stu-id="93eed-129">System.String</span></span>

### <span data-ttu-id="93eed-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="93eed-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="93eed-131">출력</span><span class="sxs-lookup"><span data-stu-id="93eed-131">OUTPUTS</span></span>

### <span data-ttu-id="93eed-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="93eed-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="93eed-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="93eed-133">NOTES</span></span>

## <span data-ttu-id="93eed-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93eed-134">RELATED LINKS</span></span>

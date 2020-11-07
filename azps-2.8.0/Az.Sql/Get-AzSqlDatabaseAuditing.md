---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
ms.openlocfilehash: 641ab27f75950a2c15035a7787346250a41f9ab9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873727"
---
# <span data-ttu-id="ff7e3-101">Get-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="ff7e3-101">Get-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="ff7e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff7e3-102">SYNOPSIS</span></span>
<span data-ttu-id="ff7e3-103">**중요:이 cmdlet은 (는) 더 이상 사용 되지 않으며, [Get-AzSqlDatbaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseaudit) 에서 바꿉니다.**</span><span class="sxs-lookup"><span data-stu-id="ff7e3-103">**Important: This cmdlet is deprecated, [Get-AzSqlDatbaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseaudit) is replacing it.**</span></span>

<span data-ttu-id="ff7e3-104">Azure SQL 데이터베이스의 감사 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-104">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="ff7e3-105">구문과</span><span class="sxs-lookup"><span data-stu-id="ff7e3-105">SYNTAX</span></span>

### <span data-ttu-id="ff7e3-106">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ff7e3-106">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-BlobStorage] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff7e3-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="ff7e3-107">EventHubSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-EventHub] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff7e3-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="ff7e3-108">LogAnalyticsSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff7e3-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="ff7e3-109">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff7e3-110">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="ff7e3-110">EventHubByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff7e3-111">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="ff7e3-111">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff7e3-112">설명은</span><span class="sxs-lookup"><span data-stu-id="ff7e3-112">DESCRIPTION</span></span>
<span data-ttu-id="ff7e3-113">**AzSqlDatabaseAuditing** Cmdlet은 Azure SQL 데이터베이스의 감사 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-113">The **Get-AzSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="ff7e3-114">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-114">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="ff7e3-115">감사 로그 대상은 BlobStorage, LogAnalytics 또는 EventHub (지정 하지 않은 경우 기본적으로 BlobStorage)와 같은 스위치 매개 변수 중 하나를 지정 하 여 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-115">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="ff7e3-116">예제의</span><span class="sxs-lookup"><span data-stu-id="ff7e3-116">EXAMPLES</span></span>

### <span data-ttu-id="ff7e3-117">예제 1: Azure SQL 데이터베이스의 blob 저장소 감사 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="ff7e3-117">Example 1: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="ff7e3-118">예제 2: Azure SQL 데이터베이스의 blob 저장소 감사 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="ff7e3-118">Example 2: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorage
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="ff7e3-119">예제 3: Azure SQL 데이터베이스의 blob 저장소 감사 설정, 파이프라인으로 가져오기</span><span class="sxs-lookup"><span data-stu-id="ff7e3-119">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAuditing
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="ff7e3-120">예제 4: Azure SQL 데이터베이스의 이벤트 허브 감사 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="ff7e3-120">Example 4: Get the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="ff7e3-121">예제 5: Azure SQL 데이터베이스의 이벤트 허브 감사 설정 및 파이프라인 가져오기</span><span class="sxs-lookup"><span data-stu-id="ff7e3-121">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>$database = Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\>$database | Get-AzSqlDatabaseAuditing -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="ff7e3-122">예제 6: Azure SQL 데이터베이스의 로그 분석 감사 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="ff7e3-122">Example 6: Get the log analytics auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
DatabaseName        : database01
AuditAction         : {}
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="ff7e3-123">변수</span><span class="sxs-lookup"><span data-stu-id="ff7e3-123">PARAMETERS</span></span>

### <span data-ttu-id="ff7e3-124">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="ff7e3-124">-BlobStorage</span></span>
<span data-ttu-id="ff7e3-125">감사 로그 대상이 blob storage 임을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-125">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7e3-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ff7e3-126">-DatabaseName</span></span>
<span data-ttu-id="ff7e3-127">SQL 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-127">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7e3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff7e3-128">-DefaultProfile</span></span>
<span data-ttu-id="ff7e3-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff7e3-130">-EventHub</span><span class="sxs-lookup"><span data-stu-id="ff7e3-130">-EventHub</span></span>
<span data-ttu-id="ff7e3-131">감사 로그 대상이 이벤트 허브 인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-131">Specifies that audit logs destination is event hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7e3-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff7e3-132">-InputObject</span></span>
<span data-ttu-id="ff7e3-133">감사 정책을 관리 하는 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-133">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7e3-134">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="ff7e3-134">-LogAnalytics</span></span>
<span data-ttu-id="ff7e3-135">감사 로그 대상이 로그 분석 임을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-135">Specifies that audit logs destination is log analytics</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7e3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff7e3-136">-ResourceGroupName</span></span>
<span data-ttu-id="ff7e3-137">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7e3-138">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ff7e3-138">-ServerName</span></span>
<span data-ttu-id="ff7e3-139">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-139">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7e3-140">-확인</span><span class="sxs-lookup"><span data-stu-id="ff7e3-140">-Confirm</span></span>
<span data-ttu-id="ff7e3-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff7e3-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff7e3-142">-WhatIf</span></span>
<span data-ttu-id="ff7e3-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff7e3-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff7e3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff7e3-145">CommonParameters</span></span>
<span data-ttu-id="ff7e3-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff7e3-147">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff7e3-148">입력</span><span class="sxs-lookup"><span data-stu-id="ff7e3-148">INPUTS</span></span>

### <span data-ttu-id="ff7e3-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ff7e3-149">System.String</span></span>

### <span data-ttu-id="ff7e3-150">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="ff7e3-150">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="ff7e3-151">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ff7e3-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ff7e3-152">출력</span><span class="sxs-lookup"><span data-stu-id="ff7e3-152">OUTPUTS</span></span>

### <span data-ttu-id="ff7e3-153">Microsoft. .Sql. 감사. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="ff7e3-153">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="ff7e3-154">상속자</span><span class="sxs-lookup"><span data-stu-id="ff7e3-154">NOTES</span></span>

## <span data-ttu-id="ff7e3-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff7e3-155">RELATED LINKS</span></span>

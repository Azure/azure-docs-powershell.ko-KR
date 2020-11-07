---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
ms.openlocfilehash: ba225571780d4d09dfd5ecc1b47132462468b734
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698951"
---
# <span data-ttu-id="50bf4-101">Get-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="50bf4-101">Get-AzSqlServerAuditing</span></span>

## <span data-ttu-id="50bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="50bf4-103">Azure SQL server의 감사 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="50bf4-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="50bf4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="50bf4-104">SYNTAX</span></span>

### <span data-ttu-id="50bf4-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="50bf4-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50bf4-106">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="50bf4-106">EventHubSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50bf4-107">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="50bf4-107">LogAnalyticsSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50bf4-108">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="50bf4-108">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50bf4-109">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="50bf4-109">EventHubByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50bf4-110">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="50bf4-110">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50bf4-111">설명은</span><span class="sxs-lookup"><span data-stu-id="50bf4-111">DESCRIPTION</span></span>
<span data-ttu-id="50bf4-112">**AzSqlServerAuditing** Cmdlet은 Azure SQL server의 감사 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="50bf4-112">The **Get-AzSqlServerAuditing** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="50bf4-113">서버를 식별 하는 *ResourceGroupName* 및 *ServerName* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50bf4-113">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="50bf4-114">감사 로그 대상은 BlobStorage, LogAnalytics 또는 EventHub (지정 하지 않은 경우 기본적으로 BlobStorage)와 같은 스위치 매개 변수 중 하나를 지정 하 여 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="50bf4-114">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="50bf4-115">예제의</span><span class="sxs-lookup"><span data-stu-id="50bf4-115">EXAMPLES</span></span>

### <span data-ttu-id="50bf4-116">예제 1: Azure SQL server의 blob 저장소 감사 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="50bf4-116">Example 1: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

### <span data-ttu-id="50bf4-117">예제 2: Azure SQL server의 blob 저장소 감사 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="50bf4-117">Example 2: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -BlobStorage
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

### <span data-ttu-id="50bf4-118">예제 3: Azure SQL server의 blob 저장소 감사 설정, 파이프라인으로 가져오기</span><span class="sxs-lookup"><span data-stu-id="50bf4-118">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAuditing -BlobStorage
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

### <span data-ttu-id="50bf4-119">예제 4: Azure SQL server의 이벤트 허브 감사 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="50bf4-119">Example 4: Get the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="50bf4-120">예제 5: Get, 파이프라인, Azure SQL server의 이벤트 허브 감사 설정</span><span class="sxs-lookup"><span data-stu-id="50bf4-120">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>$server = Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
PS C:\>$server | Get-AzSqlServerAuditing -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="50bf4-121">예제 6: Azure SQL server의 로그 분석 감사 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="50bf4-121">Example 6: Get the log analytics auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -LogAnalytics
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="50bf4-122">변수</span><span class="sxs-lookup"><span data-stu-id="50bf4-122">PARAMETERS</span></span>

### <span data-ttu-id="50bf4-123">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="50bf4-123">-BlobStorage</span></span>
<span data-ttu-id="50bf4-124">감사 로그 대상이 blob storage 임을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50bf4-124">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="50bf4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50bf4-125">-DefaultProfile</span></span>
<span data-ttu-id="50bf4-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50bf4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50bf4-127">-EventHub</span><span class="sxs-lookup"><span data-stu-id="50bf4-127">-EventHub</span></span>
<span data-ttu-id="50bf4-128">감사 로그 대상이 이벤트 허브 인지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50bf4-128">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="50bf4-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50bf4-129">-InputObject</span></span>
<span data-ttu-id="50bf4-130">감사 정책을 관리 하는 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="50bf4-130">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50bf4-131">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="50bf4-131">-LogAnalytics</span></span>
<span data-ttu-id="50bf4-132">감사 로그 대상이 로그 분석 임을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50bf4-132">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="50bf4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50bf4-133">-ResourceGroupName</span></span>
<span data-ttu-id="50bf4-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50bf4-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="50bf4-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="50bf4-135">-ServerName</span></span>
<span data-ttu-id="50bf4-136">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50bf4-136">SQL server name.</span></span>

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

### <span data-ttu-id="50bf4-137">-확인</span><span class="sxs-lookup"><span data-stu-id="50bf4-137">-Confirm</span></span>
<span data-ttu-id="50bf4-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="50bf4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50bf4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50bf4-139">-WhatIf</span></span>
<span data-ttu-id="50bf4-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="50bf4-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50bf4-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50bf4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50bf4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50bf4-142">CommonParameters</span></span>
<span data-ttu-id="50bf4-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="50bf4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50bf4-144">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="50bf4-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50bf4-145">입력</span><span class="sxs-lookup"><span data-stu-id="50bf4-145">INPUTS</span></span>

### <span data-ttu-id="50bf4-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="50bf4-146">System.String</span></span>

### <span data-ttu-id="50bf4-147">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="50bf4-147">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="50bf4-148">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="50bf4-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="50bf4-149">출력</span><span class="sxs-lookup"><span data-stu-id="50bf4-149">OUTPUTS</span></span>

### <span data-ttu-id="50bf4-150">Microsoft. .Sql. 감사. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="50bf4-150">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="50bf4-151">상속자</span><span class="sxs-lookup"><span data-stu-id="50bf4-151">NOTES</span></span>

## <span data-ttu-id="50bf4-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50bf4-152">RELATED LINKS</span></span>

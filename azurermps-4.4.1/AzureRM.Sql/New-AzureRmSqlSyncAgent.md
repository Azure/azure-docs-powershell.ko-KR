---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgent.md
ms.openlocfilehash: e296e338d519537f688085fc5c142e3c12804b0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702051"
---
# <span data-ttu-id="eb394-101">New-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="eb394-101">New-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="eb394-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb394-102">SYNOPSIS</span></span>
<span data-ttu-id="eb394-103">Azure SQL 동기화 에이전트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb394-103">Creates an Azure SQL Sync Agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb394-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eb394-104">SYNTAX</span></span>

### <span data-ttu-id="eb394-105">SyncDatabaseComponent (기본값)</span><span class="sxs-lookup"><span data-stu-id="eb394-105">SyncDatabaseComponent (Default)</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseName <String> [-SyncDatabaseServerName <String>]
 [-SyncDatabaseResourceGroupName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb394-106">SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="eb394-106">SyncDatabaseResourceID</span></span>
```
New-AzureRmSqlSyncAgent [-Name] <String> -SyncDatabaseResourceID <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb394-107">설명은</span><span class="sxs-lookup"><span data-stu-id="eb394-107">DESCRIPTION</span></span>
<span data-ttu-id="eb394-108">**AzureRmSqlSyncAgent** Cmdlet은 Azure SQL 동기화 에이전트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb394-108">The **New-AzureRmSqlSyncAgent** cmdlet creates an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="eb394-109">예제의</span><span class="sxs-lookup"><span data-stu-id="eb394-109">EXAMPLES</span></span>

### <span data-ttu-id="eb394-110">예제 1: Azure SQL server에 대 한 동기화 에이전트 만들기</span><span class="sxs-lookup"><span data-stu-id="eb394-110">Example 1: Create a sync agent for an Azure SQL server.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" -SyncDatabaseServerName "syncDatabaseServer01" 
-SyncDatabaseName "syncDatabaseName01" -SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 
Version                     : 4.2.0.0
IsUpToDate                  : True
ExpiryTime                  : 12/31/9999 11:59:59 PM
State                       : NeverConnected
```

<span data-ttu-id="eb394-111">이 명령은 Azure SQL server에 대 한 동기화 에이전트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb394-111">This command creates a sync agent for an Azure SQL server.</span></span>

## <span data-ttu-id="eb394-112">변수</span><span class="sxs-lookup"><span data-stu-id="eb394-112">PARAMETERS</span></span>

### <span data-ttu-id="eb394-113">-확인</span><span class="sxs-lookup"><span data-stu-id="eb394-113">-Confirm</span></span>
<span data-ttu-id="eb394-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb394-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb394-115">-이름</span><span class="sxs-lookup"><span data-stu-id="eb394-115">-Name</span></span>
<span data-ttu-id="eb394-116">동기화 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb394-116">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb394-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb394-117">-ResourceGroupName</span></span>
<span data-ttu-id="eb394-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb394-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="eb394-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eb394-119">-ServerName</span></span>
<span data-ttu-id="eb394-120">동기화 에이전트가 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb394-120">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="eb394-121">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb394-121">-SyncDatabaseName</span></span>
<span data-ttu-id="eb394-122">동기화 관련 메타 데이터를 저장 하는 데 사용 되는 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="eb394-122">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb394-123">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb394-123">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="eb394-124">동기화 메타 데이터 데이터베이스가 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="eb394-124">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb394-125">-SyncDatabaseResourceID</span><span class="sxs-lookup"><span data-stu-id="eb394-125">-SyncDatabaseResourceID</span></span>
<span data-ttu-id="eb394-126">동기화 메타 데이터 데이터베이스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="eb394-126">The resource ID of  the sync metadata database.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseResourceID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb394-127">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="eb394-127">-SyncDatabaseServerName</span></span>
<span data-ttu-id="eb394-128">동기화 메타 데이터 데이터베이스가 호스팅되는 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="eb394-128">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: SyncDatabaseComponent
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb394-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb394-129">-WhatIf</span></span>
<span data-ttu-id="eb394-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eb394-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb394-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eb394-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb394-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb394-132">-DefaultProfile</span></span>
<span data-ttu-id="eb394-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eb394-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb394-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb394-134">CommonParameters</span></span>
<span data-ttu-id="eb394-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb394-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb394-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb394-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb394-137">입력</span><span class="sxs-lookup"><span data-stu-id="eb394-137">INPUTS</span></span>

## <span data-ttu-id="eb394-138">출력</span><span class="sxs-lookup"><span data-stu-id="eb394-138">OUTPUTS</span></span>

### <span data-ttu-id="eb394-139">AzureSqlSyncAgentModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb394-139">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="eb394-140">상속자</span><span class="sxs-lookup"><span data-stu-id="eb394-140">NOTES</span></span>

## <span data-ttu-id="eb394-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb394-141">RELATED LINKS</span></span>

[<span data-ttu-id="eb394-142">제거-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="eb394-142">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="eb394-143">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="eb394-143">Get-AzureRmSqlSyncAgent</span></span>](./Get-AzureRmSqlSyncAgent.md)


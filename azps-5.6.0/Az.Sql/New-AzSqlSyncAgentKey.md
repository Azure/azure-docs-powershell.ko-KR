---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: 35942c51aa383dbc7dcbe071083eee575228372a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957995"
---
# <span data-ttu-id="d3828-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="d3828-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="d3828-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3828-102">SYNOPSIS</span></span>
<span data-ttu-id="d3828-103">Azure SQL 동기화 에이전트 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3828-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="d3828-104">구문</span><span class="sxs-lookup"><span data-stu-id="d3828-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3828-105">설명</span><span class="sxs-lookup"><span data-stu-id="d3828-105">DESCRIPTION</span></span>
<span data-ttu-id="d3828-106">**New-AzSqlSyncAgentKey** cmdlet은 Azure SQL 동기화 에이전트 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3828-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="d3828-107">예제</span><span class="sxs-lookup"><span data-stu-id="d3828-107">EXAMPLES</span></span>

### <span data-ttu-id="d3828-108">예제 1: Azure 동기화 에이전트에 대한 동기화 에이전트 키를 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3828-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="d3828-109">이 명령은 Azure 동기화 에이전트에 대한 동기화 SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3828-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="d3828-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d3828-110">PARAMETERS</span></span>

### <span data-ttu-id="d3828-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3828-111">-DefaultProfile</span></span>
<span data-ttu-id="d3828-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d3828-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3828-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3828-113">-ResourceGroupName</span></span>
<span data-ttu-id="d3828-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3828-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="d3828-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d3828-115">-ServerName</span></span>
<span data-ttu-id="d3828-116">동기화 에이전트가 SQL Server Azure 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3828-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="d3828-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="d3828-117">-SyncAgentName</span></span>
<span data-ttu-id="d3828-118">동기화 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3828-118">The sync agent name.</span></span>

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

### <span data-ttu-id="d3828-119">-확인</span><span class="sxs-lookup"><span data-stu-id="d3828-119">-Confirm</span></span>
<span data-ttu-id="d3828-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3828-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3828-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3828-121">-WhatIf</span></span>
<span data-ttu-id="d3828-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d3828-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3828-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3828-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3828-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3828-124">CommonParameters</span></span>
<span data-ttu-id="d3828-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d3828-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3828-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3828-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3828-127">입력</span><span class="sxs-lookup"><span data-stu-id="d3828-127">INPUTS</span></span>

### <span data-ttu-id="d3828-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d3828-128">System.String</span></span>

## <span data-ttu-id="d3828-129">출력</span><span class="sxs-lookup"><span data-stu-id="d3828-129">OUTPUTS</span></span>

### <span data-ttu-id="d3828-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="d3828-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="d3828-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d3828-131">NOTES</span></span>

## <span data-ttu-id="d3828-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3828-132">RELATED LINKS</span></span>

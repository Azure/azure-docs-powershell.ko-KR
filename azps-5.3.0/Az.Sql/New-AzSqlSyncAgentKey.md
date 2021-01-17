---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: e6ccf84d2de6c64000a6663de5a5b696d9033eae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491580"
---
# <span data-ttu-id="4014e-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="4014e-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="4014e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4014e-102">SYNOPSIS</span></span>
<span data-ttu-id="4014e-103">Azure SQL 동기화 에이전트 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4014e-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="4014e-104">구문</span><span class="sxs-lookup"><span data-stu-id="4014e-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4014e-105">설명</span><span class="sxs-lookup"><span data-stu-id="4014e-105">DESCRIPTION</span></span>
<span data-ttu-id="4014e-106">**New-AzSqlSyncAgentKey** cmdlet은 Azure SQL 동기화 에이전트 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4014e-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="4014e-107">예제</span><span class="sxs-lookup"><span data-stu-id="4014e-107">EXAMPLES</span></span>

### <span data-ttu-id="4014e-108">예제 1: Azure SQL 동기화 에이전트 키 만들기</span><span class="sxs-lookup"><span data-stu-id="4014e-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="4014e-109">이 명령은 Azure SQL 동기화 에이전트 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4014e-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="4014e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4014e-110">PARAMETERS</span></span>

### <span data-ttu-id="4014e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4014e-111">-DefaultProfile</span></span>
<span data-ttu-id="4014e-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4014e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4014e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4014e-113">-ResourceGroupName</span></span>
<span data-ttu-id="4014e-114">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4014e-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="4014e-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4014e-115">-ServerName</span></span>
<span data-ttu-id="4014e-116">동기화 에이전트가 SQL Server Azure 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4014e-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="4014e-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="4014e-117">-SyncAgentName</span></span>
<span data-ttu-id="4014e-118">동기화 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4014e-118">The sync agent name.</span></span>

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

### <span data-ttu-id="4014e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4014e-119">-Confirm</span></span>
<span data-ttu-id="4014e-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4014e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4014e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4014e-121">-WhatIf</span></span>
<span data-ttu-id="4014e-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4014e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4014e-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4014e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4014e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4014e-124">CommonParameters</span></span>
<span data-ttu-id="4014e-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4014e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4014e-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4014e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4014e-127">입력</span><span class="sxs-lookup"><span data-stu-id="4014e-127">INPUTS</span></span>

### <span data-ttu-id="4014e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4014e-128">System.String</span></span>

## <span data-ttu-id="4014e-129">출력</span><span class="sxs-lookup"><span data-stu-id="4014e-129">OUTPUTS</span></span>

### <span data-ttu-id="4014e-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="4014e-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="4014e-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4014e-131">NOTES</span></span>

## <span data-ttu-id="4014e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4014e-132">RELATED LINKS</span></span>

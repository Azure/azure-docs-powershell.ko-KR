---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: ca3ef83fab80e73d687fd11cde418c9ad43f499e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322685"
---
# <span data-ttu-id="260d7-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="260d7-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="260d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="260d7-102">SYNOPSIS</span></span>
<span data-ttu-id="260d7-103">Azure SQL 동기화 에이전트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="260d7-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="260d7-104">구문</span><span class="sxs-lookup"><span data-stu-id="260d7-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="260d7-105">설명</span><span class="sxs-lookup"><span data-stu-id="260d7-105">DESCRIPTION</span></span>
<span data-ttu-id="260d7-106">**Remove-AzSqlSyncAgent** cmdlet은 Azure SQL 동기화 에이전트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="260d7-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="260d7-107">예제</span><span class="sxs-lookup"><span data-stu-id="260d7-107">EXAMPLES</span></span>

### <span data-ttu-id="260d7-108">예제 1: 동기화 에이전트 제거</span><span class="sxs-lookup"><span data-stu-id="260d7-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="260d7-109">이 명령은 syncAgent01이라는 Azure SQL 동기화 에이전트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="260d7-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="260d7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="260d7-110">PARAMETERS</span></span>

### <span data-ttu-id="260d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="260d7-111">-DefaultProfile</span></span>
<span data-ttu-id="260d7-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="260d7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="260d7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="260d7-113">-Force</span></span>
<span data-ttu-id="260d7-114">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="260d7-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="260d7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="260d7-115">-Name</span></span>
<span data-ttu-id="260d7-116">동기화 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="260d7-116">The sync agent name.</span></span>

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

### <span data-ttu-id="260d7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="260d7-117">-PassThru</span></span>
<span data-ttu-id="260d7-118">제거된 동기화 에이전트를 반환할지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="260d7-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="260d7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="260d7-119">-ResourceGroupName</span></span>
<span data-ttu-id="260d7-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="260d7-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="260d7-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="260d7-121">-ServerName</span></span>
<span data-ttu-id="260d7-122">동기화 에이전트가 SQL Server Azure 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="260d7-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="260d7-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="260d7-123">-Confirm</span></span>
<span data-ttu-id="260d7-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="260d7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="260d7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="260d7-125">-WhatIf</span></span>
<span data-ttu-id="260d7-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="260d7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="260d7-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="260d7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="260d7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="260d7-128">CommonParameters</span></span>
<span data-ttu-id="260d7-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="260d7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="260d7-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="260d7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="260d7-131">입력</span><span class="sxs-lookup"><span data-stu-id="260d7-131">INPUTS</span></span>

### <span data-ttu-id="260d7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="260d7-132">System.String</span></span>

## <span data-ttu-id="260d7-133">출력</span><span class="sxs-lookup"><span data-stu-id="260d7-133">OUTPUTS</span></span>

### <span data-ttu-id="260d7-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="260d7-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="260d7-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="260d7-135">NOTES</span></span>

## <span data-ttu-id="260d7-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="260d7-136">RELATED LINKS</span></span>

[<span data-ttu-id="260d7-137">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="260d7-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="260d7-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="260d7-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)


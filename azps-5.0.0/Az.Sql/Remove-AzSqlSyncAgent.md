---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncAgent.md
ms.openlocfilehash: ca3ef83fab80e73d687fd11cde418c9ad43f499e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216980"
---
# <span data-ttu-id="40129-101">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="40129-101">Remove-AzSqlSyncAgent</span></span>

## <span data-ttu-id="40129-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40129-102">SYNOPSIS</span></span>
<span data-ttu-id="40129-103">Azure SQL 동기화 에이전트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="40129-103">Removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="40129-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40129-104">SYNTAX</span></span>

```
Remove-AzSqlSyncAgent [-Name] <String> [-Force] [-PassThru] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40129-105">설명은</span><span class="sxs-lookup"><span data-stu-id="40129-105">DESCRIPTION</span></span>
<span data-ttu-id="40129-106">**AzSqlSyncAgent** Cmdlet은 Azure SQL 동기화 에이전트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="40129-106">The **Remove-AzSqlSyncAgent** cmdlet removes an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="40129-107">예제의</span><span class="sxs-lookup"><span data-stu-id="40129-107">EXAMPLES</span></span>

### <span data-ttu-id="40129-108">예제 1: 동기화 에이전트 제거</span><span class="sxs-lookup"><span data-stu-id="40129-108">Example 1: Remove a sync agent</span></span>
```
PS C:\>Remove-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "syncAgent01"
```

<span data-ttu-id="40129-109">이 명령은 syncAgent01 이라는 Azure SQL 동기화 에이전트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="40129-109">This command removes the Azure SQL Sync Agent named syncAgent01.</span></span>

## <span data-ttu-id="40129-110">변수</span><span class="sxs-lookup"><span data-stu-id="40129-110">PARAMETERS</span></span>

### <span data-ttu-id="40129-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40129-111">-DefaultProfile</span></span>
<span data-ttu-id="40129-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="40129-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40129-113">-Force</span><span class="sxs-lookup"><span data-stu-id="40129-113">-Force</span></span>
<span data-ttu-id="40129-114">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="40129-114">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="40129-115">-이름</span><span class="sxs-lookup"><span data-stu-id="40129-115">-Name</span></span>
<span data-ttu-id="40129-116">동기화 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40129-116">The sync agent name.</span></span>

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

### <span data-ttu-id="40129-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40129-117">-PassThru</span></span>
<span data-ttu-id="40129-118">제거 된 동기화 에이전트를 반환할지 여부를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="40129-118">Defines Whether return the removed sync agent</span></span>

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

### <span data-ttu-id="40129-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40129-119">-ResourceGroupName</span></span>
<span data-ttu-id="40129-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40129-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="40129-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="40129-121">-ServerName</span></span>
<span data-ttu-id="40129-122">동기화 에이전트가 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40129-122">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="40129-123">-확인</span><span class="sxs-lookup"><span data-stu-id="40129-123">-Confirm</span></span>
<span data-ttu-id="40129-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="40129-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40129-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40129-125">-WhatIf</span></span>
<span data-ttu-id="40129-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="40129-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40129-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40129-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40129-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40129-128">CommonParameters</span></span>
<span data-ttu-id="40129-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40129-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40129-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="40129-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40129-131">입력</span><span class="sxs-lookup"><span data-stu-id="40129-131">INPUTS</span></span>

### <span data-ttu-id="40129-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="40129-132">System.String</span></span>

## <span data-ttu-id="40129-133">출력</span><span class="sxs-lookup"><span data-stu-id="40129-133">OUTPUTS</span></span>

### <span data-ttu-id="40129-134">AzureSqlSyncAgentModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="40129-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="40129-135">상속자</span><span class="sxs-lookup"><span data-stu-id="40129-135">NOTES</span></span>

## <span data-ttu-id="40129-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40129-136">RELATED LINKS</span></span>

[<span data-ttu-id="40129-137">새로운 AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="40129-137">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

[<span data-ttu-id="40129-138">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="40129-138">Get-AzSqlSyncAgent</span></span>](./Get-AzSqlSyncAgent.md)


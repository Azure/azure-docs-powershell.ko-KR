---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: d611f0bc14d657f47881cbdfbb1326111873114a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489531"
---
# <span data-ttu-id="f3af8-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="f3af8-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="f3af8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3af8-102">SYNOPSIS</span></span>
<span data-ttu-id="f3af8-103">Azure SQL Server DNS 별칭을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f3af8-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="f3af8-104">구문</span><span class="sxs-lookup"><span data-stu-id="f3af8-104">SYNTAX</span></span>

### <span data-ttu-id="f3af8-105">cmdlet 입력 매개 변수에서 서버 Dns 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="f3af8-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3af8-106">AzureSqlServerDnsAliasModel 인스턴스 정의에서 서버 Dns 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="f3af8-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3af8-107">Azure 리소스 ID에서 서버 Dns 별칭 제거</span><span class="sxs-lookup"><span data-stu-id="f3af8-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3af8-108">설명</span><span class="sxs-lookup"><span data-stu-id="f3af8-108">DESCRIPTION</span></span>
<span data-ttu-id="f3af8-109">이 명령은 서버에서 Azure SQL Server DNS 별칭을 제거하여 서버를 그대로 떠났습니다.</span><span class="sxs-lookup"><span data-stu-id="f3af8-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="f3af8-110">예제</span><span class="sxs-lookup"><span data-stu-id="f3af8-110">EXAMPLES</span></span>

### <span data-ttu-id="f3af8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f3af8-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="f3af8-112">serverName이 SQL Server aliasName 이름의 Azure SQL Server DNS 별칭을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f3af8-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="f3af8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3af8-113">PARAMETERS</span></span>

### <span data-ttu-id="f3af8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3af8-114">-AsJob</span></span>
<span data-ttu-id="f3af8-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f3af8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3af8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3af8-116">-DefaultProfile</span></span>
<span data-ttu-id="f3af8-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3af8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3af8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f3af8-118">-Force</span></span>
<span data-ttu-id="f3af8-119">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="f3af8-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="f3af8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3af8-120">-InputObject</span></span>
<span data-ttu-id="f3af8-121">제거할 서버 Dns 별칭 개체</span><span class="sxs-lookup"><span data-stu-id="f3af8-121">The Server Dns Alias object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel
Parameter Sets: Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3af8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f3af8-122">-Name</span></span>
<span data-ttu-id="f3af8-123">Azure Sql Server Dns 별칭 이름</span><span class="sxs-lookup"><span data-stu-id="f3af8-123">Azure Sql Server Dns Alias name</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3af8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3af8-124">-ResourceGroupName</span></span>
<span data-ttu-id="f3af8-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3af8-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3af8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3af8-126">-ResourceId</span></span>
<span data-ttu-id="f3af8-127">제거할 서버 Dns 별칭 개체의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="f3af8-127">The resource id of Server Dns Alias object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from an Azure resource id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3af8-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f3af8-128">-ServerName</span></span>
<span data-ttu-id="f3af8-129">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3af8-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3af8-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3af8-130">-Confirm</span></span>
<span data-ttu-id="f3af8-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3af8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3af8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3af8-132">-WhatIf</span></span>
<span data-ttu-id="f3af8-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f3af8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3af8-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3af8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3af8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3af8-135">CommonParameters</span></span>
<span data-ttu-id="f3af8-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f3af8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3af8-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f3af8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3af8-138">입력</span><span class="sxs-lookup"><span data-stu-id="f3af8-138">INPUTS</span></span>

### <span data-ttu-id="f3af8-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="f3af8-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="f3af8-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f3af8-140">System.String</span></span>

## <span data-ttu-id="f3af8-141">출력</span><span class="sxs-lookup"><span data-stu-id="f3af8-141">OUTPUTS</span></span>

### <span data-ttu-id="f3af8-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="f3af8-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="f3af8-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f3af8-143">NOTES</span></span>

## <span data-ttu-id="f3af8-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3af8-144">RELATED LINKS</span></span>

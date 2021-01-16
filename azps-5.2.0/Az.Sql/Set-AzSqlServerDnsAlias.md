---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: 791658e9f4f10fdbb8b1000d6b1bc88d392aaf46
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343965"
---
# <span data-ttu-id="10bcd-101">Set-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="10bcd-101">Set-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="10bcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10bcd-102">SYNOPSIS</span></span>
<span data-ttu-id="10bcd-103">Azure 및 DNS 별칭이 SQL Server 서버를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="10bcd-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

## <span data-ttu-id="10bcd-104">구문</span><span class="sxs-lookup"><span data-stu-id="10bcd-104">SYNTAX</span></span>

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10bcd-105">설명</span><span class="sxs-lookup"><span data-stu-id="10bcd-105">DESCRIPTION</span></span>
<span data-ttu-id="10bcd-106">이 명령은 별칭이 포인터가 있는 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="10bcd-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="10bcd-107">별칭이 지점이 될 새 서버가 있는 구독에 로그인하는 동안 이 명령을 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="10bcd-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="10bcd-108">예제</span><span class="sxs-lookup"><span data-stu-id="10bcd-108">EXAMPLES</span></span>

### <span data-ttu-id="10bcd-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="10bcd-109">Example 1</span></span>
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="10bcd-110">이 명령은 이전에 oldServer를 통해 서버 newServer를 지점으로 하는 별칭을 업데이트하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10bcd-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="10bcd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10bcd-111">PARAMETERS</span></span>

### <span data-ttu-id="10bcd-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10bcd-112">-AsJob</span></span>
<span data-ttu-id="10bcd-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="10bcd-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10bcd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10bcd-114">-DefaultProfile</span></span>
<span data-ttu-id="10bcd-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10bcd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10bcd-116">-Name</span><span class="sxs-lookup"><span data-stu-id="10bcd-116">-Name</span></span>
<span data-ttu-id="10bcd-117">Azure Sql Server Dns 별칭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10bcd-117">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10bcd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10bcd-118">-ResourceGroupName</span></span>
<span data-ttu-id="10bcd-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10bcd-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10bcd-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="10bcd-120">-SourceServerName</span></span>
<span data-ttu-id="10bcd-121">현재 별칭이 지정되는 Azure Sql Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10bcd-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10bcd-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10bcd-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="10bcd-123">원본 서버의 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10bcd-123">The name of resource group of the source server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10bcd-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10bcd-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="10bcd-125">원본 서버의 구독 ID</span><span class="sxs-lookup"><span data-stu-id="10bcd-125">The subscription id of the source server</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10bcd-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="10bcd-126">-TargetServerName</span></span>
<span data-ttu-id="10bcd-127">별칭이 지정해야 하는 Azure Sql Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10bcd-127">The name of Azure Sql Server to which alias should point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10bcd-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10bcd-128">-Confirm</span></span>
<span data-ttu-id="10bcd-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="10bcd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10bcd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10bcd-130">-WhatIf</span></span>
<span data-ttu-id="10bcd-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="10bcd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10bcd-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10bcd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10bcd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10bcd-133">CommonParameters</span></span>
<span data-ttu-id="10bcd-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="10bcd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10bcd-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="10bcd-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10bcd-136">입력</span><span class="sxs-lookup"><span data-stu-id="10bcd-136">INPUTS</span></span>

### <span data-ttu-id="10bcd-137">System.String</span><span class="sxs-lookup"><span data-stu-id="10bcd-137">System.String</span></span>

## <span data-ttu-id="10bcd-138">출력</span><span class="sxs-lookup"><span data-stu-id="10bcd-138">OUTPUTS</span></span>

### <span data-ttu-id="10bcd-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="10bcd-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="10bcd-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="10bcd-140">NOTES</span></span>

## <span data-ttu-id="10bcd-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10bcd-141">RELATED LINKS</span></span>

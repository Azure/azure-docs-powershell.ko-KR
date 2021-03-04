---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 46a3476d5ae4cead17eba0d03412ad2db57b01a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955211"
---
# <span data-ttu-id="66c0e-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="66c0e-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="66c0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="66c0e-103">이 명령은 새 Azure SQL Server DNS 별칭을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66c0e-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="66c0e-104">구문</span><span class="sxs-lookup"><span data-stu-id="66c0e-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66c0e-105">설명</span><span class="sxs-lookup"><span data-stu-id="66c0e-105">DESCRIPTION</span></span>
<span data-ttu-id="66c0e-106">지정된 서버를 SQL Server DNS 별칭을 새로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66c0e-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="66c0e-107">예제</span><span class="sxs-lookup"><span data-stu-id="66c0e-107">EXAMPLES</span></span>

### <span data-ttu-id="66c0e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="66c0e-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="66c0e-109">이 명령은 서버 서버를 SQL Server 별칭으로 Azure SQL Server DNS 별칭을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="66c0e-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="66c0e-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="66c0e-110">PARAMETERS</span></span>

### <span data-ttu-id="66c0e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66c0e-111">-AsJob</span></span>
<span data-ttu-id="66c0e-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="66c0e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66c0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c0e-113">-DefaultProfile</span></span>
<span data-ttu-id="66c0e-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66c0e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66c0e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="66c0e-115">-Name</span></span>
<span data-ttu-id="66c0e-116">Azure Sql Server Dns 별칭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66c0e-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c0e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66c0e-117">-ResourceGroupName</span></span>
<span data-ttu-id="66c0e-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66c0e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="66c0e-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="66c0e-119">-ServerName</span></span>
<span data-ttu-id="66c0e-120">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66c0e-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="66c0e-121">-확인</span><span class="sxs-lookup"><span data-stu-id="66c0e-121">-Confirm</span></span>
<span data-ttu-id="66c0e-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="66c0e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66c0e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66c0e-123">-WhatIf</span></span>
<span data-ttu-id="66c0e-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="66c0e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66c0e-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66c0e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66c0e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c0e-126">CommonParameters</span></span>
<span data-ttu-id="66c0e-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66c0e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c0e-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66c0e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c0e-129">입력</span><span class="sxs-lookup"><span data-stu-id="66c0e-129">INPUTS</span></span>

### <span data-ttu-id="66c0e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="66c0e-130">System.String</span></span>

## <span data-ttu-id="66c0e-131">출력</span><span class="sxs-lookup"><span data-stu-id="66c0e-131">OUTPUTS</span></span>

### <span data-ttu-id="66c0e-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="66c0e-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="66c0e-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66c0e-133">NOTES</span></span>

## <span data-ttu-id="66c0e-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66c0e-134">RELATED LINKS</span></span>

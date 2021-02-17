---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 417bab5679da4607cc42468fc4620cf392323919
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188084"
---
# <span data-ttu-id="c9daa-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="c9daa-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="c9daa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9daa-102">SYNOPSIS</span></span>
<span data-ttu-id="c9daa-103">Azure 및 DNS 별칭을 SQL Server 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c9daa-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="c9daa-104">구문</span><span class="sxs-lookup"><span data-stu-id="c9daa-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9daa-105">설명</span><span class="sxs-lookup"><span data-stu-id="c9daa-105">DESCRIPTION</span></span>
<span data-ttu-id="c9daa-106">특정 Azure SQL Server DNS 별칭을 얻거나 서버에 대한 모든 서버 DNS 별칭을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c9daa-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="c9daa-107">예제</span><span class="sxs-lookup"><span data-stu-id="c9daa-107">EXAMPLES</span></span>

### <span data-ttu-id="c9daa-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c9daa-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="c9daa-109">특정 서버에 대한 모든 서버 DNS 별칭을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c9daa-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="c9daa-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="c9daa-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="c9daa-111">서버 및 별칭 이름으로 지정된 서버 DNS 별칭을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9daa-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="c9daa-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="c9daa-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="c9daa-113">"dnsaliasname"으로 시작하는 특정 서버에 대한 모든 서버 DNS 별칭을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c9daa-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="c9daa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9daa-114">PARAMETERS</span></span>

### <span data-ttu-id="c9daa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9daa-115">-DefaultProfile</span></span>
<span data-ttu-id="c9daa-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9daa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9daa-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c9daa-117">-Name</span></span>
<span data-ttu-id="c9daa-118">Azure Sql Server DNS 별칭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9daa-118">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9daa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9daa-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9daa-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9daa-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="c9daa-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c9daa-121">-ServerName</span></span>
<span data-ttu-id="c9daa-122">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9daa-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c9daa-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9daa-123">-Confirm</span></span>
<span data-ttu-id="c9daa-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9daa-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9daa-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9daa-125">-WhatIf</span></span>
<span data-ttu-id="c9daa-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c9daa-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9daa-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9daa-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9daa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9daa-128">CommonParameters</span></span>
<span data-ttu-id="c9daa-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9daa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9daa-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c9daa-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9daa-131">입력</span><span class="sxs-lookup"><span data-stu-id="c9daa-131">INPUTS</span></span>

### <span data-ttu-id="c9daa-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c9daa-132">System.String</span></span>

## <span data-ttu-id="c9daa-133">출력</span><span class="sxs-lookup"><span data-stu-id="c9daa-133">OUTPUTS</span></span>

### <span data-ttu-id="c9daa-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="c9daa-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="c9daa-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c9daa-135">NOTES</span></span>

## <span data-ttu-id="c9daa-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9daa-136">RELATED LINKS</span></span>

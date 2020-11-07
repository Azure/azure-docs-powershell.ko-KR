---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 60790af3396177e2885b4a83fda4d24db8c4e4d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873873"
---
# <span data-ttu-id="33490-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="33490-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="33490-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33490-102">SYNOPSIS</span></span>
<span data-ttu-id="33490-103">이 명령은 새 Azure SQL Server DNS 별칭을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="33490-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="33490-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33490-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33490-105">설명은</span><span class="sxs-lookup"><span data-stu-id="33490-105">DESCRIPTION</span></span>
<span data-ttu-id="33490-106">지정 된 서버를 가리키는 새 Azure SQL Server DNS 별칭을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="33490-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="33490-107">예제의</span><span class="sxs-lookup"><span data-stu-id="33490-107">EXAMPLES</span></span>

### <span data-ttu-id="33490-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="33490-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="33490-109">이 명령은 서버 serverName을 가리키는 이름 aliasName를 사용 하 여 Azure SQL Server DNS 별칭을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="33490-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="33490-110">변수</span><span class="sxs-lookup"><span data-stu-id="33490-110">PARAMETERS</span></span>

### <span data-ttu-id="33490-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33490-111">-AsJob</span></span>
<span data-ttu-id="33490-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="33490-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33490-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33490-113">-DefaultProfile</span></span>
<span data-ttu-id="33490-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33490-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33490-115">-이름</span><span class="sxs-lookup"><span data-stu-id="33490-115">-Name</span></span>
<span data-ttu-id="33490-116">Azure Sql Server Dns 별칭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33490-116">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="33490-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33490-117">-ResourceGroupName</span></span>
<span data-ttu-id="33490-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33490-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="33490-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="33490-119">-ServerName</span></span>
<span data-ttu-id="33490-120">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33490-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="33490-121">-확인</span><span class="sxs-lookup"><span data-stu-id="33490-121">-Confirm</span></span>
<span data-ttu-id="33490-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="33490-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33490-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33490-123">-WhatIf</span></span>
<span data-ttu-id="33490-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="33490-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33490-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33490-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33490-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33490-126">CommonParameters</span></span>
<span data-ttu-id="33490-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33490-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33490-128">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="33490-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33490-129">입력</span><span class="sxs-lookup"><span data-stu-id="33490-129">INPUTS</span></span>

### <span data-ttu-id="33490-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="33490-130">System.String</span></span>

## <span data-ttu-id="33490-131">출력</span><span class="sxs-lookup"><span data-stu-id="33490-131">OUTPUTS</span></span>

### <span data-ttu-id="33490-132">Microsoft. ServerDnsAlias. AzureSqlServerDnsAliasModel.</span><span class="sxs-lookup"><span data-stu-id="33490-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="33490-133">상속자</span><span class="sxs-lookup"><span data-stu-id="33490-133">NOTES</span></span>

## <span data-ttu-id="33490-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33490-134">RELATED LINKS</span></span>

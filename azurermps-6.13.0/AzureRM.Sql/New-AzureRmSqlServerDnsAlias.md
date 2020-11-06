---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 3ce18369645705f78722f7505c8dd1e46f2514b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525999"
---
# <span data-ttu-id="58b25-101">New-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="58b25-101">New-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="58b25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58b25-102">SYNOPSIS</span></span>
<span data-ttu-id="58b25-103">이 명령은 새 Azure SQL Server DNS 별칭을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="58b25-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58b25-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58b25-104">SYNTAX</span></span>

```
New-AzureRmSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58b25-105">설명은</span><span class="sxs-lookup"><span data-stu-id="58b25-105">DESCRIPTION</span></span>
<span data-ttu-id="58b25-106">지정 된 서버를 가리키는 새 Azure SQL Server DNS 별칭을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="58b25-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="58b25-107">예제의</span><span class="sxs-lookup"><span data-stu-id="58b25-107">EXAMPLES</span></span>

### <span data-ttu-id="58b25-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="58b25-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzureRmSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="58b25-109">이 명령은 서버 serverName을 가리키는 이름 aliasName를 사용 하 여 Azure SQL Server DNS 별칭을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="58b25-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="58b25-110">변수</span><span class="sxs-lookup"><span data-stu-id="58b25-110">PARAMETERS</span></span>

### <span data-ttu-id="58b25-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58b25-111">-AsJob</span></span>
<span data-ttu-id="58b25-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="58b25-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58b25-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b25-113">-DefaultProfile</span></span>
<span data-ttu-id="58b25-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58b25-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58b25-115">-이름</span><span class="sxs-lookup"><span data-stu-id="58b25-115">-Name</span></span>
<span data-ttu-id="58b25-116">Azure Sql Server Dns 별칭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58b25-116">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="58b25-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58b25-117">-ResourceGroupName</span></span>
<span data-ttu-id="58b25-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58b25-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="58b25-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="58b25-119">-ServerName</span></span>
<span data-ttu-id="58b25-120">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58b25-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="58b25-121">-확인</span><span class="sxs-lookup"><span data-stu-id="58b25-121">-Confirm</span></span>
<span data-ttu-id="58b25-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b25-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58b25-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58b25-123">-WhatIf</span></span>
<span data-ttu-id="58b25-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="58b25-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58b25-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58b25-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58b25-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b25-126">CommonParameters</span></span>
<span data-ttu-id="58b25-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58b25-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b25-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58b25-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b25-129">입력</span><span class="sxs-lookup"><span data-stu-id="58b25-129">INPUTS</span></span>

### <span data-ttu-id="58b25-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="58b25-130">System.String</span></span>

## <span data-ttu-id="58b25-131">출력</span><span class="sxs-lookup"><span data-stu-id="58b25-131">OUTPUTS</span></span>

### <span data-ttu-id="58b25-132">Microsoft. ServerDnsAlias. AzureSqlServerDnsAliasModel.</span><span class="sxs-lookup"><span data-stu-id="58b25-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="58b25-133">상속자</span><span class="sxs-lookup"><span data-stu-id="58b25-133">NOTES</span></span>

## <span data-ttu-id="58b25-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58b25-134">RELATED LINKS</span></span>

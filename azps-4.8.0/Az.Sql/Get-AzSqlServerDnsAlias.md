---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDnsAlias.md
ms.openlocfilehash: 417bab5679da4607cc42468fc4620cf392323919
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204285"
---
# <span data-ttu-id="364c2-101">Get-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="364c2-101">Get-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="364c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="364c2-102">SYNOPSIS</span></span>
<span data-ttu-id="364c2-103">Azure SQL Server DNS 별칭을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="364c2-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="364c2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="364c2-104">SYNTAX</span></span>

```
Get-AzSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="364c2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="364c2-105">DESCRIPTION</span></span>
<span data-ttu-id="364c2-106">특정 Azure SQL Server DNS 별칭을 가져오거나 서버에 대 한 모든 서버 DNS 별칭을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="364c2-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="364c2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="364c2-107">EXAMPLES</span></span>

### <span data-ttu-id="364c2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="364c2-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="364c2-109">특정 서버에 대 한 모든 서버 DNS 별칭을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="364c2-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="364c2-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="364c2-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="364c2-111">서버 및 별칭 이름으로 지정 된 서버 DNS 별칭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="364c2-111">Gets Server DNS Alias specified by server and alias name</span></span>

### <span data-ttu-id="364c2-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="364c2-112">Example 3</span></span>
```
PS C:\> $serverDNSAliases = Get-AzSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname -DnsAliasName "dnsaliasname*"

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="364c2-113">"Dnsaliasname"로 시작 하는 특정 서버에 대 한 모든 서버 DNS 별칭을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="364c2-113">Lists all Server DNS Aliases for the specific server that start with "dnsaliasname".</span></span>

## <span data-ttu-id="364c2-114">변수</span><span class="sxs-lookup"><span data-stu-id="364c2-114">PARAMETERS</span></span>

### <span data-ttu-id="364c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="364c2-115">-DefaultProfile</span></span>
<span data-ttu-id="364c2-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="364c2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="364c2-117">-이름</span><span class="sxs-lookup"><span data-stu-id="364c2-117">-Name</span></span>
<span data-ttu-id="364c2-118">Azure Sql Server DNS 별칭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="364c2-118">The Azure Sql Server DNS Alias name.</span></span>

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

### <span data-ttu-id="364c2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="364c2-119">-ResourceGroupName</span></span>
<span data-ttu-id="364c2-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="364c2-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="364c2-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="364c2-121">-ServerName</span></span>
<span data-ttu-id="364c2-122">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="364c2-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="364c2-123">-확인</span><span class="sxs-lookup"><span data-stu-id="364c2-123">-Confirm</span></span>
<span data-ttu-id="364c2-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="364c2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="364c2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="364c2-125">-WhatIf</span></span>
<span data-ttu-id="364c2-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="364c2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="364c2-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="364c2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="364c2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="364c2-128">CommonParameters</span></span>
<span data-ttu-id="364c2-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="364c2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="364c2-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="364c2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="364c2-131">입력</span><span class="sxs-lookup"><span data-stu-id="364c2-131">INPUTS</span></span>

### <span data-ttu-id="364c2-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="364c2-132">System.String</span></span>

## <span data-ttu-id="364c2-133">출력</span><span class="sxs-lookup"><span data-stu-id="364c2-133">OUTPUTS</span></span>

### <span data-ttu-id="364c2-134">Microsoft. ServerDnsAlias. AzureSqlServerDnsAliasModel.</span><span class="sxs-lookup"><span data-stu-id="364c2-134">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="364c2-135">상속자</span><span class="sxs-lookup"><span data-stu-id="364c2-135">NOTES</span></span>

## <span data-ttu-id="364c2-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="364c2-136">RELATED LINKS</span></span>

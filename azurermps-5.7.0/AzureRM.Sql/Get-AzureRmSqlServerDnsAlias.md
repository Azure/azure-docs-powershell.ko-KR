---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 4a2b7de83036e274b9d53b701615e3c348c5f4df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524843"
---
# <span data-ttu-id="f751b-101">Get-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="f751b-101">Get-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="f751b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f751b-102">SYNOPSIS</span></span>
<span data-ttu-id="f751b-103">Azure SQL Server DNS 별칭을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f751b-103">Gets or lists Azure SQL Server DNS Alias.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f751b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f751b-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDnsAlias [-Name <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f751b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f751b-105">DESCRIPTION</span></span>
<span data-ttu-id="f751b-106">특정 Azure SQL Server DNS 별칭을 가져오거나 서버에 대 한 모든 서버 DNS 별칭을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f751b-106">Get the specific Azure SQL Server DNS Alias or lists all Server DNS Aliases for the server</span></span>

## <span data-ttu-id="f751b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f751b-107">EXAMPLES</span></span>

### <span data-ttu-id="f751b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f751b-108">Example 1</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
rgname             servername   dnsaliasname2
```

<span data-ttu-id="f751b-109">특정 서버에 대 한 모든 서버 DNS 별칭을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f751b-109">Lists all Server DNS Aliases for the specific server</span></span>

### <span data-ttu-id="f751b-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="f751b-110">Example 2</span></span>
```
PS C:\> $serverDNSAliases = Get-AzureRmSqlServerDNSAlias -DnsAliasName dnsaliasname -ServerName servername -ResourceGroupName rgname

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="f751b-111">서버 및 별칭 이름으로 지정 된 서버 DNS 별칭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f751b-111">Gets Server DNS Alias specified by server and alias name</span></span>

## <span data-ttu-id="f751b-112">변수</span><span class="sxs-lookup"><span data-stu-id="f751b-112">PARAMETERS</span></span>

### <span data-ttu-id="f751b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f751b-113">-DefaultProfile</span></span>
<span data-ttu-id="f751b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f751b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f751b-115">-이름</span><span class="sxs-lookup"><span data-stu-id="f751b-115">-Name</span></span>
<span data-ttu-id="f751b-116">Azure Sql Server DNS 별칭 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f751b-116">The Azure Sql Server DNS Alias name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f751b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f751b-117">-ResourceGroupName</span></span>
<span data-ttu-id="f751b-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f751b-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f751b-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f751b-119">-ServerName</span></span>
<span data-ttu-id="f751b-120">Azure Sql Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f751b-120">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f751b-121">-확인</span><span class="sxs-lookup"><span data-stu-id="f751b-121">-Confirm</span></span>
<span data-ttu-id="f751b-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f751b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f751b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f751b-123">-WhatIf</span></span>
<span data-ttu-id="f751b-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f751b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f751b-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f751b-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f751b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f751b-126">CommonParameters</span></span>
<span data-ttu-id="f751b-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f751b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f751b-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f751b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f751b-129">입력</span><span class="sxs-lookup"><span data-stu-id="f751b-129">INPUTS</span></span>

### <span data-ttu-id="f751b-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f751b-130">System.String</span></span>

## <span data-ttu-id="f751b-131">출력</span><span class="sxs-lookup"><span data-stu-id="f751b-131">OUTPUTS</span></span>

### <span data-ttu-id="f751b-132">Microsoft. ServerDnsAlias. AzureSqlServerDnsAliasModel.</span><span class="sxs-lookup"><span data-stu-id="f751b-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="f751b-133">상속자</span><span class="sxs-lookup"><span data-stu-id="f751b-133">NOTES</span></span>

## <span data-ttu-id="f751b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f751b-134">RELATED LINKS</span></span>

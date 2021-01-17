---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 282ef9f77f5902d698353528b10e154eb7fd86ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374669"
---
# <span data-ttu-id="facd2-101">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="facd2-101">New-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="facd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="facd2-102">SYNOPSIS</span></span>
<span data-ttu-id="facd2-103">두 데이터베이스 서버 간의 탄력적 데이터베이스 트랜잭션에 대한 SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="facd2-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

## <span data-ttu-id="facd2-104">구문</span><span class="sxs-lookup"><span data-stu-id="facd2-104">SYNTAX</span></span>

```
New-AzSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="facd2-105">설명</span><span class="sxs-lookup"><span data-stu-id="facd2-105">DESCRIPTION</span></span>
<span data-ttu-id="facd2-106">**New-AzSqlServerCommunicationLink** cmdlet은 Azure SQL Database의 두 논리 서버 간에 탄력적 데이터베이스 트랜잭션에 대한 통신 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="facd2-106">The **New-AzSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="facd2-107">탄력적 데이터베이스 트랜잭션은 쌍을 이을 서버 중 하나에 있는 데이터베이스에 걸쳐 있습니다.</span><span class="sxs-lookup"><span data-stu-id="facd2-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="facd2-108">서버에 링크를 두 개 이상 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="facd2-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="facd2-109">따라서 탄력적 데이터베이스 트랜잭션은 많은 수의 서버에 걸쳐 있습니다.</span><span class="sxs-lookup"><span data-stu-id="facd2-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="facd2-110">예제</span><span class="sxs-lookup"><span data-stu-id="facd2-110">EXAMPLES</span></span>

### <span data-ttu-id="facd2-111">예제 1: 통신 링크 만들기</span><span class="sxs-lookup"><span data-stu-id="facd2-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="facd2-112">이 명령은 ContosoServer17과 ContosoServer02 사이에 Link01이라는 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="facd2-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="facd2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="facd2-113">PARAMETERS</span></span>

### <span data-ttu-id="facd2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="facd2-114">-AsJob</span></span>
<span data-ttu-id="facd2-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="facd2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="facd2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="facd2-116">-DefaultProfile</span></span>
<span data-ttu-id="facd2-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="facd2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="facd2-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="facd2-118">-LinkName</span></span>
<span data-ttu-id="facd2-119">이 cmdlet에서 만드는 서버 통신 링크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="facd2-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="facd2-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="facd2-120">-PartnerServer</span></span>
<span data-ttu-id="facd2-121">이 통신 링크에 참여하는 다른 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="facd2-121">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="facd2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="facd2-122">-ResourceGroupName</span></span>
<span data-ttu-id="facd2-123">*ServerName* 매개 변수로 지정된 서버가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="facd2-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="facd2-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="facd2-124">-ServerName</span></span>
<span data-ttu-id="facd2-125">이 cmdlet이 통신 링크를 설정하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="facd2-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="facd2-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="facd2-126">-Confirm</span></span>
<span data-ttu-id="facd2-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="facd2-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="facd2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="facd2-128">-WhatIf</span></span>
<span data-ttu-id="facd2-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="facd2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="facd2-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="facd2-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="facd2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="facd2-131">CommonParameters</span></span>
<span data-ttu-id="facd2-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="facd2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="facd2-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="facd2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="facd2-134">입력</span><span class="sxs-lookup"><span data-stu-id="facd2-134">INPUTS</span></span>

### <span data-ttu-id="facd2-135">System.String</span><span class="sxs-lookup"><span data-stu-id="facd2-135">System.String</span></span>

## <span data-ttu-id="facd2-136">출력</span><span class="sxs-lookup"><span data-stu-id="facd2-136">OUTPUTS</span></span>

### <span data-ttu-id="facd2-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="facd2-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="facd2-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="facd2-138">NOTES</span></span>
* <span data-ttu-id="facd2-139">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, 데이터베이스, mssql</span><span class="sxs-lookup"><span data-stu-id="facd2-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="facd2-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="facd2-140">RELATED LINKS</span></span>

[<span data-ttu-id="facd2-141">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="facd2-141">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="facd2-142">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="facd2-142">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="facd2-143">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="facd2-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

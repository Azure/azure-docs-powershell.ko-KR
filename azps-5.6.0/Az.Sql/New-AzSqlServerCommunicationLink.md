---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 79d920f866991cae15e2da08d03e2eecd4d2e91e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969771"
---
# <span data-ttu-id="258cf-101">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="258cf-101">New-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="258cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="258cf-102">SYNOPSIS</span></span>
<span data-ttu-id="258cf-103">두 데이터베이스 서버 간에 탄력적 데이터베이스 트랜잭션에 대한 SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="258cf-103">Creates a communication link for elastic database transactions between two SQL Database servers.</span></span>

## <span data-ttu-id="258cf-104">구문</span><span class="sxs-lookup"><span data-stu-id="258cf-104">SYNTAX</span></span>

```
New-AzSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="258cf-105">설명</span><span class="sxs-lookup"><span data-stu-id="258cf-105">DESCRIPTION</span></span>
<span data-ttu-id="258cf-106">**New-AzSqlServerCommunicationLink** cmdlet은 Azure SQL 데이터베이스의 두 논리 서버 간에 탄력적 데이터베이스 트랜잭션에 대한 통신 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="258cf-106">The **New-AzSqlServerCommunicationLink** cmdlet creates a communication link for elastic database transactions between two logical servers in Azure SQL Database.</span></span>
<span data-ttu-id="258cf-107">탄력적 데이터베이스 트랜잭션은 페어링된 서버 중 하나에서 데이터베이스를 확장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="258cf-107">Elastic database transactions can span databases in either of the paired servers.</span></span>
<span data-ttu-id="258cf-108">서버에 두 개 이상의 링크를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="258cf-108">You can create more than one link on a server.</span></span>
<span data-ttu-id="258cf-109">따라서 탄력적 데이터베이스 트랜잭션은 더 많은 수의 서버에 걸쳐 분산될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="258cf-109">Therefore, elastic database transactions can span across a larger number of servers.</span></span>

## <span data-ttu-id="258cf-110">예제</span><span class="sxs-lookup"><span data-stu-id="258cf-110">EXAMPLES</span></span>

### <span data-ttu-id="258cf-111">예제 1: 통신 링크 만들기</span><span class="sxs-lookup"><span data-stu-id="258cf-111">Example 1: Create a communication link</span></span>
```
PS C:\>New-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

<span data-ttu-id="258cf-112">이 명령은 ContosoServer17과 ContosoServer02 사이에 Link01이라는 링크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="258cf-112">This command creates a link named Link01 between ContosoServer17 and ContosoServer02.</span></span>

## <span data-ttu-id="258cf-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="258cf-113">PARAMETERS</span></span>

### <span data-ttu-id="258cf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="258cf-114">-AsJob</span></span>
<span data-ttu-id="258cf-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="258cf-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="258cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="258cf-116">-DefaultProfile</span></span>
<span data-ttu-id="258cf-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="258cf-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="258cf-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="258cf-118">-LinkName</span></span>
<span data-ttu-id="258cf-119">이 cmdlet이 만드는 서버 통신 링크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="258cf-119">Specifies the name of the server communication link that this cmdlet creates.</span></span>

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

### <span data-ttu-id="258cf-120">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="258cf-120">-PartnerServer</span></span>
<span data-ttu-id="258cf-121">이 통신 링크에 참여하는 다른 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="258cf-121">Specifies the name of the other server that takes part in this communication link.</span></span>

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

### <span data-ttu-id="258cf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="258cf-122">-ResourceGroupName</span></span>
<span data-ttu-id="258cf-123">*ServerName* 매개 변수에 의해 지정된 서버가 속하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="258cf-123">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="258cf-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="258cf-124">-ServerName</span></span>
<span data-ttu-id="258cf-125">이 cmdlet에서 통신 링크를 설정하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="258cf-125">Specifies the name of the server on which this cmdlet sets up the communication link.</span></span>

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

### <span data-ttu-id="258cf-126">-확인</span><span class="sxs-lookup"><span data-stu-id="258cf-126">-Confirm</span></span>
<span data-ttu-id="258cf-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="258cf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="258cf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="258cf-128">-WhatIf</span></span>
<span data-ttu-id="258cf-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="258cf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="258cf-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="258cf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="258cf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="258cf-131">CommonParameters</span></span>
<span data-ttu-id="258cf-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="258cf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="258cf-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="258cf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="258cf-134">입력</span><span class="sxs-lookup"><span data-stu-id="258cf-134">INPUTS</span></span>

### <span data-ttu-id="258cf-135">System.String</span><span class="sxs-lookup"><span data-stu-id="258cf-135">System.String</span></span>

## <span data-ttu-id="258cf-136">출력</span><span class="sxs-lookup"><span data-stu-id="258cf-136">OUTPUTS</span></span>

### <span data-ttu-id="258cf-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="258cf-137">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="258cf-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="258cf-138">NOTES</span></span>
* <span data-ttu-id="258cf-139">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, 데이터베이스, mssql</span><span class="sxs-lookup"><span data-stu-id="258cf-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="258cf-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="258cf-140">RELATED LINKS</span></span>

[<span data-ttu-id="258cf-141">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="258cf-141">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="258cf-142">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="258cf-142">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="258cf-143">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="258cf-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 355690129f8edcda2586d2dfee570254ce44d998
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493308"
---
# <span data-ttu-id="8f497-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="8f497-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="8f497-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f497-102">SYNOPSIS</span></span>
<span data-ttu-id="8f497-103">데이터베이스 서버 간의 탄력적 데이터베이스 트랜잭션에 대한 통신 링크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8f497-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="8f497-104">구문</span><span class="sxs-lookup"><span data-stu-id="8f497-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f497-105">설명</span><span class="sxs-lookup"><span data-stu-id="8f497-105">DESCRIPTION</span></span>
<span data-ttu-id="8f497-106">**Get-AzSqlServerCommunicationLink** cmdlet은 Azure SQL Database에서 탄력적 데이터베이스 트랜잭션에 대한 서버 간 통신 링크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8f497-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="8f497-107">해당 링크의 속성을 확인하려면 서버 통신 링크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f497-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="8f497-108">예제</span><span class="sxs-lookup"><span data-stu-id="8f497-108">EXAMPLES</span></span>

### <span data-ttu-id="8f497-109">예제 1: 서버에 대한 모든 통신 링크 다운로드</span><span class="sxs-lookup"><span data-stu-id="8f497-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="8f497-110">이 명령은 ContosoServer17이라는 서버에 대한 탄력적 데이터베이스 트랜잭션에 대한 모든 서버 간 통신 링크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8f497-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="8f497-111">예제 2: 서버에 대한 특정 통신 링크 다운로드</span><span class="sxs-lookup"><span data-stu-id="8f497-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="8f497-112">이 명령은 Link01이라는 서버 간 통신 링크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8f497-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="8f497-113">예제 3: 필터링을 사용하여 서버에 대한 모든 통신 링크 다운로드</span><span class="sxs-lookup"><span data-stu-id="8f497-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="8f497-114">이 명령은 "Link"로 시작하는 ContosoServer17이라는 서버에 대한 탄력적 데이터베이스 트랜잭션에 대한 모든 서버 간 통신 링크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8f497-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="8f497-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f497-115">PARAMETERS</span></span>

### <span data-ttu-id="8f497-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f497-116">-DefaultProfile</span></span>
<span data-ttu-id="8f497-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8f497-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f497-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="8f497-118">-LinkName</span></span>
<span data-ttu-id="8f497-119">이 cmdlet에서 얻을 서버 통신 링크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f497-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f497-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f497-120">-ResourceGroupName</span></span>
<span data-ttu-id="8f497-121">*ServerName* 매개 변수로 지정된 서버가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f497-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="8f497-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8f497-122">-ServerName</span></span>
<span data-ttu-id="8f497-123">서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f497-123">Specifies the name of a server.</span></span>
<span data-ttu-id="8f497-124">이 서버에는 이 cmdlet이 얻을 수 있는 통신 링크가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8f497-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8f497-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f497-125">-Confirm</span></span>
<span data-ttu-id="8f497-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f497-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f497-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f497-127">-WhatIf</span></span>
<span data-ttu-id="8f497-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8f497-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f497-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f497-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f497-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f497-130">CommonParameters</span></span>
<span data-ttu-id="8f497-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8f497-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f497-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8f497-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f497-133">입력</span><span class="sxs-lookup"><span data-stu-id="8f497-133">INPUTS</span></span>

### <span data-ttu-id="8f497-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8f497-134">System.String</span></span>

## <span data-ttu-id="8f497-135">출력</span><span class="sxs-lookup"><span data-stu-id="8f497-135">OUTPUTS</span></span>

### <span data-ttu-id="8f497-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="8f497-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="8f497-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8f497-137">NOTES</span></span>
* <span data-ttu-id="8f497-138">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, 데이터베이스, mssql</span><span class="sxs-lookup"><span data-stu-id="8f497-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="8f497-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f497-139">RELATED LINKS</span></span>

[<span data-ttu-id="8f497-140">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="8f497-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="8f497-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="8f497-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="8f497-142">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="8f497-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
ms.openlocfilehash: ed6f1c2a689ed122ac16004b80f2ab0f0ea2ea3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995176"
---
# <span data-ttu-id="a58b4-101">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="a58b4-101">Remove-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="a58b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a58b4-102">SYNOPSIS</span></span>
<span data-ttu-id="a58b4-103">두 서버 간의 탄력적 데이터베이스 트랜잭션에 대한 통신 링크를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a58b4-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

## <span data-ttu-id="a58b4-104">구문</span><span class="sxs-lookup"><span data-stu-id="a58b4-104">SYNTAX</span></span>

```
Remove-AzSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a58b4-105">설명</span><span class="sxs-lookup"><span data-stu-id="a58b4-105">DESCRIPTION</span></span>
<span data-ttu-id="a58b4-106">**Remove-AzSqlServerCommunicationLink** cmdlet은 Azure SQL 데이터베이스에서 탄력적 데이터베이스 트랜잭션에 대한 서버 간 통신 링크를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a58b4-106">The **Remove-AzSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="a58b4-107">예제</span><span class="sxs-lookup"><span data-stu-id="a58b4-107">EXAMPLES</span></span>

### <span data-ttu-id="a58b4-108">예제 1: 통신 링크 삭제</span><span class="sxs-lookup"><span data-stu-id="a58b4-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="a58b4-109">이 명령은 ContosoServer17의 Link01이라는 서버 간 통신 링크를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a58b4-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="a58b4-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a58b4-110">PARAMETERS</span></span>

### <span data-ttu-id="a58b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a58b4-111">-DefaultProfile</span></span>
<span data-ttu-id="a58b4-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a58b4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a58b4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a58b4-113">-Force</span></span>
<span data-ttu-id="a58b4-114">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a58b4-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a58b4-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="a58b4-115">-LinkName</span></span>
<span data-ttu-id="a58b4-116">이 cmdlet이 삭제하는 서버 통신 링크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a58b4-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a58b4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a58b4-117">-ResourceGroupName</span></span>
<span data-ttu-id="a58b4-118">*ServerName* 매개 변수에 의해 지정된 서버가 속하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a58b4-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="a58b4-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a58b4-119">-ServerName</span></span>
<span data-ttu-id="a58b4-120">서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a58b4-120">Specifies the name of a server.</span></span>
<span data-ttu-id="a58b4-121">이 서버에는 이 cmdlet이 삭제하는 통신 링크가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a58b4-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="a58b4-122">-확인</span><span class="sxs-lookup"><span data-stu-id="a58b4-122">-Confirm</span></span>
<span data-ttu-id="a58b4-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a58b4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a58b4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a58b4-124">-WhatIf</span></span>
<span data-ttu-id="a58b4-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a58b4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a58b4-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a58b4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a58b4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a58b4-127">CommonParameters</span></span>
<span data-ttu-id="a58b4-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a58b4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a58b4-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a58b4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a58b4-130">입력</span><span class="sxs-lookup"><span data-stu-id="a58b4-130">INPUTS</span></span>

### <span data-ttu-id="a58b4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a58b4-131">System.String</span></span>

## <span data-ttu-id="a58b4-132">출력</span><span class="sxs-lookup"><span data-stu-id="a58b4-132">OUTPUTS</span></span>

### <span data-ttu-id="a58b4-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="a58b4-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="a58b4-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a58b4-134">NOTES</span></span>
* <span data-ttu-id="a58b4-135">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, 데이터베이스, mssql</span><span class="sxs-lookup"><span data-stu-id="a58b4-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="a58b4-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a58b4-136">RELATED LINKS</span></span>

[<span data-ttu-id="a58b4-137">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="a58b4-137">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="a58b4-138">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="a58b4-138">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="a58b4-139">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="a58b4-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

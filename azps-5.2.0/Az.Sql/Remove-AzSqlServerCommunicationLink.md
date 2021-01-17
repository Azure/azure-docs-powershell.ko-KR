---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 064262f16a67920b84ca00803325108cc34e6fe5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369489"
---
# <span data-ttu-id="f5a84-101">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="f5a84-101">Remove-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="f5a84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5a84-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a84-103">두 서버 간의 탄력적 데이터베이스 트랜잭션에 대한 통신 링크를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a84-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

## <span data-ttu-id="f5a84-104">구문</span><span class="sxs-lookup"><span data-stu-id="f5a84-104">SYNTAX</span></span>

```
Remove-AzSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5a84-105">설명</span><span class="sxs-lookup"><span data-stu-id="f5a84-105">DESCRIPTION</span></span>
<span data-ttu-id="f5a84-106">**Remove-AzSqlServerCommunicationLink** cmdlet은 Azure SQL Database에서 탄력적 데이터베이스 트랜잭션에 대한 서버 간 통신 링크를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a84-106">The **Remove-AzSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="f5a84-107">예제</span><span class="sxs-lookup"><span data-stu-id="f5a84-107">EXAMPLES</span></span>

### <span data-ttu-id="f5a84-108">예제 1: 통신 링크 삭제</span><span class="sxs-lookup"><span data-stu-id="f5a84-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="f5a84-109">이 명령은 ContosoServer17의 Link01이라는 서버 간 통신 링크를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a84-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="f5a84-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5a84-110">PARAMETERS</span></span>

### <span data-ttu-id="f5a84-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5a84-111">-DefaultProfile</span></span>
<span data-ttu-id="f5a84-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f5a84-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5a84-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f5a84-113">-Force</span></span>
<span data-ttu-id="f5a84-114">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a84-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f5a84-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="f5a84-115">-LinkName</span></span>
<span data-ttu-id="f5a84-116">이 cmdlet이 삭제하는 서버 통신 링크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a84-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="f5a84-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5a84-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5a84-118">*ServerName* 매개 변수로 지정된 서버가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a84-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="f5a84-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f5a84-119">-ServerName</span></span>
<span data-ttu-id="f5a84-120">서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a84-120">Specifies the name of a server.</span></span>
<span data-ttu-id="f5a84-121">이 서버에는 이 cmdlet이 삭제하는 통신 링크가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f5a84-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="f5a84-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5a84-122">-Confirm</span></span>
<span data-ttu-id="f5a84-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5a84-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5a84-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5a84-124">-WhatIf</span></span>
<span data-ttu-id="f5a84-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f5a84-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5a84-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5a84-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5a84-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a84-127">CommonParameters</span></span>
<span data-ttu-id="f5a84-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f5a84-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a84-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f5a84-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a84-130">입력</span><span class="sxs-lookup"><span data-stu-id="f5a84-130">INPUTS</span></span>

### <span data-ttu-id="f5a84-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f5a84-131">System.String</span></span>

## <span data-ttu-id="f5a84-132">출력</span><span class="sxs-lookup"><span data-stu-id="f5a84-132">OUTPUTS</span></span>

### <span data-ttu-id="f5a84-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="f5a84-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="f5a84-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f5a84-134">NOTES</span></span>
* <span data-ttu-id="f5a84-135">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, 데이터베이스, mssql</span><span class="sxs-lookup"><span data-stu-id="f5a84-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="f5a84-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5a84-136">RELATED LINKS</span></span>

[<span data-ttu-id="f5a84-137">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="f5a84-137">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="f5a84-138">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="f5a84-138">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="f5a84-139">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="f5a84-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

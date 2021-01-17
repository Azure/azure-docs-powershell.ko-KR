---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
ms.openlocfilehash: 670b3e6ec71a768fe40bbcf542440db5ec685b2f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369517"
---
# <span data-ttu-id="03e45-101">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="03e45-101">Remove-AzSqlServer</span></span>

## <span data-ttu-id="03e45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03e45-102">SYNOPSIS</span></span>
<span data-ttu-id="03e45-103">Azure SQL 데이터베이스 서버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="03e45-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="03e45-104">구문</span><span class="sxs-lookup"><span data-stu-id="03e45-104">SYNTAX</span></span>

```
Remove-AzSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03e45-105">설명</span><span class="sxs-lookup"><span data-stu-id="03e45-105">DESCRIPTION</span></span>
<span data-ttu-id="03e45-106">**Remove-AzSqlServer** cmdlet은 Azure SQL 데이터베이스 서버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="03e45-106">The **Remove-AzSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="03e45-107">삭제 작업은 비동기적이기 때문에 완전히 삭제되는 서버에 종속된 추가 작업을 수행하기 전에 작업이 완료된 것을 확인하는 데 시간이 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e45-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="03e45-108">예를 들어 동일한 이름을 사용하는 새 서버를 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03e45-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="03e45-109">예제</span><span class="sxs-lookup"><span data-stu-id="03e45-109">EXAMPLES</span></span>

### <span data-ttu-id="03e45-110">예제 1: 서버 제거</span><span class="sxs-lookup"><span data-stu-id="03e45-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="03e45-111">이 명령은 Server01이라는 Azure SQL 데이터베이스 서버를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="03e45-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="03e45-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03e45-112">PARAMETERS</span></span>

### <span data-ttu-id="03e45-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03e45-113">-DefaultProfile</span></span>
<span data-ttu-id="03e45-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="03e45-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03e45-115">-Force</span><span class="sxs-lookup"><span data-stu-id="03e45-115">-Force</span></span>
<span data-ttu-id="03e45-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="03e45-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="03e45-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03e45-117">-ResourceGroupName</span></span>
<span data-ttu-id="03e45-118">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e45-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="03e45-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="03e45-119">-ServerName</span></span>
<span data-ttu-id="03e45-120">제거할 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e45-120">Specifies the name of the server to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03e45-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03e45-121">-Confirm</span></span>
<span data-ttu-id="03e45-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e45-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03e45-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03e45-123">-WhatIf</span></span>
<span data-ttu-id="03e45-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="03e45-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03e45-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e45-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03e45-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03e45-126">CommonParameters</span></span>
<span data-ttu-id="03e45-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03e45-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03e45-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="03e45-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03e45-129">입력</span><span class="sxs-lookup"><span data-stu-id="03e45-129">INPUTS</span></span>

### <span data-ttu-id="03e45-130">System.String</span><span class="sxs-lookup"><span data-stu-id="03e45-130">System.String</span></span>

## <span data-ttu-id="03e45-131">출력</span><span class="sxs-lookup"><span data-stu-id="03e45-131">OUTPUTS</span></span>

### <span data-ttu-id="03e45-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="03e45-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="03e45-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="03e45-133">NOTES</span></span>

## <span data-ttu-id="03e45-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03e45-134">RELATED LINKS</span></span>

[<span data-ttu-id="03e45-135">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="03e45-135">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="03e45-136">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="03e45-136">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="03e45-137">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="03e45-137">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="03e45-138">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="03e45-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



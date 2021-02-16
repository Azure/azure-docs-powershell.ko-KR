---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: f6beaa0651e406d94e1718bb1b1fdea6ef1c3507
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178300"
---
# <span data-ttu-id="5eb4c-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="5eb4c-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="5eb4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eb4c-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb4c-103">데이터베이스의 비동기 업데이트 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="5eb4c-104">구문</span><span class="sxs-lookup"><span data-stu-id="5eb4c-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5eb4c-105">설명</span><span class="sxs-lookup"><span data-stu-id="5eb4c-105">DESCRIPTION</span></span>
<span data-ttu-id="5eb4c-106">**Stop-AzSqlDatabaseActivity** cmdlet은 데이터베이스에 대한 비동기 업데이트 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="5eb4c-107">예제</span><span class="sxs-lookup"><span data-stu-id="5eb4c-107">EXAMPLES</span></span>

### <span data-ttu-id="5eb4c-108">예제 1: 데이터베이스의 비동기 업데이트 작업 취소</span><span class="sxs-lookup"><span data-stu-id="5eb4c-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : Database01
State           : CANCELLED
Operation       : UpdateLogicalDatabase
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete : 
Properties      : Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel+DatabaseState
```

<span data-ttu-id="5eb4c-109">이 명령은 데이터베이스의 비동기 업데이트 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="5eb4c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5eb4c-110">PARAMETERS</span></span>

### <span data-ttu-id="5eb4c-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5eb4c-111">-DatabaseName</span></span>
<span data-ttu-id="5eb4c-112">이 cmdlet이 상태를 얻을 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eb4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eb4c-113">-DefaultProfile</span></span>
<span data-ttu-id="5eb4c-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5eb4c-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5eb4c-115">-ElasticPoolName</span></span>
<span data-ttu-id="5eb4c-116">Azure SQL 탄력적 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-116">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eb4c-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5eb4c-117">-OperationId</span></span>
<span data-ttu-id="5eb4c-118">이 cmdlet에서 얻을 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eb4c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eb4c-119">-ResourceGroupName</span></span>
<span data-ttu-id="5eb4c-120">데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5eb4c-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5eb4c-121">-ServerName</span></span>
<span data-ttu-id="5eb4c-122">데이터베이스를 호스트하는 Microsoft SQL Server 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="5eb4c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5eb4c-123">-Confirm</span></span>
<span data-ttu-id="5eb4c-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eb4c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eb4c-125">-WhatIf</span></span>
<span data-ttu-id="5eb4c-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5eb4c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5eb4c-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eb4c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb4c-128">CommonParameters</span></span>
<span data-ttu-id="5eb4c-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb4c-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5eb4c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb4c-131">입력</span><span class="sxs-lookup"><span data-stu-id="5eb4c-131">INPUTS</span></span>

### <span data-ttu-id="5eb4c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5eb4c-132">System.String</span></span>

### <span data-ttu-id="5eb4c-133">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5eb4c-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5eb4c-134">출력</span><span class="sxs-lookup"><span data-stu-id="5eb4c-134">OUTPUTS</span></span>

### <span data-ttu-id="5eb4c-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="5eb4c-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="5eb4c-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5eb4c-136">NOTES</span></span>

## <span data-ttu-id="5eb4c-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5eb4c-137">RELATED LINKS</span></span>

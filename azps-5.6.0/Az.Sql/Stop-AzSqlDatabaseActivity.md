---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: 014cd61e53f002a2615153103ddcbb0b966751a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008459"
---
# <span data-ttu-id="4dd13-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="4dd13-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="4dd13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dd13-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd13-103">데이터베이스의 비동기 업데이트 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd13-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="4dd13-104">구문</span><span class="sxs-lookup"><span data-stu-id="4dd13-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dd13-105">설명</span><span class="sxs-lookup"><span data-stu-id="4dd13-105">DESCRIPTION</span></span>
<span data-ttu-id="4dd13-106">**Stop-AzSqlDatabaseActivity** cmdlet은 데이터베이스의 비동기 업데이트 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd13-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="4dd13-107">예제</span><span class="sxs-lookup"><span data-stu-id="4dd13-107">EXAMPLES</span></span>

### <span data-ttu-id="4dd13-108">예제 1: 데이터베이스의 비동기 업데이트 작업 취소</span><span class="sxs-lookup"><span data-stu-id="4dd13-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
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

<span data-ttu-id="4dd13-109">이 명령은 데이터베이스의 비동기 업데이트 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd13-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="4dd13-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4dd13-110">PARAMETERS</span></span>

### <span data-ttu-id="4dd13-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4dd13-111">-DatabaseName</span></span>
<span data-ttu-id="4dd13-112">이 cmdlet이 상태를 얻을 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd13-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="4dd13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd13-113">-DefaultProfile</span></span>
<span data-ttu-id="4dd13-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4dd13-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dd13-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4dd13-115">-ElasticPoolName</span></span>
<span data-ttu-id="4dd13-116">Azure SQL 탄력적 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="4dd13-116">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="4dd13-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="4dd13-117">-OperationId</span></span>
<span data-ttu-id="4dd13-118">이 cmdlet이 얻을 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd13-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4dd13-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dd13-119">-ResourceGroupName</span></span>
<span data-ttu-id="4dd13-120">데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd13-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="4dd13-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4dd13-121">-ServerName</span></span>
<span data-ttu-id="4dd13-122">데이터베이스를 호스트하는 Microsoft SQL Server 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd13-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="4dd13-123">-확인</span><span class="sxs-lookup"><span data-stu-id="4dd13-123">-Confirm</span></span>
<span data-ttu-id="4dd13-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4dd13-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dd13-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dd13-125">-WhatIf</span></span>
<span data-ttu-id="4dd13-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4dd13-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dd13-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4dd13-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dd13-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd13-128">CommonParameters</span></span>
<span data-ttu-id="4dd13-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4dd13-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd13-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dd13-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd13-131">입력</span><span class="sxs-lookup"><span data-stu-id="4dd13-131">INPUTS</span></span>

### <span data-ttu-id="4dd13-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4dd13-132">System.String</span></span>

### <span data-ttu-id="4dd13-133">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4dd13-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4dd13-134">출력</span><span class="sxs-lookup"><span data-stu-id="4dd13-134">OUTPUTS</span></span>

### <span data-ttu-id="4dd13-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="4dd13-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="4dd13-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4dd13-136">NOTES</span></span>

## <span data-ttu-id="4dd13-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4dd13-137">RELATED LINKS</span></span>

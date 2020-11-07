---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: f4f3b935aa9303ab38888d6f28f0a89bbdeb6c23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698734"
---
# <span data-ttu-id="52a5c-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="52a5c-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="52a5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="52a5c-103">데이터베이스에서 비동기 업데이트 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a5c-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="52a5c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="52a5c-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52a5c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="52a5c-105">DESCRIPTION</span></span>
<span data-ttu-id="52a5c-106">**AzSqlDatabaseActivity** cmdlet은 데이터베이스에서 비동기 업데이트 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a5c-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="52a5c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="52a5c-107">EXAMPLES</span></span>

### <span data-ttu-id="52a5c-108">예제 1: 데이터베이스에서 비동기 업데이트 작업 취소</span><span class="sxs-lookup"><span data-stu-id="52a5c-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
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

<span data-ttu-id="52a5c-109">이 명령은 데이터베이스에서 비동기 업데이트 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a5c-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="52a5c-110">변수</span><span class="sxs-lookup"><span data-stu-id="52a5c-110">PARAMETERS</span></span>

### <span data-ttu-id="52a5c-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="52a5c-111">-DatabaseName</span></span>
<span data-ttu-id="52a5c-112">이 cmdlet이 상태를 가져오는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a5c-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="52a5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a5c-113">-DefaultProfile</span></span>
<span data-ttu-id="52a5c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52a5c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52a5c-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="52a5c-115">-ElasticPoolName</span></span>
<span data-ttu-id="52a5c-116">Azure SQL 탄력적 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52a5c-116">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="52a5c-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="52a5c-117">-OperationId</span></span>
<span data-ttu-id="52a5c-118">이 cmdlet이 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a5c-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="52a5c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52a5c-119">-ResourceGroupName</span></span>
<span data-ttu-id="52a5c-120">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a5c-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="52a5c-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="52a5c-121">-ServerName</span></span>
<span data-ttu-id="52a5c-122">데이터베이스를 호스트 하는 Microsoft SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a5c-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="52a5c-123">-확인</span><span class="sxs-lookup"><span data-stu-id="52a5c-123">-Confirm</span></span>
<span data-ttu-id="52a5c-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a5c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52a5c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52a5c-125">-WhatIf</span></span>
<span data-ttu-id="52a5c-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="52a5c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52a5c-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52a5c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52a5c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a5c-128">CommonParameters</span></span>
<span data-ttu-id="52a5c-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="52a5c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a5c-130">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="52a5c-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a5c-131">입력</span><span class="sxs-lookup"><span data-stu-id="52a5c-131">INPUTS</span></span>

### <span data-ttu-id="52a5c-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="52a5c-132">System.String</span></span>

### <span data-ttu-id="52a5c-133">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="52a5c-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="52a5c-134">출력</span><span class="sxs-lookup"><span data-stu-id="52a5c-134">OUTPUTS</span></span>

### <span data-ttu-id="52a5c-135">AzureSqlDatabaseActivityModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="52a5c-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="52a5c-136">상속자</span><span class="sxs-lookup"><span data-stu-id="52a5c-136">NOTES</span></span>

## <span data-ttu-id="52a5c-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52a5c-137">RELATED LINKS</span></span>

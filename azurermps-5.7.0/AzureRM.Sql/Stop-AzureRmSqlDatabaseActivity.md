---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: d0aa42b8b584ade698c3d03848a537350ac342d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703208"
---
# <span data-ttu-id="31b0b-101">Stop-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="31b0b-101">Stop-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="31b0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="31b0b-103">데이터베이스에서 비동기 업데이트 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b0b-103">Cancels the asynchronous updates operation on the database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31b0b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31b0b-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31b0b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="31b0b-105">DESCRIPTION</span></span>
<span data-ttu-id="31b0b-106">**AzureRmSqlDatabaseActivity** cmdlet은 데이터베이스에서 비동기 업데이트 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b0b-106">The **Stop-AzureRmSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="31b0b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="31b0b-107">EXAMPLES</span></span>

### <span data-ttu-id="31b0b-108">예제 1: 데이터베이스에서 비동기 업데이트 작업 취소</span><span class="sxs-lookup"><span data-stu-id="31b0b-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

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

<span data-ttu-id="31b0b-109">이 명령은 데이터베이스에서 비동기 업데이트 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b0b-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="31b0b-110">변수</span><span class="sxs-lookup"><span data-stu-id="31b0b-110">PARAMETERS</span></span>

### <span data-ttu-id="31b0b-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="31b0b-111">-DatabaseName</span></span>
<span data-ttu-id="31b0b-112">이 cmdlet이 상태를 가져오는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b0b-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b0b-113">-DefaultProfile</span></span>
<span data-ttu-id="31b0b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31b0b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31b0b-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="31b0b-115">-ElasticPoolName</span></span>
<span data-ttu-id="31b0b-116">Azure SQL 탄력적 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="31b0b-116">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b0b-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="31b0b-117">-OperationId</span></span>
<span data-ttu-id="31b0b-118">이 cmdlet이 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b0b-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b0b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b0b-119">-ResourceGroupName</span></span>
<span data-ttu-id="31b0b-120">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b0b-120">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="31b0b-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="31b0b-121">-ServerName</span></span>
<span data-ttu-id="31b0b-122">데이터베이스를 호스트 하는 Microsoft SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b0b-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b0b-123">-확인</span><span class="sxs-lookup"><span data-stu-id="31b0b-123">-Confirm</span></span>
<span data-ttu-id="31b0b-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b0b-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b0b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31b0b-125">-WhatIf</span></span>
<span data-ttu-id="31b0b-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="31b0b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31b0b-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31b0b-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b0b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b0b-128">CommonParameters</span></span>
<span data-ttu-id="31b0b-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b0b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b0b-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b0b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b0b-131">입력</span><span class="sxs-lookup"><span data-stu-id="31b0b-131">INPUTS</span></span>

### <span data-ttu-id="31b0b-132">않아야</span><span class="sxs-lookup"><span data-stu-id="31b0b-132">None</span></span>
<span data-ttu-id="31b0b-133">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31b0b-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31b0b-134">출력</span><span class="sxs-lookup"><span data-stu-id="31b0b-134">OUTPUTS</span></span>

### <span data-ttu-id="31b0b-135">AzureSqlDatabaseActivityModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="31b0b-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="31b0b-136">상속자</span><span class="sxs-lookup"><span data-stu-id="31b0b-136">NOTES</span></span>

## <span data-ttu-id="31b0b-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31b0b-137">RELATED LINKS</span></span>

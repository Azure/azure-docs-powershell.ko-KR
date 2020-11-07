---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: 1305e9e74b0f8a2ef1a8d866d4a2dd6d62e1cef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703537"
---
# <span data-ttu-id="f404d-101">New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="f404d-101">New-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="f404d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f404d-102">SYNOPSIS</span></span>
<span data-ttu-id="f404d-103">SQL 데이터베이스를 복원할 수 있는 새 복원 지점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f404d-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f404d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f404d-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f404d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f404d-105">DESCRIPTION</span></span>
<span data-ttu-id="f404d-106">**새 AzureRmSqlDatabaseRestorePoint** Cmdlet은 Azure SQL 데이터베이스를 복원할 수 있는 새 복원 지점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f404d-106">The **New-AzureRmSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Database can be restored from.</span></span>

<span data-ttu-id="f404d-107">이 cmdlet은 Azure SQL Database의 SQL Server Datawarehouse 서비스에서 현재 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f404d-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="f404d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="f404d-108">EXAMPLES</span></span>

### <span data-ttu-id="f404d-109">예제 1: 복원 시점 만들기</span><span class="sxs-lookup"><span data-stu-id="f404d-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="f404d-110">이 명령은 Azure SQL Database의 복원 지점을 만들고 복원 지점의 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f404d-110">This command creates a restore point for Azure SQL Database and returns the details of the restore point.</span></span>

## <span data-ttu-id="f404d-111">변수</span><span class="sxs-lookup"><span data-stu-id="f404d-111">PARAMETERS</span></span>

### <span data-ttu-id="f404d-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f404d-112">-DatabaseName</span></span>
<span data-ttu-id="f404d-113">SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f404d-113">Specifies the name of the SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f404d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f404d-114">-DefaultProfile</span></span>
<span data-ttu-id="f404d-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f404d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f404d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f404d-116">-ResourceGroupName</span></span>
<span data-ttu-id="f404d-117">SQL 데이터베이스를 할당할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f404d-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="f404d-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="f404d-118">-RestorePointLabel</span></span>
<span data-ttu-id="f404d-119">쉽게 식별할 수 있도록 복원 지점의 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f404d-119">Specifies the label of the restore point for easy identification.</span></span>

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

### <span data-ttu-id="f404d-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f404d-120">-ServerName</span></span>
<span data-ttu-id="f404d-121">데이터베이스를 호스트 하는 AzureSQL 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f404d-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="f404d-122">-확인</span><span class="sxs-lookup"><span data-stu-id="f404d-122">-Confirm</span></span>
<span data-ttu-id="f404d-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f404d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f404d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f404d-124">-WhatIf</span></span>
<span data-ttu-id="f404d-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f404d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f404d-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f404d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f404d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f404d-127">CommonParameters</span></span>
<span data-ttu-id="f404d-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f404d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f404d-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f404d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f404d-130">입력</span><span class="sxs-lookup"><span data-stu-id="f404d-130">INPUTS</span></span>

## <span data-ttu-id="f404d-131">출력</span><span class="sxs-lookup"><span data-stu-id="f404d-131">OUTPUTS</span></span>

## <span data-ttu-id="f404d-132">상속자</span><span class="sxs-lookup"><span data-stu-id="f404d-132">NOTES</span></span>

## <span data-ttu-id="f404d-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f404d-133">RELATED LINKS</span></span>

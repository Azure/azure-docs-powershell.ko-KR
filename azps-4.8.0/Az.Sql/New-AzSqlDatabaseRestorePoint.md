---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: d2dc1b6acf1978976ce29adea2e79146828accb1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048652"
---
# <span data-ttu-id="8aa4a-101">New-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="8aa4a-101">New-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="8aa4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aa4a-102">SYNOPSIS</span></span>
<span data-ttu-id="8aa4a-103">SQL 데이터베이스를 복원할 수 있는 새 복원 지점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8aa4a-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

## <span data-ttu-id="8aa4a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8aa4a-104">SYNTAX</span></span>

```
New-AzSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8aa4a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8aa4a-105">DESCRIPTION</span></span>
<span data-ttu-id="8aa4a-106">**AzSqlDatabaseRestorePoint** Cmdlet은 Azure SQL 데이터 웨어하우스가 복원 될 수 있는 새 복원 지점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8aa4a-106">The **New-AzSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="8aa4a-107">이 cmdlet은 현재 Azure SQL 데이터 웨어하우스에서 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8aa4a-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="8aa4a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="8aa4a-108">EXAMPLES</span></span>

### <span data-ttu-id="8aa4a-109">예제 1: 복원 시점 만들기</span><span class="sxs-lookup"><span data-stu-id="8aa4a-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="8aa4a-110">이 명령은 Azure SQL 데이터 웨어하우스의 복원 지점을 만들고 복원 지점의 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa4a-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="8aa4a-111">변수</span><span class="sxs-lookup"><span data-stu-id="8aa4a-111">PARAMETERS</span></span>

### <span data-ttu-id="8aa4a-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8aa4a-112">-DatabaseName</span></span>
<span data-ttu-id="8aa4a-113">SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa4a-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="8aa4a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aa4a-114">-DefaultProfile</span></span>
<span data-ttu-id="8aa4a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8aa4a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8aa4a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aa4a-116">-ResourceGroupName</span></span>
<span data-ttu-id="8aa4a-117">SQL 데이터베이스를 할당할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa4a-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="8aa4a-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="8aa4a-118">-RestorePointLabel</span></span>
<span data-ttu-id="8aa4a-119">쉽게 식별할 수 있도록 복원 지점의 레이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa4a-119">Specifies the label of the restore point for easy identification.</span></span>

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

### <span data-ttu-id="8aa4a-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8aa4a-120">-ServerName</span></span>
<span data-ttu-id="8aa4a-121">데이터베이스를 호스트 하는 AzureSQL 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa4a-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="8aa4a-122">-확인</span><span class="sxs-lookup"><span data-stu-id="8aa4a-122">-Confirm</span></span>
<span data-ttu-id="8aa4a-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa4a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aa4a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aa4a-124">-WhatIf</span></span>
<span data-ttu-id="8aa4a-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8aa4a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8aa4a-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa4a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aa4a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aa4a-127">CommonParameters</span></span>
<span data-ttu-id="8aa4a-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa4a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aa4a-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8aa4a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aa4a-130">입력</span><span class="sxs-lookup"><span data-stu-id="8aa4a-130">INPUTS</span></span>

### <span data-ttu-id="8aa4a-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8aa4a-131">System.String</span></span>

## <span data-ttu-id="8aa4a-132">출력</span><span class="sxs-lookup"><span data-stu-id="8aa4a-132">OUTPUTS</span></span>

### <span data-ttu-id="8aa4a-133">AzureSqlDatabaseRestorePointModel (Microsoft.).</span><span class="sxs-lookup"><span data-stu-id="8aa4a-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="8aa4a-134">상속자</span><span class="sxs-lookup"><span data-stu-id="8aa4a-134">NOTES</span></span>

## <span data-ttu-id="8aa4a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8aa4a-135">RELATED LINKS</span></span>

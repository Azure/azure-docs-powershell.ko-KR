---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
ms.openlocfilehash: 18d387aeb8ca9e777af0767ce407e373fc2adf09
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215201"
---
# <span data-ttu-id="16126-101">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="16126-101">Get-AzSqlDatabaseExpanded</span></span>

## <span data-ttu-id="16126-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16126-102">SYNOPSIS</span></span>
<span data-ttu-id="16126-103">데이터베이스 및 확장 된 속성 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16126-103">Gets a database and its expanded property values.</span></span>

## <span data-ttu-id="16126-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16126-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16126-105">설명은</span><span class="sxs-lookup"><span data-stu-id="16126-105">DESCRIPTION</span></span>
<span data-ttu-id="16126-106">**AzSqlDatabaseExpanded** cmdlet은 데이터베이스 및 확장 된 속성 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="16126-106">The **Get-AzSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="16126-107">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16126-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="16126-108">예제의</span><span class="sxs-lookup"><span data-stu-id="16126-108">EXAMPLES</span></span>

### <span data-ttu-id="16126-109">예제 1: 서비스 계층 관리자 정보가 있는 데이터베이스 개체 가져오기</span><span class="sxs-lookup"><span data-stu-id="16126-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="16126-110">이 명령은 서비스 계층 관리자 정보를 포함 하는 확장 된 속성이 있는 데이터베이스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="16126-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

### <span data-ttu-id="16126-111">예제 2: 필터링을 사용 하 여 데이터베이스 개체 나열</span><span class="sxs-lookup"><span data-stu-id="16126-111">Example 2: List database objects using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="16126-112">이 명령은 "Database"로 시작 하는 Server01의 모든 데이터베이스에 대해 확장 된 데이터베이스 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="16126-112">This command returns expanded database object for all databases in Server01 that start with "Database".</span></span>

## <span data-ttu-id="16126-113">변수</span><span class="sxs-lookup"><span data-stu-id="16126-113">PARAMETERS</span></span>

### <span data-ttu-id="16126-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="16126-114">-DatabaseName</span></span>
<span data-ttu-id="16126-115">가져올 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16126-115">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="16126-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16126-116">-DefaultProfile</span></span>
<span data-ttu-id="16126-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="16126-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16126-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16126-118">-ResourceGroupName</span></span>
<span data-ttu-id="16126-119">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16126-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="16126-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="16126-120">-ServerName</span></span>
<span data-ttu-id="16126-121">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="16126-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="16126-122">-확인</span><span class="sxs-lookup"><span data-stu-id="16126-122">-Confirm</span></span>
<span data-ttu-id="16126-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="16126-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16126-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16126-124">-WhatIf</span></span>
<span data-ttu-id="16126-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="16126-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16126-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16126-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16126-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16126-127">CommonParameters</span></span>
<span data-ttu-id="16126-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16126-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16126-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="16126-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16126-130">입력</span><span class="sxs-lookup"><span data-stu-id="16126-130">INPUTS</span></span>

### <span data-ttu-id="16126-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="16126-131">System.String</span></span>

## <span data-ttu-id="16126-132">출력</span><span class="sxs-lookup"><span data-stu-id="16126-132">OUTPUTS</span></span>

### <span data-ttu-id="16126-133">AzureSqlDatabaseModelExpanded을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="16126-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="16126-134">상속자</span><span class="sxs-lookup"><span data-stu-id="16126-134">NOTES</span></span>

## <span data-ttu-id="16126-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16126-135">RELATED LINKS</span></span>

[<span data-ttu-id="16126-136">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="16126-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

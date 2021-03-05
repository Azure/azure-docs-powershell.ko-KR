---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseExpanded.md
ms.openlocfilehash: d7eb52a9da5866b4aed280f1ac35651800c67a25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995876"
---
# <span data-ttu-id="52adc-101">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="52adc-101">Get-AzSqlDatabaseExpanded</span></span>

## <span data-ttu-id="52adc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52adc-102">SYNOPSIS</span></span>
<span data-ttu-id="52adc-103">데이터베이스 및 확장된 속성 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="52adc-103">Gets a database and its expanded property values.</span></span>

## <span data-ttu-id="52adc-104">구문</span><span class="sxs-lookup"><span data-stu-id="52adc-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52adc-105">설명</span><span class="sxs-lookup"><span data-stu-id="52adc-105">DESCRIPTION</span></span>
<span data-ttu-id="52adc-106">**Get-AzSqlDatabaseExpanded** cmdlet은 데이터베이스 및 확장된 속성 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="52adc-106">The **Get-AzSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>
<span data-ttu-id="52adc-107">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="52adc-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="52adc-108">예제</span><span class="sxs-lookup"><span data-stu-id="52adc-108">EXAMPLES</span></span>

### <span data-ttu-id="52adc-109">예제 1: 서비스 계층 어드바이저 정보가 있는 데이터베이스 개체 얻기</span><span class="sxs-lookup"><span data-stu-id="52adc-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="52adc-110">이 명령은 서비스 계층 어드바이저 정보를 포함하는 확장된 속성이 있는 데이터베이스를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="52adc-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

### <span data-ttu-id="52adc-111">예제 2: 필터링을 사용하여 데이터베이스 개체 나열</span><span class="sxs-lookup"><span data-stu-id="52adc-111">Example 2: List database objects using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="52adc-112">이 명령은 "Database"로 시작하는 Server01의 모든 데이터베이스에 대해 확장된 데이터베이스 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="52adc-112">This command returns expanded database object for all databases in Server01 that start with "Database".</span></span>

## <span data-ttu-id="52adc-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="52adc-113">PARAMETERS</span></span>

### <span data-ttu-id="52adc-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="52adc-114">-DatabaseName</span></span>
<span data-ttu-id="52adc-115">얻을 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="52adc-115">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="52adc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52adc-116">-DefaultProfile</span></span>
<span data-ttu-id="52adc-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="52adc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52adc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52adc-118">-ResourceGroupName</span></span>
<span data-ttu-id="52adc-119">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="52adc-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="52adc-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="52adc-120">-ServerName</span></span>
<span data-ttu-id="52adc-121">데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="52adc-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="52adc-122">-확인</span><span class="sxs-lookup"><span data-stu-id="52adc-122">-Confirm</span></span>
<span data-ttu-id="52adc-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="52adc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52adc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52adc-124">-WhatIf</span></span>
<span data-ttu-id="52adc-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="52adc-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52adc-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52adc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52adc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52adc-127">CommonParameters</span></span>
<span data-ttu-id="52adc-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="52adc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52adc-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52adc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52adc-130">입력</span><span class="sxs-lookup"><span data-stu-id="52adc-130">INPUTS</span></span>

### <span data-ttu-id="52adc-131">System.String</span><span class="sxs-lookup"><span data-stu-id="52adc-131">System.String</span></span>

## <span data-ttu-id="52adc-132">출력</span><span class="sxs-lookup"><span data-stu-id="52adc-132">OUTPUTS</span></span>

### <span data-ttu-id="52adc-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span><span class="sxs-lookup"><span data-stu-id="52adc-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModelExpanded</span></span>

## <span data-ttu-id="52adc-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="52adc-134">NOTES</span></span>

## <span data-ttu-id="52adc-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52adc-135">RELATED LINKS</span></span>

[<span data-ttu-id="52adc-136">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="52adc-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

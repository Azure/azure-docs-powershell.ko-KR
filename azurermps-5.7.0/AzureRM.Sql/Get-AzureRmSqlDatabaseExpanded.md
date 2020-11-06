---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
ms.openlocfilehash: 472e8e7a2f0919115686764136b6b40f5e1da913
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529704"
---
# <span data-ttu-id="e963d-101">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="e963d-101">Get-AzureRmSqlDatabaseExpanded</span></span>

## <span data-ttu-id="e963d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e963d-102">SYNOPSIS</span></span>
<span data-ttu-id="e963d-103">데이터베이스 및 확장 된 속성 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e963d-103">Gets a database and its expanded property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e963d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e963d-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e963d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e963d-105">DESCRIPTION</span></span>
<span data-ttu-id="e963d-106">**AzureRmSqlDatabaseExpanded** cmdlet은 데이터베이스 및 확장 된 속성 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e963d-106">The **Get-AzureRmSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>

<span data-ttu-id="e963d-107">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e963d-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e963d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e963d-108">EXAMPLES</span></span>

### <span data-ttu-id="e963d-109">예제 1: 서비스 계층 관리자 정보가 있는 데이터베이스 개체 가져오기</span><span class="sxs-lookup"><span data-stu-id="e963d-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\>Get-AzureSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="e963d-110">이 명령은 서비스 계층 관리자 정보를 포함 하는 확장 된 속성이 있는 데이터베이스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e963d-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

## <span data-ttu-id="e963d-111">변수</span><span class="sxs-lookup"><span data-stu-id="e963d-111">PARAMETERS</span></span>

### <span data-ttu-id="e963d-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e963d-112">-DatabaseName</span></span>
<span data-ttu-id="e963d-113">가져올 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e963d-113">Specifies the name of the database to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e963d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e963d-114">-DefaultProfile</span></span>
<span data-ttu-id="e963d-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e963d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e963d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e963d-116">-ResourceGroupName</span></span>
<span data-ttu-id="e963d-117">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e963d-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e963d-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e963d-118">-ServerName</span></span>
<span data-ttu-id="e963d-119">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e963d-119">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="e963d-120">-확인</span><span class="sxs-lookup"><span data-stu-id="e963d-120">-Confirm</span></span>
<span data-ttu-id="e963d-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e963d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e963d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e963d-122">-WhatIf</span></span>
<span data-ttu-id="e963d-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e963d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e963d-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e963d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e963d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e963d-125">CommonParameters</span></span>
<span data-ttu-id="e963d-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e963d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e963d-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e963d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e963d-128">입력</span><span class="sxs-lookup"><span data-stu-id="e963d-128">INPUTS</span></span>

### <span data-ttu-id="e963d-129">않아야</span><span class="sxs-lookup"><span data-stu-id="e963d-129">None</span></span>
<span data-ttu-id="e963d-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e963d-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e963d-131">출력</span><span class="sxs-lookup"><span data-stu-id="e963d-131">OUTPUTS</span></span>

## <span data-ttu-id="e963d-132">상속자</span><span class="sxs-lookup"><span data-stu-id="e963d-132">NOTES</span></span>

## <span data-ttu-id="e963d-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e963d-133">RELATED LINKS</span></span>

[<span data-ttu-id="e963d-134">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="e963d-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

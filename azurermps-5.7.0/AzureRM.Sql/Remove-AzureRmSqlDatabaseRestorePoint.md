---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-EF14-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: 235165b178a721bf5e450a2430a6454eb3b2c1be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533576"
---
# <span data-ttu-id="322aa-101">Remove-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="322aa-101">Remove-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="322aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="322aa-102">SYNOPSIS</span></span>
<span data-ttu-id="322aa-103">SQL 데이터베이스에서 지정 된 복원 지점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="322aa-103">Removes given restore point from a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="322aa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="322aa-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseRestorePoint -RestorePointCreationDate <DateTime> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="322aa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="322aa-105">DESCRIPTION</span></span>
<span data-ttu-id="322aa-106">**AzureRmSqlDatabaseRestorePoint** Cmdlet은 Azure SQL 데이터베이스에서 지정 된 복원 지점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="322aa-106">The **Remove-AzureRmSqlDatabaseRestorePoint** cmdlet removes given restore point from Azure SQL Database.</span></span>

<span data-ttu-id="322aa-107">이 cmdlet은 Azure SQL Database의 SQL Server Datawarehouse 서비스에서 현재 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="322aa-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="322aa-108">예제의</span><span class="sxs-lookup"><span data-stu-id="322aa-108">EXAMPLES</span></span>

### <span data-ttu-id="322aa-109">예제 1: 복원 지점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="322aa-109">Example 1: Removes a restore point</span></span>
```
PS C:\>$RestorePointCreationDate = Get-Date "3/11/2017 1:50:00 AM"
PS C:\>Remove-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointCreationDate $RestorePointCreationDate
```

<span data-ttu-id="322aa-110">이 명령은 Azure SQL Database에서 제공 된 생성 날짜에 대 한 복원 지점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="322aa-110">This command removes a restore point for Azure SQL Database given creation date.</span></span>

## <span data-ttu-id="322aa-111">변수</span><span class="sxs-lookup"><span data-stu-id="322aa-111">PARAMETERS</span></span>

### <span data-ttu-id="322aa-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="322aa-112">-DatabaseName</span></span>
<span data-ttu-id="322aa-113">SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="322aa-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="322aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="322aa-114">-DefaultProfile</span></span>
<span data-ttu-id="322aa-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="322aa-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="322aa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="322aa-116">-ResourceGroupName</span></span>
<span data-ttu-id="322aa-117">SQL 데이터베이스를 할당할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="322aa-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="322aa-118">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="322aa-118">-RestorePointCreationDate</span></span>
<span data-ttu-id="322aa-119">복원 시점 만든 날짜를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="322aa-119">Specifies the restore point creation date.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="322aa-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="322aa-120">-ServerName</span></span>
<span data-ttu-id="322aa-121">데이터베이스를 호스트 하는 AzureSQL 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="322aa-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="322aa-122">-확인</span><span class="sxs-lookup"><span data-stu-id="322aa-122">-Confirm</span></span>
<span data-ttu-id="322aa-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="322aa-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="322aa-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="322aa-124">-WhatIf</span></span>
<span data-ttu-id="322aa-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="322aa-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="322aa-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="322aa-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="322aa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="322aa-127">CommonParameters</span></span>
<span data-ttu-id="322aa-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="322aa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="322aa-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="322aa-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="322aa-130">입력</span><span class="sxs-lookup"><span data-stu-id="322aa-130">INPUTS</span></span>

## <span data-ttu-id="322aa-131">출력</span><span class="sxs-lookup"><span data-stu-id="322aa-131">OUTPUTS</span></span>

## <span data-ttu-id="322aa-132">상속자</span><span class="sxs-lookup"><span data-stu-id="322aa-132">NOTES</span></span>

## <span data-ttu-id="322aa-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="322aa-133">RELATED LINKS</span></span>

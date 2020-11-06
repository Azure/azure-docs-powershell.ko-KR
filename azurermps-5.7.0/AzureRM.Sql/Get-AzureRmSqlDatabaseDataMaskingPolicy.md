---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: bb6beb99171f376fb1ce6ba19b43a93b830457e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532612"
---
# <span data-ttu-id="1321a-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="1321a-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="1321a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1321a-102">SYNOPSIS</span></span>
<span data-ttu-id="1321a-103">데이터베이스에 대 한 데이터 마스킹 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1321a-103">Gets the data masking policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1321a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1321a-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1321a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1321a-105">DESCRIPTION</span></span>
<span data-ttu-id="1321a-106">**AzureRmSqlDatabaseDataMaskingPolicy** Cmdlet은 Azure SQL 데이터베이스의 데이터 마스킹 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1321a-106">The **Get-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="1321a-107">이 cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="1321a-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="1321a-108">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1321a-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1321a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1321a-109">EXAMPLES</span></span>

### <span data-ttu-id="1321a-110">예제 1: Azure SQL 데이터베이스에 대 한 데이터 마스킹 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="1321a-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="1321a-111">이 명령은 서버 Server01의 리소스 그룹 ResourceGroup01에서 데이터베이스 Database01의 데이터 마스킹 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1321a-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="1321a-112">변수</span><span class="sxs-lookup"><span data-stu-id="1321a-112">PARAMETERS</span></span>

### <span data-ttu-id="1321a-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1321a-113">-DatabaseName</span></span>
<span data-ttu-id="1321a-114">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1321a-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="1321a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1321a-115">-DefaultProfile</span></span>
<span data-ttu-id="1321a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1321a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1321a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1321a-117">-ResourceGroupName</span></span>
<span data-ttu-id="1321a-118">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1321a-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="1321a-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1321a-119">-ServerName</span></span>
<span data-ttu-id="1321a-120">데이터베이스가 있는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1321a-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="1321a-121">-확인</span><span class="sxs-lookup"><span data-stu-id="1321a-121">-Confirm</span></span>
<span data-ttu-id="1321a-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1321a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1321a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1321a-123">-WhatIf</span></span>
<span data-ttu-id="1321a-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1321a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1321a-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1321a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1321a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1321a-126">CommonParameters</span></span>
<span data-ttu-id="1321a-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1321a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1321a-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1321a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1321a-129">입력</span><span class="sxs-lookup"><span data-stu-id="1321a-129">INPUTS</span></span>

### <span data-ttu-id="1321a-130">않아야</span><span class="sxs-lookup"><span data-stu-id="1321a-130">None</span></span>
<span data-ttu-id="1321a-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1321a-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1321a-132">출력</span><span class="sxs-lookup"><span data-stu-id="1321a-132">OUTPUTS</span></span>

### <span data-ttu-id="1321a-133">DatabaseDataMaskingPolicyModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="1321a-133">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="1321a-134">상속자</span><span class="sxs-lookup"><span data-stu-id="1321a-134">NOTES</span></span>

## <span data-ttu-id="1321a-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1321a-135">RELATED LINKS</span></span>

[<span data-ttu-id="1321a-136">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1321a-136">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="1321a-137">새로운 AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1321a-137">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="1321a-138">제거-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1321a-138">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="1321a-139">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="1321a-139">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="1321a-140">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1321a-140">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)



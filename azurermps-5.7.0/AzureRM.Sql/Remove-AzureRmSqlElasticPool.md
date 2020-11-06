---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
ms.openlocfilehash: a6b5b21b8911aa8d156ced40476d1b0ecadad361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528770"
---
# <span data-ttu-id="daa59-101">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="daa59-101">Remove-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="daa59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daa59-102">SYNOPSIS</span></span>
<span data-ttu-id="daa59-103">탄력적 데이터베이스 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="daa59-103">Deletes an elastic database pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="daa59-104">구문과</span><span class="sxs-lookup"><span data-stu-id="daa59-104">SYNTAX</span></span>

```
Remove-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="daa59-105">설명은</span><span class="sxs-lookup"><span data-stu-id="daa59-105">DESCRIPTION</span></span>
<span data-ttu-id="daa59-106">**AzureRmSqlElasticPool** Cmdlet은 Azure SQL Database 탄력적인 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="daa59-106">The **Remove-AzureRmSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="daa59-107">예제의</span><span class="sxs-lookup"><span data-stu-id="daa59-107">EXAMPLES</span></span>

### <span data-ttu-id="daa59-108">예제 1: 탄력적 풀 삭제</span><span class="sxs-lookup"><span data-stu-id="daa59-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="daa59-109">이 명령은 ElasticPool01 이라는 탄력적 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="daa59-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="daa59-110">변수</span><span class="sxs-lookup"><span data-stu-id="daa59-110">PARAMETERS</span></span>

### <span data-ttu-id="daa59-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa59-111">-DefaultProfile</span></span>
<span data-ttu-id="daa59-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="daa59-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="daa59-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="daa59-113">-ElasticPoolName</span></span>
<span data-ttu-id="daa59-114">이 cmdlet이 삭제 하는 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daa59-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daa59-115">-Force</span><span class="sxs-lookup"><span data-stu-id="daa59-115">-Force</span></span>
<span data-ttu-id="daa59-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="daa59-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daa59-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daa59-117">-ResourceGroupName</span></span>
<span data-ttu-id="daa59-118">탄력적 풀이 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daa59-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="daa59-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="daa59-119">-ServerName</span></span>
<span data-ttu-id="daa59-120">탄력적 풀을 호스팅하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daa59-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="daa59-121">-확인</span><span class="sxs-lookup"><span data-stu-id="daa59-121">-Confirm</span></span>
<span data-ttu-id="daa59-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="daa59-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daa59-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daa59-123">-WhatIf</span></span>
<span data-ttu-id="daa59-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="daa59-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daa59-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="daa59-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daa59-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa59-126">CommonParameters</span></span>
<span data-ttu-id="daa59-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="daa59-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa59-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daa59-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa59-129">입력</span><span class="sxs-lookup"><span data-stu-id="daa59-129">INPUTS</span></span>

### <span data-ttu-id="daa59-130">ElasticPool. AzureSqlElasticPoolModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="daa59-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="daa59-131">출력</span><span class="sxs-lookup"><span data-stu-id="daa59-131">OUTPUTS</span></span>

### <span data-ttu-id="daa59-132">ElasticPool. AzureSqlElasticPoolModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="daa59-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="daa59-133">상속자</span><span class="sxs-lookup"><span data-stu-id="daa59-133">NOTES</span></span>

## <span data-ttu-id="daa59-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="daa59-134">RELATED LINKS</span></span>

[<span data-ttu-id="daa59-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="daa59-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="daa59-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="daa59-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="daa59-137">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="daa59-137">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="daa59-138">새로운 AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="daa59-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="daa59-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="daa59-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="daa59-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="daa59-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



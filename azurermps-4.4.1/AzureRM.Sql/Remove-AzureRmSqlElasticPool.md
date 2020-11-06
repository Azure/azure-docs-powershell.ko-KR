---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
ms.openlocfilehash: 57f5f656f3c85e9d1c0d29c07a602a303208e7f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531807"
---
# <span data-ttu-id="5e7c2-101">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5e7c2-101">Remove-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="5e7c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e7c2-102">SYNOPSIS</span></span>
<span data-ttu-id="5e7c2-103">탄력적 데이터베이스 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c2-103">Deletes an elastic database pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e7c2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5e7c2-104">SYNTAX</span></span>

```
Remove-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e7c2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5e7c2-105">DESCRIPTION</span></span>
<span data-ttu-id="5e7c2-106">**AzureRmSqlElasticPool** Cmdlet은 Azure SQL Database 탄력적인 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c2-106">The **Remove-AzureRmSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="5e7c2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5e7c2-107">EXAMPLES</span></span>

### <span data-ttu-id="5e7c2-108">예제 1: 탄력적 풀 삭제</span><span class="sxs-lookup"><span data-stu-id="5e7c2-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="5e7c2-109">이 명령은 ElasticPool01 이라는 탄력적 풀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c2-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="5e7c2-110">변수</span><span class="sxs-lookup"><span data-stu-id="5e7c2-110">PARAMETERS</span></span>

### <span data-ttu-id="5e7c2-111">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5e7c2-111">-ElasticPoolName</span></span>
<span data-ttu-id="5e7c2-112">이 cmdlet이 삭제 하는 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c2-112">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e7c2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5e7c2-113">-Force</span></span>
<span data-ttu-id="5e7c2-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c2-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e7c2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e7c2-115">-ResourceGroupName</span></span>
<span data-ttu-id="5e7c2-116">탄력적 풀이 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c2-116">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="5e7c2-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5e7c2-117">-ServerName</span></span>
<span data-ttu-id="5e7c2-118">탄력적 풀을 호스팅하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c2-118">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="5e7c2-119">-확인</span><span class="sxs-lookup"><span data-stu-id="5e7c2-119">-Confirm</span></span>
<span data-ttu-id="5e7c2-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e7c2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e7c2-121">-WhatIf</span></span>
<span data-ttu-id="5e7c2-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e7c2-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e7c2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e7c2-124">-DefaultProfile</span></span>
<span data-ttu-id="5e7c2-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e7c2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e7c2-126">CommonParameters</span></span>
<span data-ttu-id="5e7c2-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e7c2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e7c2-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e7c2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e7c2-129">입력</span><span class="sxs-lookup"><span data-stu-id="5e7c2-129">INPUTS</span></span>

### <span data-ttu-id="5e7c2-130">ElasticPool. AzureSqlElasticPoolModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="5e7c2-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="5e7c2-131">출력</span><span class="sxs-lookup"><span data-stu-id="5e7c2-131">OUTPUTS</span></span>

### <span data-ttu-id="5e7c2-132">ElasticPool. AzureSqlElasticPoolModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="5e7c2-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="5e7c2-133">상속자</span><span class="sxs-lookup"><span data-stu-id="5e7c2-133">NOTES</span></span>

## <span data-ttu-id="5e7c2-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e7c2-134">RELATED LINKS</span></span>

[<span data-ttu-id="5e7c2-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5e7c2-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="5e7c2-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="5e7c2-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="5e7c2-137">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="5e7c2-137">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="5e7c2-138">새로운 AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5e7c2-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="5e7c2-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5e7c2-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="5e7c2-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="5e7c2-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



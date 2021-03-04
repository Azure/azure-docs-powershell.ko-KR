---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: 565d22bc2860acc69f5d919bf000a564d9295ce5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955163"
---
# <span data-ttu-id="6fcd8-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6fcd8-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="6fcd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fcd8-102">SYNOPSIS</span></span>
<span data-ttu-id="6fcd8-103">탄력적 데이터베이스 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6fcd8-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="6fcd8-104">구문</span><span class="sxs-lookup"><span data-stu-id="6fcd8-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6fcd8-105">설명</span><span class="sxs-lookup"><span data-stu-id="6fcd8-105">DESCRIPTION</span></span>
<span data-ttu-id="6fcd8-106">**Remove-AzSqlElasticPool** cmdlet은 Azure SQL 탄력적 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6fcd8-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="6fcd8-107">예제</span><span class="sxs-lookup"><span data-stu-id="6fcd8-107">EXAMPLES</span></span>

### <span data-ttu-id="6fcd8-108">예제 1: 탄력적 풀 삭제</span><span class="sxs-lookup"><span data-stu-id="6fcd8-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="6fcd8-109">이 명령은 ElasticPool01이라는 탄력적 풀을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6fcd8-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="6fcd8-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6fcd8-110">PARAMETERS</span></span>

### <span data-ttu-id="6fcd8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fcd8-111">-DefaultProfile</span></span>
<span data-ttu-id="6fcd8-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6fcd8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6fcd8-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6fcd8-113">-ElasticPoolName</span></span>
<span data-ttu-id="6fcd8-114">이 cmdlet이 삭제하는 탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6fcd8-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="6fcd8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6fcd8-115">-Force</span></span>
<span data-ttu-id="6fcd8-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6fcd8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6fcd8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fcd8-117">-ResourceGroupName</span></span>
<span data-ttu-id="6fcd8-118">탄력적 풀이 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6fcd8-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="6fcd8-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6fcd8-119">-ServerName</span></span>
<span data-ttu-id="6fcd8-120">탄력적 풀을 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6fcd8-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="6fcd8-121">-확인</span><span class="sxs-lookup"><span data-stu-id="6fcd8-121">-Confirm</span></span>
<span data-ttu-id="6fcd8-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6fcd8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fcd8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fcd8-123">-WhatIf</span></span>
<span data-ttu-id="6fcd8-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6fcd8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fcd8-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6fcd8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fcd8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fcd8-126">CommonParameters</span></span>
<span data-ttu-id="6fcd8-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6fcd8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fcd8-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fcd8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fcd8-129">입력</span><span class="sxs-lookup"><span data-stu-id="6fcd8-129">INPUTS</span></span>

### <span data-ttu-id="6fcd8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6fcd8-130">System.String</span></span>

## <span data-ttu-id="6fcd8-131">출력</span><span class="sxs-lookup"><span data-stu-id="6fcd8-131">OUTPUTS</span></span>

### <span data-ttu-id="6fcd8-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="6fcd8-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="6fcd8-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6fcd8-133">NOTES</span></span>

## <span data-ttu-id="6fcd8-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6fcd8-134">RELATED LINKS</span></span>

[<span data-ttu-id="6fcd8-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6fcd8-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="6fcd8-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="6fcd8-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="6fcd8-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="6fcd8-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="6fcd8-138">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6fcd8-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="6fcd8-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="6fcd8-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="6fcd8-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="6fcd8-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



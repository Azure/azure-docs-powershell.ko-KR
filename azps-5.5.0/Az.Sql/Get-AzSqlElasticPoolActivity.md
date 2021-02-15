---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 2e0768b14337f4504df1e6cdf9565533584e0339
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188940"
---
# <span data-ttu-id="1a966-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="1a966-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="1a966-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a966-102">SYNOPSIS</span></span>
<span data-ttu-id="1a966-103">탄력적 풀에 대한 작업의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1a966-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="1a966-104">구문</span><span class="sxs-lookup"><span data-stu-id="1a966-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a966-105">설명</span><span class="sxs-lookup"><span data-stu-id="1a966-105">DESCRIPTION</span></span>
<span data-ttu-id="1a966-106">**Get-AzSqlElasticPoolActivity** cmdlet은 Azure SQL Database에 대한 탄력적 풀의 작업 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1a966-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="1a966-107">풀 만들기 및 구성 업데이트의 상태를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a966-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="1a966-108">예제</span><span class="sxs-lookup"><span data-stu-id="1a966-108">EXAMPLES</span></span>

### <span data-ttu-id="1a966-109">예제 1: 탄력적 풀에 대한 작업 상태 확인</span><span class="sxs-lookup"><span data-stu-id="1a966-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="1a966-110">이 명령은 ElasticPool01이라는 탄력적 풀에 대한 작업의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1a966-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="1a966-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a966-111">PARAMETERS</span></span>

### <span data-ttu-id="1a966-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a966-112">-DefaultProfile</span></span>
<span data-ttu-id="1a966-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1a966-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a966-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="1a966-114">-ElasticPoolName</span></span>
<span data-ttu-id="1a966-115">탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a966-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="1a966-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="1a966-116">-OperationId</span></span>
<span data-ttu-id="1a966-117">검색할 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1a966-117">The ID of the operation to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a966-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a966-118">-ResourceGroupName</span></span>
<span data-ttu-id="1a966-119">탄력적 풀이 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a966-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="1a966-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1a966-120">-ServerName</span></span>
<span data-ttu-id="1a966-121">탄력적 풀을 포함하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a966-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="1a966-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a966-122">-Confirm</span></span>
<span data-ttu-id="1a966-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a966-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a966-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a966-124">-WhatIf</span></span>
<span data-ttu-id="1a966-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1a966-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a966-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a966-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a966-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a966-127">CommonParameters</span></span>
<span data-ttu-id="1a966-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1a966-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a966-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1a966-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a966-130">입력</span><span class="sxs-lookup"><span data-stu-id="1a966-130">INPUTS</span></span>

### <span data-ttu-id="1a966-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1a966-131">System.String</span></span>

### <span data-ttu-id="1a966-132">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1a966-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1a966-133">출력</span><span class="sxs-lookup"><span data-stu-id="1a966-133">OUTPUTS</span></span>

### <span data-ttu-id="1a966-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="1a966-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="1a966-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1a966-135">NOTES</span></span>

## <span data-ttu-id="1a966-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a966-136">RELATED LINKS</span></span>

[<span data-ttu-id="1a966-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1a966-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="1a966-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="1a966-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="1a966-139">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1a966-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="1a966-140">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1a966-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="1a966-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1a966-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)



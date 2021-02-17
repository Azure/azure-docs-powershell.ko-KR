---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
ms.openlocfilehash: dc1dffd84a95bd9cffac1dbafb5183d56e0b7c52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207853"
---
# <span data-ttu-id="e081e-101">Stop-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="e081e-101">Stop-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="e081e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e081e-102">SYNOPSIS</span></span>
<span data-ttu-id="e081e-103">탄력적 풀에서 비동기 업데이트 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="e081e-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="e081e-104">구문</span><span class="sxs-lookup"><span data-stu-id="e081e-104">SYNTAX</span></span>

```
Stop-AzSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e081e-105">설명</span><span class="sxs-lookup"><span data-stu-id="e081e-105">DESCRIPTION</span></span>
<span data-ttu-id="e081e-106">**Stop-AzSqlElasticPoolActivity** cmdlet은 탄력적 풀에서 비동기 업데이트 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="e081e-106">The **Stop-AzSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="e081e-107">예제</span><span class="sxs-lookup"><span data-stu-id="e081e-107">EXAMPLES</span></span>

### <span data-ttu-id="e081e-108">예제 1: 탄력적 풀에서 비동기 업데이트 작업 취소</span><span class="sxs-lookup"><span data-stu-id="e081e-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : ElasticPool01
State           : CANCELLED
Operation       : UpdateLogicalElasticPool
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete :
```

<span data-ttu-id="e081e-109">이 명령은 탄력적 풀에서 비동기 업데이트 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="e081e-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="e081e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e081e-110">PARAMETERS</span></span>

### <span data-ttu-id="e081e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e081e-111">-DefaultProfile</span></span>
<span data-ttu-id="e081e-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e081e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e081e-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e081e-113">-ElasticPoolName</span></span>
<span data-ttu-id="e081e-114">Azure SQL 탄력적 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e081e-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="e081e-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e081e-115">-OperationId</span></span>
<span data-ttu-id="e081e-116">검색할 작업의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e081e-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="e081e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e081e-117">-PassThru</span></span>
<span data-ttu-id="e081e-118">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="e081e-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e081e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e081e-119">-ResourceGroupName</span></span>
<span data-ttu-id="e081e-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e081e-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="e081e-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e081e-121">-ServerName</span></span>
<span data-ttu-id="e081e-122">탄력적 풀이 SQL Server Azure 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e081e-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="e081e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e081e-123">-Confirm</span></span>
<span data-ttu-id="e081e-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e081e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e081e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e081e-125">-WhatIf</span></span>
<span data-ttu-id="e081e-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e081e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e081e-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e081e-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e081e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e081e-128">CommonParameters</span></span>
<span data-ttu-id="e081e-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e081e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e081e-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e081e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e081e-131">입력</span><span class="sxs-lookup"><span data-stu-id="e081e-131">INPUTS</span></span>

### <span data-ttu-id="e081e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e081e-132">System.String</span></span>

### <span data-ttu-id="e081e-133">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e081e-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e081e-134">출력</span><span class="sxs-lookup"><span data-stu-id="e081e-134">OUTPUTS</span></span>

### <span data-ttu-id="e081e-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="e081e-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="e081e-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e081e-136">NOTES</span></span>

## <span data-ttu-id="e081e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e081e-137">RELATED LINKS</span></span>

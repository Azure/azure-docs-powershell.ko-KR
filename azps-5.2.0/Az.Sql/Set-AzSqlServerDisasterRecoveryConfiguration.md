---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: c49eb386265dff2650ba9bdb0882d25be98fca0c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355490"
---
# <span data-ttu-id="d9208-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9208-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="d9208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9208-102">SYNOPSIS</span></span>
<span data-ttu-id="d9208-103">데이터베이스 서버 복구 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9208-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="d9208-104">구문</span><span class="sxs-lookup"><span data-stu-id="d9208-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9208-105">설명</span><span class="sxs-lookup"><span data-stu-id="d9208-105">DESCRIPTION</span></span>
<span data-ttu-id="d9208-106">**Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet은 SQL 데이터베이스 서버 복구 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9208-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="d9208-107">예제</span><span class="sxs-lookup"><span data-stu-id="d9208-107">EXAMPLES</span></span>

## <span data-ttu-id="d9208-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9208-108">PARAMETERS</span></span>

### <span data-ttu-id="d9208-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="d9208-109">-AllowDataLoss</span></span>
<span data-ttu-id="d9208-110">장애 조치(failover) 작업이 데이터 손실을 허용하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d9208-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="d9208-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9208-111">-AsJob</span></span>
<span data-ttu-id="d9208-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d9208-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9208-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9208-113">-DefaultProfile</span></span>
<span data-ttu-id="d9208-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d9208-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9208-115">-장애 조치(failover)</span><span class="sxs-lookup"><span data-stu-id="d9208-115">-Failover</span></span>
<span data-ttu-id="d9208-116">이 작업이 장애 조치(failover)를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d9208-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9208-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9208-117">-ResourceGroupName</span></span>
<span data-ttu-id="d9208-118">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9208-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d9208-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d9208-119">-ServerName</span></span>
<span data-ttu-id="d9208-120">데이터베이스 서버의 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9208-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="d9208-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="d9208-121">-VirtualEndpointName</span></span>
<span data-ttu-id="d9208-122">가상 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9208-122">Specifies the name of a virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9208-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9208-123">-Confirm</span></span>
<span data-ttu-id="d9208-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9208-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9208-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9208-125">-WhatIf</span></span>
<span data-ttu-id="d9208-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d9208-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9208-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9208-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9208-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9208-128">CommonParameters</span></span>
<span data-ttu-id="d9208-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d9208-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9208-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d9208-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9208-131">입력</span><span class="sxs-lookup"><span data-stu-id="d9208-131">INPUTS</span></span>

### <span data-ttu-id="d9208-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d9208-132">System.String</span></span>

## <span data-ttu-id="d9208-133">출력</span><span class="sxs-lookup"><span data-stu-id="d9208-133">OUTPUTS</span></span>

### <span data-ttu-id="d9208-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="d9208-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="d9208-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d9208-135">NOTES</span></span>

## <span data-ttu-id="d9208-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9208-136">RELATED LINKS</span></span>

[<span data-ttu-id="d9208-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9208-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d9208-138">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9208-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d9208-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9208-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="d9208-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="d9208-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

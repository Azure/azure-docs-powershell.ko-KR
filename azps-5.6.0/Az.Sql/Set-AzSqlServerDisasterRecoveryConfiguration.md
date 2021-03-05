---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a1f91c01d3183551cbabf58754fbe628e1feea32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992390"
---
# <span data-ttu-id="56cbb-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="56cbb-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="56cbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="56cbb-103">데이터베이스 서버 복구 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="56cbb-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="56cbb-104">구문</span><span class="sxs-lookup"><span data-stu-id="56cbb-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56cbb-105">설명</span><span class="sxs-lookup"><span data-stu-id="56cbb-105">DESCRIPTION</span></span>
<span data-ttu-id="56cbb-106">**Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet은 데이터베이스 서버 복구 SQL 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="56cbb-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="56cbb-107">예제</span><span class="sxs-lookup"><span data-stu-id="56cbb-107">EXAMPLES</span></span>

## <span data-ttu-id="56cbb-108">매개 변수</span><span class="sxs-lookup"><span data-stu-id="56cbb-108">PARAMETERS</span></span>

### <span data-ttu-id="56cbb-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="56cbb-109">-AllowDataLoss</span></span>
<span data-ttu-id="56cbb-110">장애 조치(failover) 작업이 데이터 손실을 허용하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56cbb-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="56cbb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56cbb-111">-AsJob</span></span>
<span data-ttu-id="56cbb-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="56cbb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56cbb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56cbb-113">-DefaultProfile</span></span>
<span data-ttu-id="56cbb-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="56cbb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56cbb-115">-Failover</span><span class="sxs-lookup"><span data-stu-id="56cbb-115">-Failover</span></span>
<span data-ttu-id="56cbb-116">이 작업은 장애 조치(failover)를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56cbb-116">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="56cbb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56cbb-117">-ResourceGroupName</span></span>
<span data-ttu-id="56cbb-118">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56cbb-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="56cbb-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="56cbb-119">-ServerName</span></span>
<span data-ttu-id="56cbb-120">데이터베이스 서버의 이름을 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56cbb-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="56cbb-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="56cbb-121">-VirtualEndpointName</span></span>
<span data-ttu-id="56cbb-122">가상 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="56cbb-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="56cbb-123">-확인</span><span class="sxs-lookup"><span data-stu-id="56cbb-123">-Confirm</span></span>
<span data-ttu-id="56cbb-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="56cbb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56cbb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56cbb-125">-WhatIf</span></span>
<span data-ttu-id="56cbb-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="56cbb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56cbb-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56cbb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56cbb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56cbb-128">CommonParameters</span></span>
<span data-ttu-id="56cbb-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="56cbb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56cbb-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56cbb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56cbb-131">입력</span><span class="sxs-lookup"><span data-stu-id="56cbb-131">INPUTS</span></span>

### <span data-ttu-id="56cbb-132">System.String</span><span class="sxs-lookup"><span data-stu-id="56cbb-132">System.String</span></span>

## <span data-ttu-id="56cbb-133">출력</span><span class="sxs-lookup"><span data-stu-id="56cbb-133">OUTPUTS</span></span>

### <span data-ttu-id="56cbb-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="56cbb-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="56cbb-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="56cbb-135">NOTES</span></span>

## <span data-ttu-id="56cbb-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56cbb-136">RELATED LINKS</span></span>

[<span data-ttu-id="56cbb-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="56cbb-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="56cbb-138">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="56cbb-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="56cbb-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="56cbb-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="56cbb-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="56cbb-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

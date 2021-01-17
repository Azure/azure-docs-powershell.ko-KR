---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a294fd3db4ded19dba2ebd55547ec1c6cbfa9c68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491589"
---
# <span data-ttu-id="65df2-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="65df2-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="65df2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65df2-102">SYNOPSIS</span></span>
<span data-ttu-id="65df2-103">데이터베이스 서버 시스템 복구 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="65df2-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="65df2-104">구문</span><span class="sxs-lookup"><span data-stu-id="65df2-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65df2-105">설명</span><span class="sxs-lookup"><span data-stu-id="65df2-105">DESCRIPTION</span></span>
<span data-ttu-id="65df2-106">**New-AzSqlServerDisasterRecoveryConfiguration** cmdlet은 SQL 서버 시스템 복구 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="65df2-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="65df2-107">예제</span><span class="sxs-lookup"><span data-stu-id="65df2-107">EXAMPLES</span></span>

## <span data-ttu-id="65df2-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65df2-108">PARAMETERS</span></span>

### <span data-ttu-id="65df2-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65df2-109">-AsJob</span></span>
<span data-ttu-id="65df2-110">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="65df2-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65df2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65df2-111">-DefaultProfile</span></span>
<span data-ttu-id="65df2-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="65df2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65df2-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="65df2-113">-FailoverPolicy</span></span>
<span data-ttu-id="65df2-114">장애 조치(failover) 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65df2-114">Specifies the failover policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65df2-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65df2-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="65df2-116">파트너 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65df2-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="65df2-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="65df2-117">-PartnerServerName</span></span>
<span data-ttu-id="65df2-118">파트너 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65df2-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="65df2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65df2-119">-ResourceGroupName</span></span>
<span data-ttu-id="65df2-120">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65df2-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="65df2-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="65df2-121">-ServerName</span></span>
<span data-ttu-id="65df2-122">서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65df2-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="65df2-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="65df2-123">-VirtualEndpointName</span></span>
<span data-ttu-id="65df2-124">가상 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65df2-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="65df2-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65df2-125">-Confirm</span></span>
<span data-ttu-id="65df2-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="65df2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65df2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65df2-127">-WhatIf</span></span>
<span data-ttu-id="65df2-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="65df2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65df2-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65df2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65df2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65df2-130">CommonParameters</span></span>
<span data-ttu-id="65df2-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="65df2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65df2-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="65df2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65df2-133">입력</span><span class="sxs-lookup"><span data-stu-id="65df2-133">INPUTS</span></span>

### <span data-ttu-id="65df2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="65df2-134">System.String</span></span>

## <span data-ttu-id="65df2-135">출력</span><span class="sxs-lookup"><span data-stu-id="65df2-135">OUTPUTS</span></span>

### <span data-ttu-id="65df2-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="65df2-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="65df2-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="65df2-137">NOTES</span></span>

## <span data-ttu-id="65df2-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65df2-138">RELATED LINKS</span></span>

[<span data-ttu-id="65df2-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="65df2-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="65df2-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="65df2-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="65df2-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="65df2-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="65df2-142">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="65df2-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

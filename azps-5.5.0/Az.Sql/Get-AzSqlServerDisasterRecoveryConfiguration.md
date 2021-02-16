---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: b4cbf71dc4b9a04a3070bab22266ba28f88b2131
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209208"
---
# <span data-ttu-id="e001e-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e001e-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="e001e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e001e-102">SYNOPSIS</span></span>
<span data-ttu-id="e001e-103">데이터베이스 서버 시스템 복구 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e001e-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="e001e-104">구문</span><span class="sxs-lookup"><span data-stu-id="e001e-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e001e-105">설명</span><span class="sxs-lookup"><span data-stu-id="e001e-105">DESCRIPTION</span></span>
<span data-ttu-id="e001e-106">**Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet은 SQL 서버 시스템 복구 구성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e001e-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="e001e-107">예제</span><span class="sxs-lookup"><span data-stu-id="e001e-107">EXAMPLES</span></span>

## <span data-ttu-id="e001e-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e001e-108">PARAMETERS</span></span>

### <span data-ttu-id="e001e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e001e-109">-DefaultProfile</span></span>
<span data-ttu-id="e001e-110">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e001e-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e001e-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e001e-111">-ResourceGroupName</span></span>
<span data-ttu-id="e001e-112">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e001e-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e001e-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e001e-113">-ServerName</span></span>
<span data-ttu-id="e001e-114">데이터베이스 서버의 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e001e-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="e001e-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="e001e-115">-VirtualEndpointName</span></span>
<span data-ttu-id="e001e-116">가상 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e001e-116">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="e001e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e001e-117">-Confirm</span></span>
<span data-ttu-id="e001e-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e001e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e001e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e001e-119">-WhatIf</span></span>
<span data-ttu-id="e001e-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e001e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e001e-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e001e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e001e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e001e-122">CommonParameters</span></span>
<span data-ttu-id="e001e-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e001e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e001e-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e001e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e001e-125">입력</span><span class="sxs-lookup"><span data-stu-id="e001e-125">INPUTS</span></span>

### <span data-ttu-id="e001e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e001e-126">System.String</span></span>

## <span data-ttu-id="e001e-127">출력</span><span class="sxs-lookup"><span data-stu-id="e001e-127">OUTPUTS</span></span>

### <span data-ttu-id="e001e-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="e001e-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="e001e-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e001e-129">NOTES</span></span>

## <span data-ttu-id="e001e-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e001e-130">RELATED LINKS</span></span>

[<span data-ttu-id="e001e-131">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e001e-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e001e-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e001e-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e001e-133">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e001e-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e001e-134">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="e001e-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

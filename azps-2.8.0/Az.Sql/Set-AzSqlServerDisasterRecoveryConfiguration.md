---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: b3a84fc37e747cb54571bc26563789599fac3a7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873738"
---
# <span data-ttu-id="0f03c-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f03c-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="0f03c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f03c-102">SYNOPSIS</span></span>
<span data-ttu-id="0f03c-103">데이터베이스 서버 복구 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f03c-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="0f03c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0f03c-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f03c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0f03c-105">DESCRIPTION</span></span>
<span data-ttu-id="0f03c-106">**AzSqlServerDisasterRecoveryConfiguration** CMDLET은 SQL 데이터베이스 서버 복구 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f03c-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="0f03c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0f03c-107">EXAMPLES</span></span>

## <span data-ttu-id="0f03c-108">변수</span><span class="sxs-lookup"><span data-stu-id="0f03c-108">PARAMETERS</span></span>

### <span data-ttu-id="0f03c-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="0f03c-109">-AllowDataLoss</span></span>
<span data-ttu-id="0f03c-110">장애 조치 (failover) 작업을 통해 데이터 손실이 허용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0f03c-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="0f03c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f03c-111">-AsJob</span></span>
<span data-ttu-id="0f03c-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0f03c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f03c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f03c-113">-DefaultProfile</span></span>
<span data-ttu-id="0f03c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0f03c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f03c-115">-장애 조치</span><span class="sxs-lookup"><span data-stu-id="0f03c-115">-Failover</span></span>
<span data-ttu-id="0f03c-116">이 작업이 장애 조치 (failover) 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0f03c-116">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="0f03c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f03c-117">-ResourceGroupName</span></span>
<span data-ttu-id="0f03c-118">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f03c-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0f03c-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0f03c-119">-ServerName</span></span>
<span data-ttu-id="0f03c-120">SQL 데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f03c-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="0f03c-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="0f03c-121">-VirtualEndpointName</span></span>
<span data-ttu-id="0f03c-122">가상 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f03c-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="0f03c-123">-확인</span><span class="sxs-lookup"><span data-stu-id="0f03c-123">-Confirm</span></span>
<span data-ttu-id="0f03c-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f03c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f03c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f03c-125">-WhatIf</span></span>
<span data-ttu-id="0f03c-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0f03c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f03c-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f03c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f03c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f03c-128">CommonParameters</span></span>
<span data-ttu-id="0f03c-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0f03c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f03c-130">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0f03c-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f03c-131">입력</span><span class="sxs-lookup"><span data-stu-id="0f03c-131">INPUTS</span></span>

### <span data-ttu-id="0f03c-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0f03c-132">System.String</span></span>

## <span data-ttu-id="0f03c-133">출력</span><span class="sxs-lookup"><span data-stu-id="0f03c-133">OUTPUTS</span></span>

### <span data-ttu-id="0f03c-134">ServerDisasterRecoveryConfiguration. AzureSqlServerDisasterRecoveryConfigurationModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="0f03c-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="0f03c-135">상속자</span><span class="sxs-lookup"><span data-stu-id="0f03c-135">NOTES</span></span>

## <span data-ttu-id="0f03c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f03c-136">RELATED LINKS</span></span>

[<span data-ttu-id="0f03c-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f03c-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="0f03c-138">새로운 AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f03c-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="0f03c-139">제거-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f03c-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="0f03c-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="0f03c-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

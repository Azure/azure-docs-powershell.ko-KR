---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 8f1400ba07444a5fc14d2a3194edd9fe960aaccc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873603"
---
# <span data-ttu-id="28819-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="28819-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="28819-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28819-102">SYNOPSIS</span></span>
<span data-ttu-id="28819-103">데이터베이스 서버 시스템 복구 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="28819-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="28819-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28819-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28819-105">설명은</span><span class="sxs-lookup"><span data-stu-id="28819-105">DESCRIPTION</span></span>
<span data-ttu-id="28819-106">**AzSqlServerDisasterRecoveryConfiguration** CMDLET은 SQL 데이터베이스 서버 시스템 복구 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="28819-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="28819-107">예제의</span><span class="sxs-lookup"><span data-stu-id="28819-107">EXAMPLES</span></span>

## <span data-ttu-id="28819-108">변수</span><span class="sxs-lookup"><span data-stu-id="28819-108">PARAMETERS</span></span>

### <span data-ttu-id="28819-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28819-109">-AsJob</span></span>
<span data-ttu-id="28819-110">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="28819-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28819-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28819-111">-DefaultProfile</span></span>
<span data-ttu-id="28819-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="28819-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28819-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="28819-113">-FailoverPolicy</span></span>
<span data-ttu-id="28819-114">장애 조치 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28819-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="28819-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28819-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="28819-116">파트너 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28819-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="28819-117">-(-)-(서버 이름)</span><span class="sxs-lookup"><span data-stu-id="28819-117">-PartnerServerName</span></span>
<span data-ttu-id="28819-118">파트너 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28819-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="28819-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28819-119">-ResourceGroupName</span></span>
<span data-ttu-id="28819-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28819-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="28819-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="28819-121">-ServerName</span></span>
<span data-ttu-id="28819-122">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28819-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="28819-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="28819-123">-VirtualEndpointName</span></span>
<span data-ttu-id="28819-124">가상 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28819-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="28819-125">-확인</span><span class="sxs-lookup"><span data-stu-id="28819-125">-Confirm</span></span>
<span data-ttu-id="28819-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="28819-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28819-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28819-127">-WhatIf</span></span>
<span data-ttu-id="28819-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="28819-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28819-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28819-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28819-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28819-130">CommonParameters</span></span>
<span data-ttu-id="28819-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28819-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28819-132">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="28819-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28819-133">입력</span><span class="sxs-lookup"><span data-stu-id="28819-133">INPUTS</span></span>

### <span data-ttu-id="28819-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="28819-134">System.String</span></span>

## <span data-ttu-id="28819-135">출력</span><span class="sxs-lookup"><span data-stu-id="28819-135">OUTPUTS</span></span>

### <span data-ttu-id="28819-136">ServerDisasterRecoveryConfiguration. AzureSqlServerDisasterRecoveryConfigurationModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="28819-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="28819-137">상속자</span><span class="sxs-lookup"><span data-stu-id="28819-137">NOTES</span></span>

## <span data-ttu-id="28819-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28819-138">RELATED LINKS</span></span>

[<span data-ttu-id="28819-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="28819-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="28819-140">제거-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="28819-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="28819-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="28819-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="28819-142">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="28819-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

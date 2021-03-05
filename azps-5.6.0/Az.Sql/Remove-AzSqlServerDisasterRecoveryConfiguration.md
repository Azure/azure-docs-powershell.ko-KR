---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 10da2a625eb3858e77343275246d8a142fefc504
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995171"
---
# <span data-ttu-id="8c073-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c073-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="8c073-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c073-102">SYNOPSIS</span></span>
<span data-ttu-id="8c073-103">데이터베이스 서버 SQL 복구 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8c073-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="8c073-104">구문</span><span class="sxs-lookup"><span data-stu-id="8c073-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c073-105">설명</span><span class="sxs-lookup"><span data-stu-id="8c073-105">DESCRIPTION</span></span>
<span data-ttu-id="8c073-106">**Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet은 데이터베이스 서버 시스템 복구 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8c073-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="8c073-107">예제</span><span class="sxs-lookup"><span data-stu-id="8c073-107">EXAMPLES</span></span>

## <span data-ttu-id="8c073-108">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8c073-108">PARAMETERS</span></span>

### <span data-ttu-id="8c073-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c073-109">-DefaultProfile</span></span>
<span data-ttu-id="8c073-110">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8c073-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c073-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8c073-111">-Force</span></span>
<span data-ttu-id="8c073-112">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8c073-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8c073-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c073-113">-ResourceGroupName</span></span>
<span data-ttu-id="8c073-114">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8c073-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8c073-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8c073-115">-ServerName</span></span>
<span data-ttu-id="8c073-116">데이터베이스 서버의 이름을 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8c073-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="8c073-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="8c073-117">-VirtualEndpointName</span></span>
<span data-ttu-id="8c073-118">가상 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8c073-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="8c073-119">-확인</span><span class="sxs-lookup"><span data-stu-id="8c073-119">-Confirm</span></span>
<span data-ttu-id="8c073-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c073-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c073-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c073-121">-WhatIf</span></span>
<span data-ttu-id="8c073-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8c073-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c073-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8c073-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c073-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c073-124">CommonParameters</span></span>
<span data-ttu-id="8c073-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8c073-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c073-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c073-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c073-127">입력</span><span class="sxs-lookup"><span data-stu-id="8c073-127">INPUTS</span></span>

### <span data-ttu-id="8c073-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8c073-128">System.String</span></span>

## <span data-ttu-id="8c073-129">출력</span><span class="sxs-lookup"><span data-stu-id="8c073-129">OUTPUTS</span></span>

### <span data-ttu-id="8c073-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="8c073-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="8c073-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8c073-131">NOTES</span></span>

## <span data-ttu-id="8c073-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c073-132">RELATED LINKS</span></span>

[<span data-ttu-id="8c073-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c073-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="8c073-134">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c073-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="8c073-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c073-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="8c073-136">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="8c073-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: 68e81a7f51ca385d5671698ad8624f523ae98c53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962624"
---
# <span data-ttu-id="c79af-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="c79af-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="c79af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c79af-102">SYNOPSIS</span></span>
<span data-ttu-id="c79af-103">데이터베이스 서버 시스템 복구 구성에 대한 활동을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c79af-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="c79af-104">구문</span><span class="sxs-lookup"><span data-stu-id="c79af-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c79af-105">설명</span><span class="sxs-lookup"><span data-stu-id="c79af-105">DESCRIPTION</span></span>
<span data-ttu-id="c79af-106">**Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet은 데이터베이스 서버 시스템 복구 구성에 대한 SQL 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c79af-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="c79af-107">예제</span><span class="sxs-lookup"><span data-stu-id="c79af-107">EXAMPLES</span></span>

## <span data-ttu-id="c79af-108">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c79af-108">PARAMETERS</span></span>

### <span data-ttu-id="c79af-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c79af-109">-DefaultProfile</span></span>
<span data-ttu-id="c79af-110">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c79af-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c79af-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="c79af-111">-OperationId</span></span>
<span data-ttu-id="c79af-112">작업 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c79af-112">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="c79af-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c79af-113">-ResourceGroupName</span></span>
<span data-ttu-id="c79af-114">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c79af-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c79af-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c79af-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="c79af-116">서버 시스템 복구 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c79af-116">Specifies the name of the server system recovery configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79af-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c79af-117">-ServerName</span></span>
<span data-ttu-id="c79af-118">서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c79af-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="c79af-119">-확인</span><span class="sxs-lookup"><span data-stu-id="c79af-119">-Confirm</span></span>
<span data-ttu-id="c79af-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c79af-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c79af-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c79af-121">-WhatIf</span></span>
<span data-ttu-id="c79af-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c79af-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c79af-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c79af-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c79af-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c79af-124">CommonParameters</span></span>
<span data-ttu-id="c79af-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c79af-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c79af-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c79af-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c79af-127">입력</span><span class="sxs-lookup"><span data-stu-id="c79af-127">INPUTS</span></span>

### <span data-ttu-id="c79af-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c79af-128">System.String</span></span>

### <span data-ttu-id="c79af-129">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c79af-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c79af-130">출력</span><span class="sxs-lookup"><span data-stu-id="c79af-130">OUTPUTS</span></span>

### <span data-ttu-id="c79af-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="c79af-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="c79af-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c79af-132">NOTES</span></span>

## <span data-ttu-id="c79af-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c79af-133">RELATED LINKS</span></span>

[<span data-ttu-id="c79af-134">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="c79af-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

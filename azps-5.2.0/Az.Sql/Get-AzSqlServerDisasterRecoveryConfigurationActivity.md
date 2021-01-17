---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: ad3c257366513a5cc9998b4e4edea8879dc38545
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350078"
---
# <span data-ttu-id="130dc-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="130dc-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="130dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="130dc-102">SYNOPSIS</span></span>
<span data-ttu-id="130dc-103">데이터베이스 서버 시스템 복구 구성에 대한 활동을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="130dc-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="130dc-104">구문</span><span class="sxs-lookup"><span data-stu-id="130dc-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="130dc-105">설명</span><span class="sxs-lookup"><span data-stu-id="130dc-105">DESCRIPTION</span></span>
<span data-ttu-id="130dc-106">**Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet은 SQL 서버 시스템 복구 구성에 대한 활동을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="130dc-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="130dc-107">예제</span><span class="sxs-lookup"><span data-stu-id="130dc-107">EXAMPLES</span></span>

## <span data-ttu-id="130dc-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="130dc-108">PARAMETERS</span></span>

### <span data-ttu-id="130dc-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="130dc-109">-DefaultProfile</span></span>
<span data-ttu-id="130dc-110">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="130dc-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="130dc-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="130dc-111">-OperationId</span></span>
<span data-ttu-id="130dc-112">작업 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="130dc-112">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="130dc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="130dc-113">-ResourceGroupName</span></span>
<span data-ttu-id="130dc-114">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="130dc-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="130dc-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="130dc-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="130dc-116">서버 시스템 복구 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="130dc-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="130dc-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="130dc-117">-ServerName</span></span>
<span data-ttu-id="130dc-118">서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="130dc-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="130dc-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="130dc-119">-Confirm</span></span>
<span data-ttu-id="130dc-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="130dc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="130dc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="130dc-121">-WhatIf</span></span>
<span data-ttu-id="130dc-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="130dc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="130dc-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="130dc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="130dc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="130dc-124">CommonParameters</span></span>
<span data-ttu-id="130dc-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="130dc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="130dc-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="130dc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="130dc-127">입력</span><span class="sxs-lookup"><span data-stu-id="130dc-127">INPUTS</span></span>

### <span data-ttu-id="130dc-128">System.String</span><span class="sxs-lookup"><span data-stu-id="130dc-128">System.String</span></span>

### <span data-ttu-id="130dc-129">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="130dc-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="130dc-130">출력</span><span class="sxs-lookup"><span data-stu-id="130dc-130">OUTPUTS</span></span>

### <span data-ttu-id="130dc-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span><span class="sxs-lookup"><span data-stu-id="130dc-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="130dc-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="130dc-132">NOTES</span></span>

## <span data-ttu-id="130dc-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="130dc-133">RELATED LINKS</span></span>

[<span data-ttu-id="130dc-134">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="130dc-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

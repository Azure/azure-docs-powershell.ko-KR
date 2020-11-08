---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 41D63CC1-5E9F-48D3-89DE-0F753C7475F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfigurationactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfigurationActivity.md
ms.openlocfilehash: ad3c257366513a5cc9998b4e4edea8879dc38545
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204284"
---
# <span data-ttu-id="039e0-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span><span class="sxs-lookup"><span data-stu-id="039e0-101">Get-AzSqlServerDisasterRecoveryConfigurationActivity</span></span>

## <span data-ttu-id="039e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="039e0-102">SYNOPSIS</span></span>
<span data-ttu-id="039e0-103">데이터베이스 서버 시스템 복구 구성에 대 한 활동을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="039e0-103">Gets activity for a database server system recovery configuration.</span></span>

## <span data-ttu-id="039e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="039e0-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfigurationActivity [-ServerName] <String>
 -ServerDisasterRecoveryConfigurationName <String> [-OperationId <Guid>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="039e0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="039e0-105">DESCRIPTION</span></span>
<span data-ttu-id="039e0-106">**AzSqlServerDisasterRecoveryConfigurationActivity** CMDLET은 SQL 데이터베이스 서버 시스템 복구 구성에 대 한 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="039e0-106">The **Get-AzSqlServerDisasterRecoveryConfigurationActivity** cmdlet gets activity for a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="039e0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="039e0-107">EXAMPLES</span></span>

## <span data-ttu-id="039e0-108">변수</span><span class="sxs-lookup"><span data-stu-id="039e0-108">PARAMETERS</span></span>

### <span data-ttu-id="039e0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="039e0-109">-DefaultProfile</span></span>
<span data-ttu-id="039e0-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="039e0-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="039e0-111">-OperationId</span><span class="sxs-lookup"><span data-stu-id="039e0-111">-OperationId</span></span>
<span data-ttu-id="039e0-112">작업 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="039e0-112">Specifies the operation ID.</span></span>

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

### <span data-ttu-id="039e0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="039e0-113">-ResourceGroupName</span></span>
<span data-ttu-id="039e0-114">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="039e0-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="039e0-115">-ServerDisasterRecoveryConfigurationName</span><span class="sxs-lookup"><span data-stu-id="039e0-115">-ServerDisasterRecoveryConfigurationName</span></span>
<span data-ttu-id="039e0-116">서버 시스템 복구 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="039e0-116">Specifies the name of the server system recovery configuration.</span></span>

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

### <span data-ttu-id="039e0-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="039e0-117">-ServerName</span></span>
<span data-ttu-id="039e0-118">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="039e0-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="039e0-119">-확인</span><span class="sxs-lookup"><span data-stu-id="039e0-119">-Confirm</span></span>
<span data-ttu-id="039e0-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="039e0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="039e0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="039e0-121">-WhatIf</span></span>
<span data-ttu-id="039e0-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="039e0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="039e0-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="039e0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="039e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="039e0-124">CommonParameters</span></span>
<span data-ttu-id="039e0-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="039e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="039e0-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="039e0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="039e0-127">입력</span><span class="sxs-lookup"><span data-stu-id="039e0-127">INPUTS</span></span>

### <span data-ttu-id="039e0-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="039e0-128">System.String</span></span>

### <span data-ttu-id="039e0-129">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="039e0-129">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="039e0-130">출력</span><span class="sxs-lookup"><span data-stu-id="039e0-130">OUTPUTS</span></span>

### <span data-ttu-id="039e0-131">ServerDisasterRecoveryConfiguration. AzureSqlServerDisasterRecoveryConfigurationActivityModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="039e0-131">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationActivityModel</span></span>

## <span data-ttu-id="039e0-132">상속자</span><span class="sxs-lookup"><span data-stu-id="039e0-132">NOTES</span></span>

## <span data-ttu-id="039e0-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="039e0-133">RELATED LINKS</span></span>

[<span data-ttu-id="039e0-134">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="039e0-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

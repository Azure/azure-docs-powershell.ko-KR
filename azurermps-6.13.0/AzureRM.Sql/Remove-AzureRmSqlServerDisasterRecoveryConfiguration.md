---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 3b5a512e5c301e328bf556d63d7ecb9191a08c5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711312"
---
# <span data-ttu-id="48f25-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="48f25-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="48f25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48f25-102">SYNOPSIS</span></span>
<span data-ttu-id="48f25-103">SQL 데이터베이스 서버 시스템 복구 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f25-103">Removes a SQL database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48f25-104">구문과</span><span class="sxs-lookup"><span data-stu-id="48f25-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48f25-105">설명은</span><span class="sxs-lookup"><span data-stu-id="48f25-105">DESCRIPTION</span></span>
<span data-ttu-id="48f25-106">**AzureRmSqlServerDisasterRecoveryConfiguration** CMDLET은 SQL 데이터베이스 서버 시스템 복구 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f25-106">The **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="48f25-107">예제의</span><span class="sxs-lookup"><span data-stu-id="48f25-107">EXAMPLES</span></span>

## <span data-ttu-id="48f25-108">변수</span><span class="sxs-lookup"><span data-stu-id="48f25-108">PARAMETERS</span></span>

### <span data-ttu-id="48f25-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48f25-109">-DefaultProfile</span></span>
<span data-ttu-id="48f25-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="48f25-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f25-111">-Force</span><span class="sxs-lookup"><span data-stu-id="48f25-111">-Force</span></span>
<span data-ttu-id="48f25-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f25-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="48f25-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48f25-113">-ResourceGroupName</span></span>
<span data-ttu-id="48f25-114">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f25-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="48f25-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="48f25-115">-ServerName</span></span>
<span data-ttu-id="48f25-116">SQL 데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f25-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="48f25-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="48f25-117">-VirtualEndpointName</span></span>
<span data-ttu-id="48f25-118">가상 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f25-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="48f25-119">-확인</span><span class="sxs-lookup"><span data-stu-id="48f25-119">-Confirm</span></span>
<span data-ttu-id="48f25-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f25-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48f25-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48f25-121">-WhatIf</span></span>
<span data-ttu-id="48f25-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="48f25-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48f25-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="48f25-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48f25-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f25-124">CommonParameters</span></span>
<span data-ttu-id="48f25-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f25-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f25-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48f25-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f25-127">입력</span><span class="sxs-lookup"><span data-stu-id="48f25-127">INPUTS</span></span>

### <span data-ttu-id="48f25-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="48f25-128">System.String</span></span>

## <span data-ttu-id="48f25-129">출력</span><span class="sxs-lookup"><span data-stu-id="48f25-129">OUTPUTS</span></span>

### <span data-ttu-id="48f25-130">ServerDisasterRecoveryConfiguration. AzureSqlServerDisasterRecoveryConfigurationModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="48f25-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="48f25-131">상속자</span><span class="sxs-lookup"><span data-stu-id="48f25-131">NOTES</span></span>

## <span data-ttu-id="48f25-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48f25-132">RELATED LINKS</span></span>

[<span data-ttu-id="48f25-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="48f25-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="48f25-134">새로운 AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="48f25-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="48f25-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="48f25-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="48f25-136">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="48f25-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

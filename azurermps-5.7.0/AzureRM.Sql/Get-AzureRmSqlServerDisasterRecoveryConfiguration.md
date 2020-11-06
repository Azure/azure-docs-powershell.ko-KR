---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 483b71d53dfb4754a4fa5f00331b07a685102782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528777"
---
# <span data-ttu-id="38f09-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="38f09-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="38f09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38f09-102">SYNOPSIS</span></span>
<span data-ttu-id="38f09-103">데이터베이스 서버 시스템 복구 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="38f09-103">Gets a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38f09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="38f09-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38f09-105">설명은</span><span class="sxs-lookup"><span data-stu-id="38f09-105">DESCRIPTION</span></span>
<span data-ttu-id="38f09-106">**Get-AzureRmSqlServerDisasterRecoveryConfiguration** CMDLET은 SQL 데이터베이스 서버 시스템 복구 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="38f09-106">The **Get-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="38f09-107">예제의</span><span class="sxs-lookup"><span data-stu-id="38f09-107">EXAMPLES</span></span>

## <span data-ttu-id="38f09-108">변수</span><span class="sxs-lookup"><span data-stu-id="38f09-108">PARAMETERS</span></span>

### <span data-ttu-id="38f09-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f09-109">-DefaultProfile</span></span>
<span data-ttu-id="38f09-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="38f09-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f09-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38f09-111">-ResourceGroupName</span></span>
<span data-ttu-id="38f09-112">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38f09-112">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38f09-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="38f09-113">-ServerName</span></span>
<span data-ttu-id="38f09-114">SQL 데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38f09-114">Specifies the name of SQL database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38f09-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="38f09-115">-VirtualEndpointName</span></span>
<span data-ttu-id="38f09-116">가상 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="38f09-116">Specifies the name of the virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f09-117">-확인</span><span class="sxs-lookup"><span data-stu-id="38f09-117">-Confirm</span></span>
<span data-ttu-id="38f09-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="38f09-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f09-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38f09-119">-WhatIf</span></span>
<span data-ttu-id="38f09-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="38f09-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38f09-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38f09-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f09-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f09-122">CommonParameters</span></span>
<span data-ttu-id="38f09-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="38f09-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f09-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38f09-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f09-125">입력</span><span class="sxs-lookup"><span data-stu-id="38f09-125">INPUTS</span></span>

### <span data-ttu-id="38f09-126">않아야</span><span class="sxs-lookup"><span data-stu-id="38f09-126">None</span></span>
<span data-ttu-id="38f09-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38f09-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38f09-128">출력</span><span class="sxs-lookup"><span data-stu-id="38f09-128">OUTPUTS</span></span>

## <span data-ttu-id="38f09-129">상속자</span><span class="sxs-lookup"><span data-stu-id="38f09-129">NOTES</span></span>

## <span data-ttu-id="38f09-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38f09-130">RELATED LINKS</span></span>

[<span data-ttu-id="38f09-131">새로운 AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="38f09-131">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="38f09-132">제거-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="38f09-132">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="38f09-133">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="38f09-133">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="38f09-134">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="38f09-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

